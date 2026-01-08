Here is the **Lecture 4 Summary**.

This lecture focuses heavily on **Frameworks** and **Decision Making** (When to automate vs. when not to). Expect the "Case Study" questions to come from the "Frameworks" section (e.g., "Which framework uses Excel files?").

***

# 📘 Lecture 4: Automated Testing & Frameworks

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

*   Testing method using tools/scripts without human intervention $\to$ **Automated Testing**
*   Testing requiring human insight, intuition, and physical interaction $\to$ **Manual Testing**
*   Development practice enabled by automation where code is merged frequently $\to$ **Continuous Integration (CI)**
*   Tests that run randomly pass/fail without code changes (instability) $\to$ **Flaky Tests**
*   Framework where scripts are recorded sequentially (Record & Playback) $\to$ **Linear Framework**
*   Framework separating application into logical units (e.g., Page Object Model) $\to$ **Modular Framework**
*   Framework grouping common tasks by action type (e.g., BrowserActions) $\to$ **Library Architecture**
*   Framework separating Test Logic from Test Data (using Excel/CSV) $\to$ **Data-Driven Framework**
*   Framework using human-readable words (Action Abstraction) for non-technical users $\to$ **Keyword-Driven Framework**
*   Framework using Gherkin syntax (Given-When-Then) to bridge business and dev $\to$ **BDD (Behavior Driven Development)**
*   Combination of two or more frameworks (e.g., Modular + Data-Driven) $\to$ **Hybrid Framework**
*   Metric calculated as `(Manual Cost - Auto Cost) / Auto Cost` $\to$ **ROI (Return on Investment)**
*   The role responsible for building the test framework (not just scripting) $\to$ **SDET (Software Development Engineer in Test)**
*   Feature where AI fixes broken locators automatically $\to$ **Self-Healing Tests**

---

## 📋 Classifications & Lists

*   **When to Automate:** Regression, Smoke/Sanity, Performance/Load, Data-Driven, Stable Features, High-Risk areas.
*   **When NOT to Automate:** Exploratory, Ad-Hoc, Usability (UX), One-time tests, Unstable environments, Physical input required.
*   **Automation Framework Types:** Linear, Modular, Library, Data-Driven, Keyword-Driven, BDD, Hybrid.
*   **Key Automation Roles:**
    *   *Developers:* Unit/Integration tests.
    *   *SDET:* Builds the framework.
    *   *DevOps:* Integrates into CI/CD pipeline.
*   **Key Metrics:** Test Coverage, Defect Density, ROI, Build Stability, Execution Time.
*   **AI in Testing Capabilities:** Test Generation, Self-Healing, Visual Testing, Predictive Analytics.

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You need to test a login page with 100 different username/password combinations.
    *   **Decision:** Data-Driven Framework
*   **Scenario:** You have a short-term project (Proof of Concept) and need quick results with minimal coding.
    *   **Decision:** Linear Framework (Record & Playback)
*   **Scenario:** Your team consists of non-technical Business Analysts who need to design test cases.
    *   **Decision:** Keyword-Driven Framework (or BDD)
*   **Scenario:** You want to ensure the product meets business requirements using "Given-When-Then" syntax.
    *   **Decision:** BDD (Behavior Driven Development)
*   **Scenario:** You are working on a large, long-term enterprise project and need maximum reusability and flexibility.
    *   **Decision:** Hybrid Framework
*   **Scenario:** The UI of the application changes frequently (unstable).
    *   **Decision:** Do Not Automate (Wait for stability)
*   **Scenario:** You need to check if the application "looks good" or is "easy to use."
    *   **Decision:** Manual Testing (Usability)
*   **Scenario:** Tests are failing because the network is slow, not because of a bug.
    *   **Diagnosis:** Flaky Tests
*   **Scenario:** A developer merges code. You need to ensure this new change didn't break existing features.
    *   **Decision:** Regression Testing

---

## ⚠️ Important Distinctions
*   **Linear vs. Modular:** Linear is hard-coded/sequential (bad for maintenance). Modular breaks app into objects/functions (good for maintenance).
*   **Data-Driven vs. Keyword-Driven:** Data-Driven separates *inputs* (Excel). Keyword-Driven separates *actions* (English words).
*   **Verification vs. Validation (Automation Context):** Automation is great for Verification (checking results), bad for Validation (checking user satisfaction).