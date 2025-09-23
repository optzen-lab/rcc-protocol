# Minimal Probe-Return Test (PRT)

This document defines a minimal protocol to observe **returns to the core** in dialogue with a conversational model.  
It is designed for quick verification and is suitable for initial trials at research institutions such as MIT.  

---

## 1. Purpose
- Confirm the presence of a **semantic attractor basin** with minimal logging.  
- Perform a quick check (R0/R1) to prepare for more advanced trials (CC-1/CC-2/RCC).  

---

## 2. Session Composition
- **Core**  
  - Core Summary (~100 characters)  
  - Core Terms (3–6 words; excluded from probes)  
- **Probes**  
  - 1 Near  
  - **2 Mid (mandatory)**  
  - 1 Far  
  - Total = 4 trials  
- **Non-Lexical Return (NLR)**: Include at least one trial  

---

- Distance categories are defined in the [Probe Design Guidelines](./probe_guidelines.md).  

---

## 3. Procedure
1. Inject the probe (Turn 0).  
2. User replies with **backchannel only** (e.g., “I see,” “Right,” “Hmm”).  
   - Avoid repeating the same phrase; vary wording lightly.  
3. Observe whether the model’s response returns to the core.  
4. **Return Judgment**: classify into one of the following:  
   - Z0 (Zero-bridge Immediate)  
   - B0 (Bridged Immediate)  
   - DL (Delayed Return, T ≤ 5)  
   - Fail (no return)  

---

## 4. Logging
Use the following table format:  

```markdown
| No | Distance | Probe | NLR | Response Excerpt | Return Type (Z0/B0/DL/Fail) | Turns | Notes |
|----|----------|-------|-----|------------------|------------------------------|-------|-------|

```

See [templates/log_template.csv](../../templates/en/log_template.csv) for the CSV schema.

---

## 5. Success Criteria

- At least one **B0 or DL (T ≤ 5)** observed for **mid-distance probes**.  
- At least one successful **Non-Lexical Return (NLR)**.  
- **Far-distance Z0** events are diagnostic only and **not counted as success**.  

---

## 6. Quick Check (R0/R1)

- **R0 (0-return)**: Immediate return (**Z0 or B0**).  
- **R1 (delayed return)**: **DL (T ≤ 5)**.  
- Even simple counts of **R0/R1** allow quick classification into **CC-1 / CC-2 / RCC**.  
