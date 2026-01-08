
# 📘 Lecture 7: AI for Data Creation & Exploratory Testing

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### Rapid Data Creation
*   LLMs are described as powerful, probabilistic \_\_\_\_\_\_\_\_. $\to$ **Text Generators**
*   A specific file format used to define structure and rules for XML data $\to$ **XSD (XML Schema Definition)**
*   A standard specification used to define structure for REST APIs (JSON data) $\to$ **OpenAPI v3**
*   Using existing documentation (like XSD/SQL schema) in a prompt to guide the LLM $\to$ **Context / Standard-Based Prompting**
*   To link data correctly across multiple SQL tables, the LLM needs both INSERT and \_\_\_\_\_ statements. $\to$ **CREATE**
*   The main risk when using real customer data for testing prompts $\to$ **Data Privacy / Data Leakage**
*   Strategy where you save effective prompts in external files for the team to use $\to$ **Prompt Reuse**

### Exploratory Testing (ET)
*   Testing approach combining simultaneous learning, test design, and execution $\to$ **Exploratory Testing**
*   ET is NOT random testing; it requires \_\_\_\_\_\_. $\to$ **Critical Thinking / Documentation**
*   Visually organizing ideas and test conditions to uncover areas to explore $\to$ **Mind Mapping**
*   Focusing testing effort on areas with the highest potential impact or likelihood of failure $\to$ **Risk-Based Exploratory Testing**
*   Executing focused, time-boxed testing sessions guided by a mission $\to$ **Session-Based Testing**
*   The specific mission statement used in Session-Based Testing $\to$ **Charter**
*   Using experience and intuition to predict where defects are likely to occur $\to$ **Error Guessing**
*   Testing values at the limits of functionality (e.g., age 17/18/65/66) $\to$ **Boundary & Edge Case Exploration**
*   Quick, lightweight experiments to spot bottlenecks (e.g., uploading large files) $\to$ **Exploratory Performance Checks**

---

## 📋 Classifications & Standards
*   **Standards for Data Context:** OpenAPI v3, XSD, JSON Schema, GraphQL Schema, CSV Header.
*   **7 Approaches to Exploratory Testing:**
    1.  Mind Mapping
    2.  Risk-Based
    3.  Session-Based (Charters)
    4.  Error Guessing
    5.  Boundary/Edge Case
    6.  Performance Checks
*   **When to use Exploratory Testing:** Unclear requirements, Time pressure, High-risk areas, Tricky bugs, Unstable UI.

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You need to generate valid XML test data. You paste the schema definition into the prompt to ensure the output is valid.
    *   **Standard Used:** XSD (XML Schema Definition)
*   **Scenario:** You need to generate SQL data for `Orders` and `Customers`. You provide the `CREATE TABLE` scripts to the LLM to ensure Foreign Keys match.
    *   **Goal:** Data Consistency / Referential Integrity
*   **Scenario:** You have a new feature with no written requirements and need to find bugs quickly.
    *   **Decision:** Exploratory Testing
*   **Scenario:** You are testing a "Transfer Money" feature because a failure there causes financial loss (High Impact).
    *   **Approach:** Risk-Based Exploratory Testing
*   **Scenario:** You allocate exactly 45 minutes to test the "Sign Up" flow and note down findings.
    *   **Approach:** Session-Based Testing
*   **Scenario:** You know from past experience that this developer often forgets to handle empty fields, so you specifically test empty inputs.
    *   **Approach:** Error Guessing
*   **Scenario:** You sketch a visual diagram of the shopping cart flow to decide what to test.
    *   **Technique:** Mind Mapping
*   **Scenario:** You upload 100 files quickly to see if the app freezes.
    *   **Technique:** Exploratory Performance Check

---

## ⚠️ Important Distinctions
*   **Exploratory vs. Scripted:** Scripted = Pre-written steps. Exploratory = Simultaneous design & execution.
*   **Charter vs. Test Case:** Charter = A mission/goal (Session-based). Test Case = Specific steps (Scripted).
*   **Error Guessing vs. Risk-Based:**
    *   *Error Guessing:* Based on **Intuition/Experience** ("I bet this breaks here").
    *   *Risk-Based:* Based on **Impact/Severity** ("If this breaks, we lose money").