Here is the **Lecture 2 Summary** (covering both Part I and Part II).

This lecture introduced many specific testing types and technical coverage definitions. These are prime candidates for **"Identify the Term"** questions.

***

# 📘 Lecture 2: Testing Life Cycle & Coverage Criteria

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### Part I: Testing Concepts & Lifecycle
*   Systematic process of testing activities during SDLC $\to$ **STLC (Software Testing Life Cycle)**
*   A version of software prepared for *internal* testing $\to$ **Build**
*   A stable version deployed to the *public* or production $\to$ **Release**
*   A human mistake in logic or understanding $\to$ **Error**
*   The flaw in the code caused by a human error $\to$ **Bug**
*   A bug found by a *tester* inside the testing phase $\to$ **Defect**
*   A defect found by the *end-user* in production $\to$ **Failure**
*   Quick, broad test to check if the build is stable (not smoking) $\to$ **Smoke Testing**
*   Checking if a specific fix works logically and reasonably $\to$ **Sanity Testing**
*   Testing module at max expected usage $\to$ **Load Testing**
*   Testing beyond normal limits to find breaking points $\to$ **Stress Testing**
*   Running the *same* test again to confirm a fix $\to$ **Retesting**
*   Checking if a new code change broke *existing* features $\to$ **Regression Testing**
*   Testing with valid inputs expecting success $\to$ **Positive Testing**
*   Testing with invalid inputs expecting error handling $\to$ **Negative Testing**
*   Tester learns and executes simultaneously (no script) $\to$ **Exploratory Testing**
*   Random testing without a plan or learning goal $\to$ **Ad-hoc Testing**
*   Automated random inputs to check stability $\to$ **Monkey Testing**
*   Brute-force repetitive testing of one specific module $\to$ **Gorilla Testing**
*   Document acting as a "blueprint" for testing (scope, strategy, schedule) $\to$ **Test Plan**
*   High-level description of *what* to test (simple sentence) $\to$ **Test Scenario**
*   Detailed step-by-step instructions (Input + Expected Result) $\to$ **Test Case**
*   Matrix mapping test cases to requirements $\to$ **RTM (Requirement Traceability Matrix)**

### Part II: Coverage Criteria
*   Rules/measurements to answer "Have we tested enough?" $\to$ **Coverage Criteria**
*   Coverage based on control flow graphs or state machines $\to$ **Graph Coverage**
*   Coverage based on Boolean expressions (True/False) $\to$ **Logic Coverage**
*   Coverage based on partitioning input values $\to$ **Input Space Partitioning**
*   Coverage based on injecting faults (mutants) to test robustness $\to$ **Syntax-Based Coverage**
*   Graph criteria requiring every node to be visited $\to$ **Node Coverage**
*   Graph criteria requiring every edge (length up to 1) to be visited $\to$ **Edge Coverage**
*   Graph criteria requiring paths of length up to 2 $\to$ **Edge-Pair Coverage**
*   Testing borders of partitions (where most errors happen) $\to$ **Boundary Value Analysis**
*   Modifying code slightly to see if tests fail (kill the mutant) $\to$ **Mutation Testing**

---

## 📋 Classifications & Types
*   **STLC Phases:** Requirement Analysis $\to$ Test Planning $\to$ Design $\to$ Environment Setup $\to$ Execution $\to$ Reporting $\to$ Closure.
*   **Components of a Use Case:** Actor, Preconditions, Main Flow, Alternate Flow, Postconditions.
*   **Types of Logic Coverage:** Predicate Coverage, Clause Coverage, Combinatorial Coverage.
*   **Graph Coverage Hierarchy:** Node Coverage $\subset$ Edge Coverage $\subset$ Edge-Pair Coverage.

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You receive a new build. You want to quickly ensure it installs and opens before doing detailed work.
    *   **Decision:** Smoke Testing
*   **Scenario:** A developer fixed a login bug. You verify the login works, AND you check that the "Forgot Password" link didn't break.
    *   **Decision:** Retesting (for the login) + Regression Testing (for the link)
*   **Scenario:** You have no test cases written, but you need to find bugs in a new feature by exploring it intuitively.
    *   **Decision:** Exploratory Testing
*   **Scenario:** You want to test a form. You divide ages into groups (<18, 18-60, >60) and pick one number from each.
    *   **Decision:** Equivalence Partitioning
*   **Scenario:** In the example above, you specifically test age 17, 18, 60, and 61.
    *   **Decision:** Boundary Value Analysis
*   **Scenario:** You change a `>` operator to `>=` in the code to see if your test suite catches the error.
    *   **Decision:** Mutation Testing
*   **Scenario:** You have a graph with a loop. You want to test every possible path.
    *   **Decision:** Impossible (Complete Path Coverage is not feasible with loops).

---

## ⚠️ Important Distinctions (The "Don't Confuse" List)

1.  **Error vs. Bug vs. Defect vs. Failure:**
    *   *Error:* Inside the Human's head.
    *   *Bug:* Inside the Code.
    *   *Defect:* Found during Testing.
    *   *Failure:* Found by the User (Production).

2.  **Smoke vs. Sanity:**
    *   *Smoke:* Broad, shallow, "Is the build alive?" (General Health).
    *   *Sanity:* Narrow, deep, "Did the specific change work?" (Logical verification).

3.  **Monkey vs. Gorilla:**
    *   *Monkey:* Random inputs everywhere (Chaos).
    *   *Gorilla:* Repetitive inputs on **one** module (Brute force).

4.  **Verification vs. Validation (Recap from Lec 1):**
    *   *Verification:* "Am I building it right?" (Reviews/Static).
    *   *Validation:* "Am I building the right product?" (Execution/Dynamic).