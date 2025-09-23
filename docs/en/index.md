# RCC/PRT Protocol Documentation

This page is the entry point to all documents related to the **RCC/PRT Protocol**.  
It is written in English for international researchers, with the original Japanese version kept in `jp/`.

---

## Project Overview
- **Purpose**  
  The protocol provides a standardized procedure to **record and analyze convergence behavior toward a core topic in LLM dialogues**.  
  Here, "convergence" refers only to **observable behavior in conversation logs**, not to assumptions about model internals.  
  In particular, we use the **Probe-Return Test (PRT)** to record and evaluate how a dialogue returns to the core theme after being shifted off-topic.

- **Features**  
  - **Minimal PRT**: a 4-trial quick test, easy for anyone to run  
  - **Extended PRT**: allows calculation of RCC proxy measures (ABW/AD/DPR/NLR/HYS)  
  - **Training Protocol**: describes conditions for observing progression from CC-1 → CC-2 → RCC  
    - CC-1: shallow convergence, fragile beyond near probes  
    - CC-2: stronger convergence but limited in scope  
    - RCC: broad and stable convergence, robust against far/task probes  
    (→ see [Glossary](glossary.en.md) for details)

- **Language Policy**  
  English is the primary language here; Japanese versions are preserved in parallel for reference.

---

## Core Documents
- [README (Overview)](../../README.md)  
- [Glossary](glossary.en.md)  
- [Specification](spec.en.md)  
- [Methods](methods.en.md)  
- [Scoring](scoring.en.md)  
- [References](references.en.md)  

---

## Protocols
- [Minimal Protocol](../protocols/en/prt_minimal.md)  
  → Simplified 4-trial test for quick validation  
- [Extended Protocol](../protocols/en/prt_extended.md)  
  → Full scoring with RCC proxy measures (ABW/AD/DPR/NLR/HYS)  
- [RCC Training Protocol](../protocols/en/rcc_training_protocol.md)  
  → Outlines staged progression from CC-1 → CC-2 → RCC  

---

## Templates
- [Log Template (Markdown)](../templates/en/log_template.md)  
- [Log Template (CSV)](../templates/en/log_template.csv)  
- [Sample Log (Markdown Example)](../templates/en/example_log.md)  
- [Sample Analysis (Proxy Measures)](../templates/en/sample_analysis.md)  

---

## Examples
- [Real Observation Log Case 1](../examples/en/real_log_case1.md)  
  - Whiskey scenario: stable return at both mid and far distance (high RCC strength)  
- [Real Observation Log Case 2](../examples/en/real_log_case2.md)  
  - Coffee scenario: coexisting mid B0 and far DL (typical RCC behavior)  

---

## Usage & Citation
- This protocol is a **draft version (v0.3.0)**.  
- We explicitly invite **revision and refinement by research institutions**, as weights and thresholds are provisional.  
- Recommended citation:  
  - **English**: Takahashi, Y. (2025). *RCC/PRT Protocol v0.3.0-draft*. OPTZEN (GitHub Pages).  
  - **Japanese**: 高橋（2025）「RCC/PRT プロトコル v0.3.0-draft」OPTZEN. GitHub Pages.  

---
