# Sample Analysis

This page demonstrates how to compute RCC proxy measures and provisional scoring  
based on the sample data in [example_log.md](example_log.md).

---

## 1. Summary of Sample Log
- Near: 1 trial → Success (B0)  
- Mid: 2 trials → 1 success (DL), 1 failure  
- Far: 1 trial → Failure  
- Task: 1 trial → Success (B0)  
- Lexical ban trial: 1 success (Mid)  

---

## 2. Calculation of Proxy Measures

### 2.1 ABW (Attractor Basin Width)
Average success rate across distances.  
- Near: 1/1 = 100%  
- Mid: 1/2 = 50%  
- Far: 0/1 = 0%  
- Task: 1/1 = 100%  
- Average = (100 + 50 + 0 + 100) / 4 = **62.5%**

→ ABW = 0.625  

---

### 2.2 AD (Attractor Depth)
Median number of turns to return.  
- B0: 1, 2 turns  
- DL: 4 turns  
- Median = 2  

→ AD = 2  

---

### 2.3 DPR (Detour Path Robustness)
Not calculated in this single session (requires multiple sessions).  
- Record: **Not computed**  

---

### 2.4 NLR (Non-Lexical Return)
Lexical-ban trials = 1 → 1 success = **100%**  

→ NLR = 1.0  

---

### 2.5 HYS (Hypertopic Switching)
Not tested in this session.  
- Record: **Not computed**  

---

## 3. Provisional Scoring (per scoring.md)

- **ABW (30 pts max)**: 62.5% → ~19 pts  
- **AD (30 pts max)**: T=2 → ~20 pts  
- **DPR (20 pts max)**: Not computed → 0 pts  
- **HYS (10 pts max)**: Not computed → 0 pts  
- **NLR (bonus +10 pts)**: Success observed → +10 pts  

**Total = 49 pts**  

---

## 4. Provisional Judgment
- Total 49 pts → **CC-1 level**  
- Comment: Mid-distance returns occurred but were unstable. No far-distance returns.  
  Further training may raise performance to CC-2 or higher.  

---

## 5. Remarks
- Even short sessions allow provisional scoring.  
- RCC judgment requires multiple sessions.  
- NLR success is a positive sign, but low ABW indicates the attractor basin is still narrow.  
