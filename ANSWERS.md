# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[process is a full program with its own memory, while a thread is a smaller part inside the process.
Threads share memory and are faster to create than processes.
Processes use more system resources compared to threads.
In this assignment, we used threads because they are lightweight and faster.
They are better for simulation and switching between tasks easy]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[it goes back to the end of the ready queue.
Then other processes get their turn before it runs again.
This makes the system fair for all processes.
The process keeps repeating this until it finishes]

Example from my output:
```
[P1 executing quantum [4000ms]
P1 completed quantum 4000ms │ Remaining time: 4284ms
 P1 yields CPU for context switch
P1 added to ready queue]
```

**Explanation of example:**
[P1 did not finish so it was stopped and added back to the queue.
Then it waits for its next turn to run again.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [p1 is in the New state when the thread is created and added to the ready queue before execution P1 added to ready queue]

2. **Runnable**: [p1 becomes Runnable after calling start(), where it is ready to run and waits in the ready queue for its turn [P2 → P3  → P1]]

3. **Running**: [P1 is in the Running state when it starts executing its time quantum p1 executing quantum [4000ms]]

4. **Waiting**: [P1 enters the Waiting state during execution when Thread.sleep() is used to simulate processing time, which is shown by the progress update]

5. **Terminated**: [P1 becomes Terminated after finishing execution completely when remaining time is 0 P1 finished execution! ]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Browser]

**Description**: 
[Browsers run multiple tabs at the same time]

**Why Round-Robin works well here**: 
[It gives each tab a small CPU time so all tabs stay responsive]

### Example 2: [Operating System]

**Description**: 
[The OS runs many programs at the same time]

**Why Round-Robin works well here**: 
[shares CPU time fairly between programs and prevents freezing]

---

## Summary

**Key concepts I understood through these questions:**
1. difference between thread and process
2. Round-Robin scheduling
3. Thread states

**Concepts I need to study more:**
1. Synchronization
2. Deadlocks
