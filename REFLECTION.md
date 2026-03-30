# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**
"I learned that Multithreading allows a program to perform multiple tasks at the same time by breaking the program into smaller execution units called threads
I understood the lifecycle of a thread. I saw how a process moves from New to Runnable, and then to Running.
What Surprised Me: I was surprised by how much the Time Quantum affects everything
at first i thought it Doesn’t matter if is it large or small but when i saw the diffrent
between the i realize how much effict on everything


---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**
The most challenging part was calculating the Waiting Time accurately. At first, my program output kept showing 0ms for every process. It was difficult to understand exactly when a process 'finishes' in the scheduler loop and when to capture its end time.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**
I overcame this challenge by using systematic debugging. First, I added System.out.println statements to track the creationTime and currentTime at each step. This helped me see exactly where the calculation was failing.
I also found some people talking about this problem on Reddit that help me a lot .

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**
Modern Video Games like Fc26
in a football match, the system must handle the AI of 22 players, the ball physics, the crowd noise, and the commentary all at once.
 Each player on the pitch has their own AI thread to decide where to run. If the game used only one thread, the screen would freeze every time a player makes a decision. Using multiple threads allows the game to run smoothly at 60 frames per second.



---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
