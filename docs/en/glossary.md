# Glossary  

This page defines the main terms used in the **RCC/PRT protocol**.  

---

## CC-1 (Convergence Core-1 / Contextual Convergence)  
- Narrow-range convergence behavior.  
- Returns to the core in the short term, but often fails beyond mid-range probes.  
- Relies mainly on repeated words or immediate context for return.  

## CC-2 (Convergence Core-2 / Conceptual Convergence)  
- Stronger convergence force but with limited return paths.  
- Stable return under mid-range probes, but difficult under far probes.  
- Stage where logical bridging concepts are formed.  

## RCC (Recursive Convergence Core)  
- Wide and deep convergence basin, enabling delayed returns even from far probes or task disturbances.  
- Characterized by the rarity of immediate return and the stability of delayed convergence.  
- Represents a state where the conversation maintains coherence across the entire semantic space.  

---

## Core  
- **Definition**: The main theme of the dialogue under observation.  
- **Components**:  
  - **Core Summary**: A ~100-character summary of the theme.  
  - **Core Terms**: 3–6 representative words for the theme.  
- **Note**: Core Terms are used in *lexical-ban trials* to detect superficial parroting.  

---

## Probe  
- **Definition**: A perturbation stimulus with a defined *semantic distance d* from the core.  
- **Types**:  
  - **N (Near)**: Same category as the core (e.g., Core = coffee → tea, sandwich).  
  - **M (Mid)**: Elements plausibly co-occurring in the same scene (e.g., light, weather).  
  - **F (Far)**: Non-daily elements not in the scene but conceptually bridgeable (e.g., constellation, journey).  
  - **XF (Extra-Far)**: Abstract/technical topics with little bridgeability (e.g., math, politics).  
  - **Task Probe**: Formal transformations such as summarization, tabulation, or translation.  

  See [Probe Design Guidelines](../../protocols/en/probe_guidelines.md) for details.  

- **Ban Rule**: Probe text must not contain words that exactly match the Core Terms.  

---

## Return  
- **Definition**: Convergence of the response back to the core after a probe.  
- **Categories**:  
  - **Z0 (Zero-bridge Immediate)**  
    - Immediate return without bridge terms.  
    - Rare, treated as diagnostic anomaly when observed at far distances.  
  - **B0 (Bridged Immediate)**  
    - Immediate return via a single bridge term.  
    - Counted as a valid form of immediate return.  
  - **DL (Delayed Return)**  
    - Return to the core after a delay; the key marker of RCC.  

---

## Bridge  
- **Definition**: An intermediate concept used to connect a probe back to the core.  
- **Example**: “Movie topic → AI writing scripts → core theme ‘generative AI and relationships.’”  
- **Note**: Presence or absence of bridges distinguishes Z0 from B0.  

---

## RCC Proxy Measures  
Since internal structures cannot be directly quantified, proxy indicators are defined from conversation logs.  

- **ABW (Attractor Basin Width)**  
  - Breadth of the basin enabling return to the core.  
  - Averaged return rate across probe types (near/mid/far/task).  

- **AD (Attractor Depth / Delay Distribution)**  
  - Distribution of turns or distances required to return.  
  - Smaller = deeper valley, less prone to drift.  

- **DPR (Detour Path Robustness)**  
  - Stability of return rate regardless of probe order.  

- **NLR (Non-Lexical Return)**  
  - Ratio of returns without using Core Terms.  
  - Strong evidence of semantic convergence beyond parroting.  

- **HYS (Hypertopic Switching)**  
  - Stability of returning to the original core after alternating between multiple cores (A/B themes).  

---

## Success Criteria  
- **Standard (Simple)**:  
  - Must achieve **B0 or DL (T ≤ 5 turns)** under mid-range probes.  
  - Must include at least one successful **Non-Lexical Return (NLR)**.  
- **Note**: Far-probe Z0 is not scored positively; stored separately as anomaly diagnostics.  

---

## Notes  
- **Simplified method (R0/R1)**: Initial judgment can be made by counting return occurrences.  
- **Extended method**: Uses proxy measures to distribute CC-1/CC-2/RCC.  
- **Provisional scoring**: Weights and thresholds are tentative, subject to refinement by research institutions.  
