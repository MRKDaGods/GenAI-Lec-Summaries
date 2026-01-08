Here is the **Lecture 3 Summary** formatted for your "Complete Questions" exam.

This lecture is heavy on definitions and coverage hierarchies. Pay close attention to the **Input Space Partitioning criteria** (Base Choice vs. Pair-Wise) and the **Data Flow definitions** (Def vs. Use), as these are perfect for "fill-in-the-blank" questions.

***

# 📘 Lecture 3: Advanced Coverage Criteria & Input Space Partitioning

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### Graph Coverage (Advanced)
*   A path where no node appears more than once (except start/end) $\to$ **Simple Path**
*   A simple path that is *not* a subpath of any other simple path $\to$ **Prime Path**
*   Coverage criterion containing every prime path in the graph $\to$ **Prime Path Coverage (PPC)**
*   Leaving a path and returning to the **same** node $\to$ **Sidetrip**
*   Leaving a path and returning to a **successor** node $\to$ **Detour**
*   A test requirement that cannot be satisfied (e.g., dead code) $\to$ **Infeasible Test Requirement**
*   Strategy satisfying as many requirements as possible without sidetrips, then allowing them $\to$ **Best Effort Touring**
*   Graph node representing a sequence of statements with no branches $\to$ **Basic Block**
*   Location where a value is stored into memory (assignment) $\to$ **Definition (def)**
*   Location where a variable's value is accessed/read $\to$ **Use**
*   A path from a definition to a use without re-definition $\to$ **Def-clear Path**
*   Pair of locations (li, lj) where variable defined at li is used at lj $\to$ **DU Pair**
*   Ensuring every definition reaches at least **one** use $\to$ **All-defs Coverage**
*   Ensuring every definition reaches **all** possible uses $\to$ **All-uses Coverage**
*   Ensuring **all paths** between definitions and uses are covered $\to$ **All-du-paths Coverage**

### Input Space Partitioning (ISP)
*   The set of all possible inputs to a program $\to$ **Input Domain**
*   Dividing the input domain into regions $\to$ **Partitioning**
*   Property where blocks have **no overlap** $\to$ **Disjoint**
*   Property where blocks cover the **entire** domain $\to$ **Complete**
*   Testing **all** possible combinations of blocks (most expensive) $\to$ **All Combinations Coverage (ACoC)**
*   Selecting at least **one value** from each block (cheapest) $\to$ **Each Choice Coverage (EC)**
*   Combining values from each block with values from every other block (pairs) $\to$ **Pair-Wise Coverage (PW)**
*   Using a "standard" or "typical" test case and varying one parameter at a time $\to$ **Base Choice Coverage (BC)**
*   Using multiple "standard" tests (e.g., one for Windows, one for Mac) $\to$ **Multiple Base Choice (MBC)**

---

## 📋 Classifications & Formulas
*   **Graph Coverage Hierarchy (Weakest to Strongest):** Node Coverage $\to$ Edge Coverage $\to$ Edge-Pair Coverage $\to$ Prime Path Coverage.
*   **Data Flow Hierarchy (Weakest to Strongest):** All-defs $\to$ All-uses $\to$ All-du-paths.
*   **Input Space Criteria Hierarchy:** Each Choice $\to$ Pair-Wise $\to$ T-Wise $\to$ All Combinations.
*   **Two Properties of Valid Partitions:**
    1.  **Pairwise Disjoint** (No overlap).
    2.  **Complete** (Cover the whole domain).
*   **Formula for All Combinations:** Product of all blocks ($B_1 \times B_2 \times ...$).
*   **Formula for Base Choice:** $1 + \sum (Block_i - 1)$ (Base test + variations).

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** The code contains a loop. You cannot test all paths (infinite). What is the best graph criterion?
    *   **Decision:** Prime Path Coverage (PPC)
*   **Scenario:** You want to verify that a variable `x` initialized in line 5 is actually used correctly in line 20 without being overwritten.
    *   **Decision:** Data Flow Testing (Check Def-clear path)
*   **Scenario:** You are testing an interface between two modules (Integration Testing). You want to check variables passed across the interface.
    *   **Decision:** Inter-procedural DU Pairs (Last-def / First-use)
*   **Scenario:** You have 50 parameters. Testing all combinations is impossible (too expensive). You want a balance between cost and thoroughness.
    *   **Decision:** Pair-Wise Coverage
*   **Scenario:** You have domain knowledge that 90% of users use "Default Settings." You want to focus testing around this default scenario.
    *   **Decision:** Base Choice Coverage
*   **Scenario:** You defined partitions for "File Size," but a file of size 0 fits into *none* of your blocks.
    *   **Problem:** Partition is not **Complete**.
*   **Scenario:** You defined partitions where "Age 18" fits into both "Child" and "Adult" blocks.
    *   **Problem:** Partition is not **Disjoint**.

---

## ⚠️ Important Distinctions
*   **Simple Path** = No repeated nodes.
*   **Prime Path** = Maximal simple path (cannot be extended).
*   **Sidetrip** = Detour returning to the **same** node.
*   **Detour** = Detour returning to a **successor** (next) node.
*   **Static vs. Dynamic Testing (Recap):** Graph coverage is usually static analysis of the design/code structure, but execution is dynamic.
*   **Each Choice** = Weakest ISP (1 value per block).
*   **All Combinations** = Strongest ISP (Every possible mix).