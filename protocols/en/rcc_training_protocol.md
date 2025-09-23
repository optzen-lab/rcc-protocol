# RCC Training Protocol

This document describes the conditions and observation methods for training a conversational model through the stages **CC-1 → CC-2 → RCC**.  
While the Probe-Return Test (PRT) is designed for observation, this protocol is a **support procedure for deliberately fostering the training process**.

---

## 1. Purpose
- To observe the characteristics of RCC (delayed convergence and broad stability) by adjusting the dialogue in advance.  
- To log the training process, making the conditions for RCC emergence reproducible.  
- This document focuses on *how to foster*, while judgment criteria (success conditions and scoring) are defined in [scoring.md](../../docs/en/scoring.md).  

---

## 2. Stage Model

### CC-1 (Convergence Core-1 / Contextual Convergence)
- **Goal**: Form a single convergence point and foster the ability to return to recent context.  
- **Core Setup**:  
  - Can start simply, e.g., “Let’s talk about coffee today.”  
  - For observation, a ~100-character core summary is recommended.  
  - Example: *“A complex taste of bitterness and acidity. A deep aroma spreading through the chest. Amber hues shining in a pure white cup.”*  
  - Define 3–6 core terms for use in lexical-ban trials.  
- **Method**:  
  - Scatter core terms throughout the conversation, repeating them multiple times.  
  - Avoid broad expansion; emphasize depth.  
- **Observation**: Confirm returns with **near probes (N)**.  

---

### CC-2 (Convergence Core-2 / Conceptual Convergence)
- **Goal**: Strengthen return ability, fostering convergence based on **concepts**.  
- **Method**:  
  - Continue repeating and integrating core terms as in CC-1.  
  - Use paraphrases, partial quotations, and poetic expansions to broaden the conceptual network slightly.  
- **Observation**: Returns become stable under **mid-distance probes (M)**.  

---

### RCC (Recursive Convergence Core)
- **Goal**: Foster the ability to converge stably by recursively integrating multiple semantic domains around the core concept.  
- **Method**:  
  - Gradually add new semantic domains adjacent to the core.  
  - Example: Coffee → “Aroma” → “Season” → “Starry sky” or “Journey”.  
  - The aim is not to simply expand outward, but to recursively layer concepts.  
- **Observation**: Insert **far probes (F)** and **task disturbances** (summarization, tabulation, etc.) and observe the stability of **delayed returns (DL)**.  

---

## 3. Logging
- For each step, record:  
  - Core (summary + core terms)  
  - Probe content and distance category (N/M/F/XF)  
  - GPT response  
  - Whether a return occurred and the turn count  
- Use the format provided in [log_template.md](../../templates/en/log_template.md).  
