Here is the **Lecture 8 Summary**.

This lecture bridges the gap between **Exploratory Testing techniques** and **Technical LLM Architecture** (RAG vs. Fine-tuning). The comparison between RAG and Fine-tuning is the most likely area for case study questions.

***

# 📘 Lecture 8: Advanced Exploratory Testing & Customizing LLMs

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### Exploratory Testing & Reporting
*   Mnemonic used to trigger test ideas for **screen orientation** and rendering $\to$ **PAOLO**
*   Report generated after a session describing what was learned/tested $\to$ **Testing Story**
*   Converting rough testing notes into a structured report using an LLM $\to$ **Summarization**

### LLM Architecture & Limits
*   The process of converting natural language into machine-readable integers $\to$ **Tokenization**
*   The textual limit (capacity) of an LLM's memory in a single conversation $\to$ **Context Window**
*   The specific units LLMs use to calculate cost and processing size $\to$ **Tokens**
*   A larger context window often requires more \_\_\_\_\_\_\_\_ resources. $\to$ **Hardware**

### RAG (Retrieval-Augmented Generation)
*   Technique that enhances the **prompt** by retrieving relevant data from an external source $\to$ **RAG**
*   Database type often used in RAG to store data meanings (vectors) $\to$ **Vector Database**
*   The main goal of RAG is to improve the model's \_\_\_\_\_\_\_\_ without retraining. $\to$ **Performance / Context**
*   RAG helps reduce this common AI problem by providing facts $\to$ **Hallucinations**

### Fine-Tuning
*   Technique that enhances the **model itself** by training it on a specific dataset $\to$ **Fine-Tuning**
*   The goal of Fine-Tuning is to **bias** the model toward a specific \_\_\_\_\_\_\_. $\to$ **Style / Tone / Behavior**
*   Process where a pre-trained model (like GPT-3.5) creates a specialized version (like ChatGPT) $\to$ **Fine-Tuning**

---

## 📋 Classifications & Acronyms

### 1. The PAOLO Mnemonic (Screen/Rendering Tests)
*   **P**ortrait (View orientation)
*   **A**udio (Artifacts/Sounds)
*   **O**bjects (Other items in view)
*   **L**andscape (View orientation)
*   **O**verlay (Pop-ups/Overlays)

### 2. RAG vs. Fine-Tuning Comparison
| Feature | RAG (Retrieval-Augmented Generation) | Fine-Tuning |
| :--- | :--- | :--- |
| **Focus** | Enhances the **Prompt** | Enhances the **Model** |
| **Data Req** | **Low** (works with small data) | **High** (needs large/curated datasets) |
| **Cost** | **Lower** (initial setup) | **Higher** (hardware/training) |
| **Speed** | **Fast** to production | **Slow** (complex process) |
| **Knowledge** | Updates dynamically (real-time) | Static (needs retraining to update) |
| **Best For** | Fact retrieval, reducing hallucinations | Changing tone, style, or code structure |

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Concept*

*   **Scenario:** You need to test how the mobile app looks when rotated sideways. Which mnemonic helps?
    *   **Decision:** PAOLO (Landscape/Portrait)
*   **Scenario:** You have a massive library of PDF manuals. You want the AI to answer questions based *only* on those manuals.
    *   **Decision:** RAG (Retrieval-Augmented Generation)
*   **Scenario:** You want the AI to write code exactly like your senior developers (specific style/syntax). You have 50,000 examples of their code.
    *   **Decision:** Fine-Tuning
*   **Scenario:** You have a small budget and need to set up a custom AI assistant by tomorrow.
    *   **Decision:** RAG
*   **Scenario:** You need the AI to speak in a "Pirate" voice or a very specific "Corporate" tone.
    *   **Decision:** Fine-Tuning
*   **Scenario:** The data changes every day (e.g., daily stock prices). You cannot retrain the model daily.
    *   **Decision:** RAG
*   **Scenario:** You need full control over the model's security and do not want to use an external API (like OpenAI).
    *   **Decision:** Fine-Tuning (on a private/local model)

---

## ⚠️ Important Distinctions
*   **Prompt vs. Model:** RAG changes the *input* (Prompt). Fine-tuning changes the *brain* (Model).
*   **Dynamic vs. Static:** RAG data is dynamic (fetch fresh data). Fine-tuned knowledge is static (locked in at training).
*   **Tokenization:** The LLM does not read words; it reads **Integers** (Tokens).