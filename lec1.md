Based on the lecture slides you provided, here is the **Lecture 1 Summary** formatted specifically for your "Complete Questions" (Short Answer) exam.

I have stripped away the fluff and focused only on the **Key Terms** and **Decision Triggers** your professor looks for.

***

# 📘 Lecture 1: Software Testing Concepts & Basics

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

*   Process of evaluating and verifying software behaves as expected $\to$ **Software Testing**
*   Testing executed manually without tools $\to$ **Manual Testing**
*   Testing executed using scripts or tools $\to$ **Automated Testing**
*   Testing functionality *without* knowing internal code $\to$ **Black Box Testing**
*   Testing with *full knowledge* of internal code/logic $\to$ **White Box Testing**
*   Testing with *partial knowledge* of internals $\to$ **Gray Box Testing**
*   Smallest scope testing (functions/methods) $\to$ **Unit Testing**
*   Checking how modules/components work together $\to$ **Integration Testing**
*   Validating complete system against requirements $\to$ **System Testing**
*   Ensuring system meets business needs $\to$ **Acceptance Testing (UAT)**
*   Requirements defining *what* the system should do (behavior) $\to$ **Functional Requirements**
*   Requirements defining quality attributes (speed, security) $\to$ **Non-Functional Requirements**
*   Linear, sequential SDLC model (no overlap) $\to$ **Waterfall Model**
*   Model developing system through repeated cycles/increments $\to$ **Iterative Model**
*   Risk-driven, incremental model with prototyping $\to$ **Spiral Model**
*   Checking documents/design ("Are we building the product right?") $\to$ **Verification**
*   Testing actual product ("Are we building the right product?") $\to$ **Validation**
*   Process-oriented approach (Preventive) $\to$ **Quality Assurance (QA)**
*   Product-oriented approach (Corrective) $\to$ **Quality Control (QC)**
*   Model where testing is planned in parallel with development $\to$ **V-Model**
*   Time-boxed iterations in Agile (1-4 weeks) $\to$ **Sprints**
*   Person representing the customer/business in Scrum $\to$ **Product Owner**
*   Rough, early version of software for visualization $\to$ **Prototype**
*   Moving testing earlier in the project timeline $\to$ **Shift-Left Testing**
*   Custom SDLC model adapting multiple existing models $\to$ **Derived Model**

---

## 📋 Classifications & Lists
*   **Types of Testing (Execution Perspective):** Manual, Automated
*   **Types of Testing (Knowledge Perspective):** Black Box, White Box, Gray Box
*   **Levels of Testing (in order):** Unit, Integration, System, Acceptance
*   **SDLC Phases:** Investigation, Analysis, Design, Coding, Testing, Release
*   **Design Phase Levels:** High-Level Design (HLD), Low-Level Design (LLD)
*   **Agile Roles:** Product Owner, Scrum Master, Development Team
*   **Scrum Artifacts:** Product Backlog, Sprint Backlog, Increment
*   **Verification Methods:** Inspection, Review, Walkthrough

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You need to run repetitive regression tests quickly.
    *   **Decision:** Automated Testing
*   **Scenario:** You want to test the UI logic but also check database values (Mix).
    *   **Decision:** Gray Box Testing
*   **Scenario:** Project has fixed requirements, short duration, stable technology.
    *   **Decision:** Waterfall Model
*   **Scenario:** Project is large, high-risk, and requirements are unclear.
    *   **Decision:** Spiral Model
*   **Scenario:** Customer wants to see working features early and give feedback often.
    *   **Decision:** Iterative Model (or Agile)
*   **Scenario:** You are reviewing the SRS document before coding starts.
    *   **Decision:** Verification (Static Testing)
*   **Scenario:** You are executing the code to find bugs.
    *   **Decision:** Validation (Dynamic Testing)
*   **Scenario:** You want to prevent defects by improving the process.
    *   **Decision:** Quality Assurance (QA)
*   **Scenario:** You want to identify and fix defects in the final product.
    *   **Decision:** Quality Control (QC)
*   **Scenario:** You need strict documentation (Waterfall) but risk analysis (Spiral).
    *   **Decision:** Derived Model
*   **Scenario:** You start writing test cases during the Design phase.
    *   **Decision:** Shift-Left Testing

---

## ⚠️ Important Distinctions (Don't Mix These Up!)
*   **Verification** = Static (Documents) | **Validation** = Dynamic (Code execution)
*   **Functional Req** = Behaviors/Features | **Non-Functional Req** = Performance/Security
*   **QA** = Process (Preventive) | **QC** = Product (Corrective)
*   **Waterfall** = Linear | **Iterative** = Cycles | **Spiral** = Risk-Focused