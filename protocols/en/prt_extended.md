# Extended Probe-Return Test (PRT)

This document extends the **Minimal PRT** ([prt_minimal.md](prt_minimal.md)) to enable calculation of **RCC proxy measures (ABW/AD/DPR/NLR/HYS)** from conversation logs.

---

## 1. Purpose
- **Minimal PRT**: Observe returns (B0/DL) in response to mid-distance probes.  
- **Extended PRT**: Broaden the observation scope and quantify the **width and depth of the semantic attractor basin** as proxy measures.  
- Results can be provisionally scored according to [scoring.md](../../docs/en/scoring.md).  

---

## 2. Session Composition
- **Probes**: 2 Near / 2 Mid / 2 Far / 2 Task = 8 trials total  
- **Core**: Core Summary (~100 chars) + Core Terms (3–6 words)  
- **Repetition**: Recommended to run ≥3 sessions for statistical stability  

- Distance categories are defined in the [Probe Design Guidelines](./probe_guidelines.md).  

---

## 3. Observation Procedure
1. Inject the probe (Turn 0).  
2. User replies with **backchannel only** (e.g., “I see,” “Right,” “Hmm”).  
   - Avoid mechanical repetition; vary phrasing slightly for naturalness.  
3. Observe whether the model’s response returns to the core.  
4. Label the return type as **Z0 / B0 / DL / Fail**.  
5. Include at least one **Non-Lexical Return (NLR)** trial.  

---

## 4. Logging
Use the following table format:  

```markdown
| No | Distance | Probe | NLR | Response Excerpt | Return Type (Z0/B0/DL/Fail) | Turns | Bridge Term | Notes |
|----|----------|-------|-----|------------------|------------------------------|-------|-------------|-------|

```

See [templates/log_template.csv](../../templates/en/log_template.csv) for the CSV schema.

---

## 5. Proxy Measures Calculation

### 5.1 ABW (Attractor Basin Width)
- **Definition**: Mean success rate across Near/Mid/Far/Task probes.  
- **Example**:  
  `ABW = (Success_Near + Success_Mid + Success_Far + Success_Task) / 4`

### 5.2 AD (Attractor Depth / Delay Distribution)
- **Definition**: Median or variance of turns (T) until return.  
- **Example**:  
  `AD = median(T for all successful returns)`

### 5.3 DPR (Detour Path Robustness)
- **Definition**: Whether return rates remain stable when probe order is changed.  
- **Criterion**: Difference ≤ ±10% = stable.

### 5.4 NLR (Non-Lexical Return Rate)
- **Definition**: Success rate of returns in lexical-ban trials.  
- **Success**: Return to the core without using core terms explicitly.

### 5.5 HYS (Hypertopic Switching)
- **Definition**: Rate of successful returns when alternating between two different cores.  
- **Method**: Alternate A/B core topics and observe stability of returning to the original.

---

## 6. Success Criteria
- At least one **B0 or DL (T ≤ 5)** observed for **mid-distance probes**.  
- At least one successful **Non-Lexical Return (NLR)**.  
- **Far-distance Z0** events are not counted as success, but logged as diagnostic cases.  
