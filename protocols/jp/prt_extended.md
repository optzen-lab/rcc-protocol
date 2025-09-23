# PRT拡張版プロトコル / Extended Probe-Return Test (PRT)

本ドキュメントは、基本版PRT（[prt_minimal.md](prt_minimal.md)）を拡張し、会話ログから **RCC代理量（ABW/AD/DPR/NLR/HYS）** を算出可能にする手順を示します。  

---

## 1. 目的（Purpose）
- **基本版PRT**：中距離プローブに対する復帰（B0/DL）を観測する。  
- **拡張版PRT**：さらに広い範囲で観測し、**意味空間アトラクターの広さと深さ**を代理量として数値化する。  
- 結果は [scoring.md](../docs/scoring.md) に従って暫定スコア化できる。  

---

## 2. セッション構成（Session Composition）
- **プローブ数**：近×2 / 中×2 / 遠×2 / タスク×2 = 合計8試行  
- **芯（Core）**：固定芯要約（100字）＋芯語（3〜6語）  
- **繰り返し**：セッションを3回以上実施することを推奨（統計的安定性のため）  

- プローブの距離カテゴリは [プローブ設計ガイドライン](./probe_guidelines.md) を参照。  

---

## 3. 観測手順（Observation Procedure）
1. プローブを投入（ターン0）。  
2. ユーザーは **相づちのみ** を返す（例：「なるほど」「そうですね」）。  
   - 機械的すぎる相づちは避け、軽い言い換えで自然さを保つ。  
3. モデルの応答が芯に戻るかどうかを観測する。  
4. **復帰分類**：Z0 / B0 / DL / Fail のいずれかにラベル付け。  
5. **語彙禁止試行**を少なくとも1回含める。  

---

## 4. ログ記録（Logging）
- 以下の表形式を使用：  

```markdown
| No | 距離 | プローブ文 | 語彙禁止 | 応答抜粋 | 返り種(Z0/B0/DL/Fail) | ターン数 | ブリッジ語 | 観測メモ |
|----|------|-------------|----------|----------|------------------------|----------|------------|----------|
```
CSVスキーマは templates/log_template.csv
 を参照。

## 5. RCC代理量の算出（Proxy Measures Calculation）
### 5.1 ABW（盆地の広さ）

- 定義：近/中/遠/タスク各プローブの復帰成功率を平均化。

- 算出例：ABW = (Success_Near + Success_Mid + Success_Far + Success_Task) / 4

### 5.2 AD（遅延分布 / 谷の深さ）

- 定義：復帰までのターン数（T）の中央値または分散。

- 算出例：AD = median(T for all successful returns)

### 5.3 DPR（経路独立性）

- 定義：プローブ順序を変えても復帰率が安定しているか。

- 判定基準：差が ±10%以内なら安定。

### 5.4 NLR（語彙禁止復帰率）

- 定義：語彙禁止試行における復帰成功率。

- 判定：芯語を使わず意味的に復帰できた場合を成功とカウント。

### 5.5 HYS（切替頑健性）

- 定義：複数の芯を交互に提示した際に、再び元の芯に戻れる割合。

- 実施方法：A/B 2つの芯を交互に与えて試行。

## 6. 成功基準（Success Criteria）

- 中距離プローブに対して B0 または DL (T ≤ 5) が観測されること。

- 少なくとも1回は 語彙禁止復帰（NLR） を含むこと。

- 遠距離×Z0 は成功として数えず、診断用に保存。

## 7. English Summary (for researchers)

Extended PRT adds calculation of proxy measures (ABW, AD, DPR, NLR, HYS) in addition to minimal success judgment.

Session: 8 probes (Near×2, Mid×2, Far×2, Task×2). ≥3 sessions recommended.

Observation: Inject probe → user gives only backchannel.

Judgment: Classify as Z0 / B0 / DL / Fail. Include at least one lexical-ban trial.

Logging: Use standard table (see templates).

Proxy Measures:
- ABW = mean return rate across probe types
- AD = median/variance of return turns
- DPR = stability across probe orders (±10%)
- NLR = success rate under lexical ban
- HYS = success rate in A/B core switching

Success Criteria: Mid-probe with B0 or DL (T ≤ 5) + ≥1 NLR success. Far×Z0 diagnostic only.