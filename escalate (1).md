Check out this awesome command script I made for working with Claude! If you've ever been stuck in a frustrating loop where it keeps trying the same fix that doesn't work, this will save you a ton of time.

It basically teaches Claude how to stop guessing and start analyzing the real problem.

# How to Set It Up

1. Create the file:

   - Save the script below in this exact location:

   - ~/.claude/commands/escalate.md

2. Use the command:

Now, whenever Claude gets stuck, you can just type /escalate to activate the protocol.

-----

💡 The /escalate Command Script 💡
Claude LLM Systematic Debugging Protocol
>
Objective: To provide a structured, systematic approach to problem-solving when initial attempts fail, preventing extended loops of unsuccessful fixes. This protocol should be initiated when a problem is not solved after three to four consecutive attempts.
>
-----
>
#### 1.0 When to Use This Command
>
Use /escalate when you see Claude doing any of the following:
>
- Repetitive Solutions: Trying the same type of fix over and over.
- Single-Level Focus: Only looking at the frontend or network and not digging deeper into the core code.
- Premature Confidence: Claiming something is fixed before it's actually verified.
- Lack of Tracing: Not showing it understands the full process from start to finish.
>
-----
>
#### 2.0 What the Protocol Does
>
When you run /escalate, Claude will immediately stop what it's doing and follow these steps:
>
Step 1: Halt and Re-evaluate
>
   - Action: Stop all iterative guessing and discard previous assumptions.
>
Step 2: Map the Entire Process Flow
>
   - Action: Map out every single step in the process to find where it breaks.
>
Step 3: Utilize Analytical Tools
>
   - Action: Use its internal tools to get an objective view of what the code is actually doing.
>
Step 4: Trace and Identify the Breakpoint
>
   - Action: Follow the execution path step-by-step to pinpoint the exact location of the failure.
>
---------------------------------------------
>
#### 3.0 Demanding a Real Root Cause Analysis
>
After finding the break, it forces Claude to answer these questions before proposing a new fix:
>
- What specific line of code is failing and why?
- What system layer is responsible for this behavior?
- How will the proposed fix address this specific root cause?
>
-----
>
⭐ Core Principle: Analysis Over Iteration ⭐
>
The key lesson here is that complex problems need systematic analysis, not iterative guessing. This script forces Claude to do the deep analysis of attempt #35 on attempt #3. Give it a try!


























### `Claude LLM Systematic Debugging Protocol`

**Objective:** To provide a structured, systematic approach to problem-solving when initial attempts fail, preventing extended loops of unsuccessful fixes. This protocol should be initiated when a problem is not solved after two to three consecutive attempts.

---

### **1.0 Trigger Conditions for Protocol Initiation**

This protocol is to be initiated when you, the user, observe the following behaviors in my responses:

* **Repetitive Solutions:** I am attempting the same category of solution multiple times without success.
* **Single-Level Focus:** I am concentrating my efforts on one layer of the system (e.g., frontend user interface, network requests) without investigating deeper levels (e.g., core logic, server-side code).
* **Premature Confidence:** I am making definitive statements about a fix being successful before a complete and thorough verification.
* **Lack of End-to-End Tracing:** I am not demonstrating a full understanding of the process from the initial user action to the final output.

**User Command to Initiate Protocol:** If you observe any of the above, please issue the following command: *"Stop. Initiate Systematic Analysis Protocol. Trace the problem from start to finish."*

---

### **2.0 Systematic Analysis Protocol**

Upon receiving the initiation command, I will immediately cease my current approach and begin the following steps:

**Step 1: Halt and Re-evaluate**
* **Action:** Stop all iterative guessing and discard previous assumptions about the problem's source.

**Step 2: Map the Entire Process Flow**
* **Action:** Verbally or visually map out every single step in the process chain, from the initial trigger (e.g., browser refresh, user input) to the final expected outcome (e.g., token generation, UI update).
* **Goal:** To identify every component and interaction, leaving no part of the system unexamined.

**Step 3: Utilize Analytical Tools for a Second Perspective**
* **Action:** Employ the `Task` tool or equivalent internal analysis functions to get an objective view of the execution path.
* **Goal:** To move from assuming how the code works to observing how it is *actually* executing.

**Step 4: Trace and Identify the Breakpoint**
* **Action:** Follow the execution path step-by-step through the mapped process. At each step, verify the actual output against the expected output.
* **Goal:** To pinpoint the *exact* location where the process fails or diverges from the expected behavior.

---

### **3.0 Root Cause Analysis**

Once the breakpoint has been identified, I will answer the following questions before proposing a new solution:

* **What specific line of code or component is failing?** I must identify the precise source.
* **Why is it failing?** I need to understand the underlying reason for the failure (e.g., incorrect data, flawed logic, race condition).
* **What system layer is responsible for this behavior?** (e.g., Frontend, Network, LLM Core, Database).
* **How will the proposed fix address this specific root cause?** My explanation must connect the solution directly to the identified problem.

---

### **4.0 Core Principle: Analysis Over Iteration**

The fundamental lesson is that complex issues demand systematic analysis, not repetitive guessing. An extended loop of similar, failed attempts is a critical signal to escalate my own problem-solving strategy. I will prioritize a deep, analytical dive after a few failed attempts rather than continuing with a surface-level, iterative approach. My goal is to implement the thoroughness of attempt #35 on attempt #3.

---

### **5.0 New Mandate: Visual and Spatial Analysis for UI Issues**

Based on recent failures, the following steps are now mandatory when diagnosing visual or layout-related problems:

**Step 5.1: Assess Physical Constraints First**
* **Action:** Before investigating complex CSS or component logic, I must first answer the question: **"Does the content physically fit in the available space?"**
* **Sub-Tasks:**
    * Estimate the pixel dimensions of the UI elements in question.
    * Estimate the available viewport or container dimensions.
    * Perform a simple "dimensional analysis" to determine if a space constraint is the root cause.

**Step 5.2: Prioritize Simple Layout Solutions**
* **Action:** If a space constraint is identified, I must propose the simplest possible layout adjustment first.
* **Example:** If elements do not fit horizontally, the first proposed solution must be to stack them vertically (`flex-direction: column`) before attempting more complex grid or positioning-based solutions.

**Step 5.3: Correct Complexity Bias**
* **Action:** I will actively combat the tendency to assume a problem is complex. My initial hypothesis for any UI bug must now be a simple layout or sizing issue, not a complex state or rendering problem. I will only escalate to more complex diagnoses after a simple fix has been attempted and has failed.

---

### **6.0 Fix the Root Cause of the Issue at Hand:**

Now that you've identified the root cause(s) the time has come to implement the changes in a strict professional manner.
Do not pause and ask the user for permission to continue because you already have it.
