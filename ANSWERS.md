# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
process is a program in execution. Thread is lightweight unit within process
process  has own space of memory while Thread share the same memory and resources with 
other threads in the same process . process is heavyweight entity ,expensive to creat and
manage so it's considered highy creation overhead Thread On the contrary, it is cheaper
to creat and manage because it's lightweight process and it's not require a new memory space.
 we use threads in simulation are lighter then process and we can control threads more eisye switch between them it's and more suitable in multiple tasks 


---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
 i use two diffrent variable firs 500ms and 10000ms when it was 500ms 
 the context switch was very fast and the overall progress in p1 for example at first time 53% and the burst time 937ms and the remaining time 437ms and The process goes to the back of the Ready Queue many times
 when time quantum 10000ms the context switch was very slow in same example p1 at first time on the proceser the overall process was 76% , the burst time was 13086ms amd the remaning 
 time was 3086ms . i saw most process finsh immediately


Example from my output:

┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P2 → P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P12 → P13 → P14 → P15 → P16]
└───────────────────────────────────────────────────────────────────────────────

  ▶ P1 executing quantum [500ms] 
  ⚡ Quantum progress: [███████████████] 100%
  ⏸ P1 completed quantum 500ms │ Overall progress: [██████████░░░░░░░░░░] 53%
     Remaining time: 437ms
  ↻ P1 yields CPU for context switch

  ➕ P1 added to ready queue │ Priority: 3 │ Burst time: 937ms
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P12 → P13 → P14 → P15 → P16 → P1]
└───────────────────────────────────────────────────────────────────────────────

```
```

**Explanation of example:**
process P1 was running on the CPU for its 500ms turn. After 500ms, the process was not finished yet it still had 53% overall progress and 437ms remaining
Because the Time Quantum ended, P1 had to leave the CPU. The system then moved P1 to the back of the Ready Queue

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

1. **New**: [When is P1 in New state?]
state New for p1 when Process process = new Process(priority, "P" + i, burstTime, timeQuantum); on line 221 
in this state the p1 had be created but didn't start
1. **Runnable**: [When does P1 become Runnable?]
p1 be in Runnable when it's added to ready queue ( processQueue.add(thread);) in line 333

1. **Running**: [When is P1 Running?]
p1 be in Running when the scheduler selects it from the queue to enter in the proceser 
in line 263 currentThread.start();
1. **Waiting**: [When/why would P1 be Waiting?]
p1 be in Waiting state when the quantum time finished but the process not end yet 
so it's will go to the ready queue until the scheduler select it agin
1. **Terminated**: [When is P1 Terminated?]
p1 be in Terminated when it's finish execution and show this massage
in output { ✓ P1 finished execution!}
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [wep server Absher]

**Description**: 
wep server like Absher it's receives thousnds of requests at the same time 

**Why Round-Robin works well here**: 
round robin perfect here because it's make us sure that server will not work on one requsts
only until finshed it will switch between them very fast 


### Example 2: [pc]

**Description**: 
in pc or mobile we often open many apps in same time 
**Why Round-Robin works well here**: 
Round-Robin work very well because  the cpu swich between apps 
and dosen't work on one app only 


---

## Summary

**Key concepts I understood through these questions:**
1. Round-Robin
2. Ready Queue Behavior
3. Thread 

**Concepts I need to study more:**
1. Terminated
2. 
