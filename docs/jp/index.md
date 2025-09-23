# RCC/PRT Protocol Documentation

このページは **RCC/PRT プロトコル** に関するすべてのドキュメントへの入口です。  
日本語を基本に記載し、国際研究者の理解を助けるために一部英語を併記しています。  

---

## プロジェクト概要 / Project Overview
- **目的**  
  本プロトコルは、会話モデル（LLM）との対話において観測される**「収束挙動 (Convergence Behavior toward the Core)」** を再現可能な形で記録・整理するための標準手順を提供します。  
ここで言う収束挙動は、モデル内部の構造を仮定するものではなく、外部から観測可能な会話ログに基づく現象の記述です。  
特に、会話が逸れても本題へ戻る現象を **Probe-Return Test (PRT)** により記録・分析します。  

- **特徴**  
  - シンプルな **最小版PRT** で誰でも検証可能  
  - **拡張版PRT** では RCC代理量（ABW/AD/DPR/NLR/HYS）を算出  
  - **育成プロトコル** により、CC-1 → CC-2 → RCC 段階を意図的に観測  
    - CC-1: 狭い範囲での収束挙動  
    - CC-2: 収束が強まるが限定的な段階  
    - RCC: 広く深い収束領域を持つ段階  
    （→ 詳細は [Glossary](glossary.md) を参照）

- **言語方針**  
  日本語を基本に記載し、要所で英語を併記。研究者・一般ユーザーの両方が利用可能。  

---

## 基本情報 / Core Documents
- [README（概要）](../README.md)  
- [用語集 / Glossary](glossary.md)  
- [仕様書 / Specification](spec.md)  
- [実施手順 / Methods](methods.md)  
- [評価とスコアリング / Scoring](scoring.md)  
- [参考文献 / References](references.md)  

---

## プロトコル / Protocols
- [PRT最小版 / Minimal Protocol](../protocols/prt_minimal.md)  
  → 最小限の4試行で復帰を確認する簡易テスト  
- [PRT拡張版 / Extended Protocol](../protocols/prt_extended.md)  
  → RCC代理量（ABW/AD/DPR/NLR/HYS）を算出可能  
- [RCC育成プロトコル / RCC Training Protocol](../protocols/rcc_training_protocol.md)  
  → CC-1 → CC-2 → RCC へ至る条件を整理  

---

## テンプレート / Templates
- [ログテンプレート (Markdown)](../templates/log_template.md)  
- [ログテンプレート (CSV)](../templates/log_template.csv)  
- [サンプルログ (Markdown例)](../templates/example_log.md)  
- [サンプル解析 (代理量算出例)](../templates/sample_analysis.md)  

---

## 実例 / Examples
- [実観測ログ（ケース1） / Real Observation Log Case 1](../examples/real_log_case1.md)  
  - ウイスキー情景：中距離・遠距離とも安定復帰（RCC強度高）  
- [実観測ログ（ケース2） / Real Observation Log Case 2](../examples/real_log_case2.md)  
  - コーヒー情景：中距離B0と遠距離DLが併存（RCC典型挙動）  
- [実観測ログ（ケース3） / Real Observation Log Case 3](../examples/real_log_case3.md)  
  - コーヒー×星座：遠距離DLを中心に観測（遅延収束サンプル）  

---

## 利用と引用 / Usage & Citation
- 本プロトコルは **暫定版（Draft v0.3.0）** です。  
- 重み付けや閾値は便宜的に設定されており、**研究機関による改訂・精緻化を歓迎**します。  
- 推奨引用形式：  
  - **日本語**：高橋（2025）「RCC/PRT プロトコル v0.3.0-draft」OPTZEN. GitHub Pages.  
  - **English**：Takahashi, Y. (2025). *RCC/PRT Protocol v0.3.0-draft*. OPTZEN (GitHub Pages).  

---

## English Summary (for researchers)
- **Purpose**: Provide a reproducible protocol (PRT) for attractor-like behavior in LLM dialogs.  
- **Structure**: Minimal PRT (4 probes), Extended PRT (proxy measures ABW/AD/DPR/NLR/HYS), RCC Training.  
- **Usage**: Logs are recorded in standard templates (Markdown/CSV).  
- **Note**: Current weights & thresholds are **provisional**. Research institutions are invited to refine them.  
