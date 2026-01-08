
# 📘 Lecture 8: Assisting Exploratory Testing with AI (Detailed)

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### Exploratory Testing (ET) Basics
*   Testing approach combining simultaneous learning, test design, and execution $\to$ **Exploratory Testing**
*   Exploratory testing relies on the tester's creativity, intuition, and \_\_\_\_\_\_. $\to$ **Experience**
*   Is ET random testing? $\to$ **No** (It is structured and thought-out)
*   Is ET limited to UI testing? $\to$ **No** (Can test APIs, DBs, logic)
*   Is ET a replacement for automation? $\to$ **No** (It complements it)

### Approaches & Techniques (Very Important for Exam)
*   Visually organizing ideas, flows, and test conditions to uncover areas to explore $\to$ **Mind Mapping**
*   Focusing testing effort on areas with the highest potential impact or likelihood of failure $\to$ **Risk-Based Exploratory Testing**
*   Executing focused, **time-boxed** testing sessions guided by a mission $\to$ **Session-Based Testing**
*   The mission statement or guide used in Session-Based testing $\to$ **Charter**
*   Using experience and intuition to predict where defects are likely to occur $\to$ **Error Guessing**
*   Testing values at the limits of functionality (e.g., age 18 vs 17) $\to$ **Boundary & Edge Case Exploration**
*   Quick, lightweight experiments to spot bottlenecks or degradation early $\to$ **Exploratory Performance Checks**
*   Explicit rules or mental shortcuts used to generate test ideas (like Mnemonics) $\to$ **Heuristics**

### LLM Integration (Before, During, After)
*   Using LLMs to visualize main features, sub-features, and edge cases hierarchically $\to$ **Mind Mapping with AI**
*   Using LLMs to generate a list of potential failures based on feature descriptions $\to$ **Risk Analysis**
*   A specific LLM prompt that asks for "Goal, Scope, Focus, and Time box" generates a \_\_\_\_\_\_. $\to$ **Charter**
*   Technique where the LLM explains code logic to a tester to help them model the system $\to$ **Code Understanding (or Explaining Code)**
*   Using LLMs to transform rough notes into a readable report describing what was learned $\to$ **Testing Story**

### Mnemonics (Memory Aids)
*   **PAOLO:** Mnemonic for **Screen Orientation & Rendering**.
    *   **P** $\to$ Portrait
    *   **A** $\to$ Audio (Artifacts)
    *   **O** $\to$ Objects (in view)
    *   **L** $\to$ Landscape
    *   **O** $\to$ Overlay (Pop-ups)
*   **SFDIPOT:** Mnemonic for **Strategy/Perspectives** (Structure, Function, Data, Interfaces, Platform, Operations, Time).
*   **CRUD:** Mnemonic for **Data Operations** (Create, Read, Update, Delete).

---

## 📋 Lists & Classifications

### 1. When to use Exploratory Testing?
*   Changing/Unclear requirements.
*   Time pressure.
*   High-risk or complex areas.
*   Regression of tricky bugs.
*   Workflows difficult to script.
*   Unstable UIs.

### 2. Components of a Charter
*   **Goal:** What to test.
*   **Scope:** What to include/exclude.
*   **Focus:** Specific risks/bugs to look for.
*   **Time Box:** Duration (e.g., 60 minutes).

### 3. The 3 Stages of LLM Assistance in ET
1.  **Before ET:** Organizing (Mind Mapping, Risk Analysis, Charters).
2.  **During ET:** Investigating bugs, Explaining Code, Generating ideas via Mnemonics.
3.  **After ET:** Summarizing notes, Writing Testing Stories.

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Technique*

*   **Scenario:** You are testing a **Banking App**'s new "Transfer Money" feature. You skip the "Edit Profile" tests to focus on "Wrong Accounts" and "Failed Transfers" because losing money is a disaster.
    *   **Approach:** Risk-Based Exploratory Testing
*   **Scenario:** You allocate exactly **45 minutes** to test "Account Creation" and you stop when the time is up.
    *   **Approach:** Session-Based Testing (Time-boxing)
*   **Scenario:** You recall that this developer often forgets to trim spaces in usernames. You specifically test " User " with spaces.
    *   **Approach:** Error Guessing
*   **Scenario:** You upload a 10GB file just to see if the application crashes or slows down.
    *   **Approach:** Exploratory Performance Check
*   **Scenario:** You are testing a mobile game. You check how it looks when you flip the phone sideways and if the volume controls cover the menu.
    *   **Mnemonic Used:** PAOLO (Landscape / Overlay)
*   **Scenario:** You have a pile of messy bullet points from your testing session. You paste them into ChatGPT to write a professional summary for the manager.
    *   **Output Generated:** Testing Story
*   **Scenario:** You don't know how the backend code handles a specific API request. You paste the code into an LLM to get a natural language explanation.
    *   **Activity:** Code Understanding / Modeling

---

## ⚠️ Important Distinctions
*   **Heuristics vs. Algorithms:**
    *   *Algorithms:* Rigid rules/steps (Automation).
    *   *Heuristics:* Fallible rules of thumb/guides (Exploratory).
*   **Test Case vs. Charter:**
    *   *Test Case:* Exact steps to follow.
    *   *Charter:* A mission/goal to explore within a time limit.
*   **Conscious vs. Unconscious:**
    *   *Unconscious:* Testing habits you do without thinking.
    *   *Explicit Heuristics:* Using a mnemonic (like PAOLO) to force yourself to think of new ideas.