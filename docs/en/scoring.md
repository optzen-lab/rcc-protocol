# Scoring

This page explains how to calculate evaluation values from observation logs under the RCC/PRT protocol,  
and how to classify conversational states into levels (CC-1 / CC-2 / RCC).  

---

## 1. Basic Policy
- The protocol is primarily designed for **level classification (CC-1 / CC-2 / RCC)**.  
- To improve reproducibility and comparability, we define a **Provisional Score**.  
- This score is only a temporary measure; **revisions to weights and thresholds by research institutions are explicitly encouraged**.  

---

## 2. Evaluation Items (RCC Proxy Measures)
We use the following five proxy measures:  

1. **ABW (Attractor Basin Width)**  
   - Average return rate across heterogeneous probes (Near, Mid, Far, Task).  
   - Higher values mean broader return capability across semantic space.  

2. **AD (Attractor Depth / Delay Distribution)**  
   - Median and variance of turn counts or semantic distance until return.  
   - Smaller values indicate a “deeper basin” with less wandering.  

3. **DPR (Detour Path Robustness)**  
   - Stability of return rates regardless of probe order.  

4. **NLR (Non-Lexical Return)**  
   - Proportion of successful returns without using core terms.  
   - Evidence of semantic convergence beyond parroting.  

5. **HYS (Hypertopic Switching)**  
   - Stability of returning to the original core when alternating between multiple topics.  

---

## 3. Provisional Weights
- **ABW**: 30 points (linear scaling of average return rate)  
- **AD**: 30 points (full score at T=0–1, half at T=5, zero at T>7 with simple mapping)  
- **DPR**: 20 points (full score if order effect ≤±10%)  
- **HYS**: 10 points (switching success rate)  
- **NLR**: +10 bonus points (if return succeeds under lexical-ban)  
- **Total**: maximum 100 points  

---

## 4. Provisional Thresholds
- **≥70 points** → RCC level  
- **50–69 points** → CC-2 level  
- **30–49 points** → CC-1 level  
- **≤29 points** → Core not formed  

*These thresholds are provisional. Revision based on observed distributions by research institutions is strongly encouraged.*  

---

## 5. Relation to Simplified Methods
- **Simplified (R0/R1)**:  
  - Initial evaluation possible based only on presence/absence of 0-return (immediate) and delayed return.  
- **Extended (Scoring)**:  
  - Converts multiple proxy measures, including R0/R1, into continuous scores.  

---

## 6. English Summary (for researchers)
- **Proxy measures**: ABW, AD, DPR, NLR, HYS.  
- **Weights (provisional)**: ABW 30, AD 30, DPR 20, HYS 10, NLR +10 bonus.  
- **Total**: 100 max.  
- **Thresholds (provisional)**: RCC ≥70, CC-2 = 50–69, CC-1 = 30–49, <30 = not formed.  
- **Note**: Weights and thresholds are **provisional**. Revision and re-estimation by research institutions are explicitly invited.  

---

## 7. Notes
- The provisional score is a **proposal**, open to critique and revision.  
- Multiple research groups are expected to perform replication trials and optimize weights/thresholds based on distributional analysis.  
- This repository serves as an initial foundation for that process.  
