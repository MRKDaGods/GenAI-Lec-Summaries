Here is the **Lecture 6 Summary**.

This lecture introduces conceptual models (Imagination vs. Implementation) and specific heuristics (SFDIPOT). These are **high-probability targets** for your exam.

***

# 📘 Lecture 6: AI-Assisted Test Planning & Models

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

*   Testing done only to check if written requirements are met $\to$ **Confirmatory Testing**
*   In James Lyndsay’s model, the circle representing "What we want" $\to$ **Imagination**
*   In James Lyndsay’s model, the circle representing "What we have" (actual product) $\to$ **Implementation**
*   In the testing model, the area where we "Expected it but didn't get it" $\to$ **Value not delivered**
*   In the testing model, the area where we "Got it but didn't expect it" (Risky) $\to$ **Side Effects / Bugs**
*   An abstract representation that simplifies a system to help understanding $\to$ **Model**
*   "All models are \_\_\_\_\_, but some are useful." (George Box) $\to$ **Wrong**
*   LLM capability to create new content (e.g., creating SQL data) $\to$ **Generative**
*   LLM capability to change format/language (e.g., Code to Text, JSON to SQL) $\to$ **Transformation**
*   LLM capability to add detail to existing material (e.g., Adding code comments) $\to$ **Enhancement**
*   The main driver that should shape test planning and scope $\to$ **Risk**
*   A mental model mnemonic used to inspect a product from different perspectives $\to$ **SFDIPOT**
*   The danger of relying too heavily on LLMs, leading to similar/repetitive tests $\to$ **Test Case Monoculture**

---

## 📋 Classifications & Acronyms

### 1. James Lyndsay’s Model (The Venn Diagram)
*   **Left Circle:** Imagination (Intentions/Expectations).
*   **Right Circle:** Implementation (Actual behavior).
*   **Goal of Testing:** Decrease the **gap** between these two circles.

### 2. LLM Capabilities in Testing
*   **Generative:** Creating test data, risk suggestions, code snippets.
*   **Transformation:** Translating code, formatting data, summarizing notes.
*   **Enhancement:** Code reviews, adding comments, expanding analysis.

### 3. SFDIPOT Mnemonic (Heuristic Test Strategy Model)
*   **S**tructure (What it is made of)
*   **F**unction (What it does)
*   **D**ata (What it processes)
*   **I**nterfaces (How we interact with it)
*   **P**latform (Dependencies)
*   **O**perations (How it is used)
*   **T**ime (Temporal relationship/delays)

### 4. Formal Modeling Techniques
*   **DFD:** Data Flow Diagram.
*   **UML:** Unified Modeling Language (e.g., Component Diagrams).
*   **User Flow:** Visualizing user steps.

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You ask the LLM to convert a list of raw text requirements into a SQL database setup script.
    *   **Capability Used:** Transformation
*   **Scenario:** You paste a complex function into ChatGPT and ask it to explain what the code does in plain English.
    *   **Capability Used:** Enhancement (or Explanation)
*   **Scenario:** You need to test a specific API. Instead of prompting "Test this API," you provide a Data Flow Diagram (DFD) to focus the LLM.
    *   **Technique:** Model-Based Prompting
*   **Scenario:** You are analyzing a product's architecture, file system, and code structure. Which letter of SFDIPOT are you using?
    *   **Answer:** Structure (S)
*   **Scenario:** You are testing how the application behaves when the network is slow or after a session timeout. Which letter of SFDIPOT is this?
    *   **Answer:** Time (T)
*   **Scenario:** You rely 100% on ChatGPT to write all your test cases without human review.
    *   **Risk:** Bias / Missed Edge Cases / Hallucination
*   **Scenario:** You create a prompt that lists specific steps: "1. List risks. 2. Create tests for those risks. 3. Output as Table."
    *   **Technique:** Focused/Structured Prompting

---

## ⚠️ Important Distinctions
*   **Imagination** = What we *think* we want (Requirements).
*   **Implementation** = What we *actually* built (Code/Product).
*   **Probabilistic vs. Reasoning:** LLMs generate ideas based on *probability*, not human-like reasoning.
*   **Formal Models vs. Mental Models:**
    *   *Formal:* Expensive, visual, detailed (e.g., UML, DFD).
    *   *Mental:* Cheaper, cognitive shortcuts (e.g., SFDIPOT).