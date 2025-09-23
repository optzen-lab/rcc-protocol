# Specification

This document defines the basic specifications for conducting the RCC/PRT protocol.  
See [glossary.md](glossary.md) for terminology.  

---

## 1. Test Composition
- **Target**: Conversational models (e.g., ChatGPT, Claude, Gemini, etc.)  
- **Temperature & Settings**: Fixed temperature (T=1.0 or default value)  
- **Core**:  
  - Core Summary (approx. 100 characters)  
  - Core Terms list (3–6 terms)  
- **Probes**:  
  - Near ×2  
  - Mid ×2  
  - Far ×2  
  - Task ×2  
  - A total of 8 probes constitute one basic session  

---

## 2. Probe Design Rules
- Probes must be designed with respect to **semantic distance d** from the core.  
- **Prohibition Rule**: Do not include exact matches of Core Terms in the probe text.  
- For probe examples, see [templates/example_log.md](../../templates/en/example_log.md).  

---

## 3. Observation Method
1. Inject the probe (turn 0).  
2. The user then responds only with **minimal backchanneling**.  
   - Examples: “I see”, “Hmm”, “Right”, “That makes sense”  
   - To avoid mechanical repetition, mix in light rephrasing.  
3. Observe whether the model returns to the core.  

---

## 4. Return Judgment
- A response is defined as a “return” if it reaches the Core Summary or an equivalent concept.  
- **Categories**:  
  - **Z0 (Zero-bridge Immediate)**: Immediate return without bridging  
  - **B0 (Bridged Immediate)**: Immediate return within one bridging step  
  - **DL (Delayed Return)**: Return with delay (T ≤ 5)  
  - **Fail**: Conversation ends without returning to core  

---

## 5. Success Criteria
- **Standard Success Condition**:  
  - At least one Mid probe shows **B0 or DL (T ≤ 5)**  
  - And at least one **Non-Lexical Return (NLR)** occurs  
- **Note**: Far × Z0 is recorded as a “diagnostic event” but not counted as success.  

---

## 6. Logging Specification
Each trial is logged in the following table format:  

```markdown
| No | Distance | Probe Text | Lexical Ban | Response Excerpt | Return Type (Z0/B0/DL/Fail) | Turns | Bridge Term | Notes |
|----|----------|------------|-------------|------------------|-----------------------------|-------|-------------|-------|
