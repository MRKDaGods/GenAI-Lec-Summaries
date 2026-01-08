You are absolutely right again. Lecture 9 is technically dense, and for a "Complete Question" exam, you need the **exact definitions of the metrics** (BLEU vs. ROUGE vs. BERTScore) and the **specific distance calculations** (Cosine vs. Euclidean).

Here is the **Improved, Detailed Lecture 9 Summary**.

***

# 📘 Lecture 9: RAG vs. Fine-Tuning (Deep Dive)

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### RAG (Retrieval-Augmented Generation) Mechanics
*   The phase of RAG where documents are pre-processed and stored $\to$ **Indexing**
*   Splitting long documents into smaller, manageable sections (200-1,000 tokens) $\to$ **Chunking**
*   Repeating a small portion (10-20%) of text between chunks to preserve context $\to$ **Overlap**
*   A mathematical representation of text meaning (list of numbers) $\to$ **Embedding (Vector)**
*   A database optimized for storing and searching high-dimensional vectors $\to$ **Vector Database**
*   Tools like FAISS, Pinecone, and Weaviate are examples of $\to$ **Vector Stores**
*   Search method that finds matches based on *meaning/semantics* rather than exact keywords $\to$ **Similarity Search**
*   The limitation on how much text an LLM can process in one prompt $\to$ **Context Window**
*   Adding too much data to a prompt, causing the model to lose focus $\to$ **Dilution (or Noise)**

### RAG Similarity Metrics (Crucial for Exam)
*   Metric measuring the **angle/direction** between two vectors (-1 to 1) $\to$ **Cosine Similarity**
*   Metric measuring the **actual distance** between points in space (like a map) $\to$ **Euclidean Distance**
*   Metric measuring how much two vectors "line up" (Faster, used in Transformers) $\to$ **Dot Product**

### Fine-Tuning Mechanics
*   Training a foundational model further with a specific dataset to bias its behavior $\to$ **Fine-Tuning**
*   A dataset where columns include instructions, inputs, and outputs (e.g., Alpaca) $\to$ **Structured Dataset**
*   Data generated artificially by another LLM to expand small datasets $\to$ **Synthetic Data**
*   Open-source tool that streamlines fine-tuning (handles tokenization/prompting) $\to$ **Axolotl**
*   The risk of company algorithms or secrets being exposed to a public model $\to$ **IP Exposure**
*   Hosting method required for high security/privacy (keeping data on-premise) $\to$ **Private LLM**

### Fine-Tuning Evaluation Metrics
*   Metric measuring how far predicted probabilities are from the correct answer (Lower is better) $\to$ **Cross-Entropy Loss**
*   Metric measuring **Precision** (How many words in output are also in the reference?) $\to$ **BLEU Score**
*   Metric measuring **Recall** (How many words from reference appear in the output?) $\to$ **ROUGE Score**
*   Metric comparing the **Meaning/Semantics** using embeddings (not just exact words) $\to$ **BERTScore**

---

## 📋 Classifications & Comparisons

### 1. The RAG Workflow (3 Phases)
1.  **Indexing:** Preparation $\to$ Chunking $\to$ Embedding $\to$ Storing.
2.  **Retrieval:** Query $\to$ Vector Search $\to$ Retrieve Top Chunks.
3.  **Generation:** Query + Retrieved Chunks $\to$ Augmented Prompt $\to$ LLM Response.

### 2. Fine-Tuning Process Steps
1.  **Goal Setting:** Define behavior (e.g., "Code Assistant").
2.  **Data Preparation:** Clean, format (JSONL), and Tokenize.
3.  **Tuning:** Run training loops (Forward pass $\to$ Loss Calc $\to$ Update Weights).
4.  **Evaluation:** Use metrics (BLEU/ROUGE) and Human Validation.

### 3. Comparison: RAG vs. Fine-Tuning
| Feature | RAG | Fine-Tuning |
| :--- | :--- | :--- |
| **Primary Goal** | Accuracy, Fact Retrieval, Reduced Hallucinations | Behavior, Tone, Style, Format |
| **Data Type** | Dynamic (Daily updates) | Static (Requires retraining) |
| **Knowledge Source** | External Database (Open Book) | Internal Weights (Memorized) |
| **Cost** | Lower (Initial), Higher (API/Token costs) | Higher (Hardware/GPU), Lower (Inference) |
| **Control** | Low (Opaque vector stores) | High (Full control over model) |
| **Learning Curve** | Low (Easier to implement) | High (Complex data prep/training) |

---

## 🧠 Case Study Triggers (Decision Tree)
*If the exam gives you a scenario $\to$ Identify the Solution*

*   **Scenario:** You need the LLM to know about **daily stock prices** or **breaking news**.
    *   *Analysis:* Data changes frequently.
    *   *Decision:* **RAG** (Retrieval-Augmented Generation).
*   **Scenario:** You want the AI to write code using your company's **specific coding style** and naming conventions.
    *   *Analysis:* Requires behavioral bias/style adaptation.
    *   *Decision:* **Fine-Tuning**.
*   **Scenario:** You have a massive database of **technical manuals** and want users to query them.
    *   *Analysis:* Needs accuracy and specific fact retrieval.
    *   *Decision:* **RAG**.
*   **Scenario:** You are a **healthcare provider** with strict data privacy laws. Data cannot leave your building.
    *   *Analysis:* High Privacy/Control requirement.
    *   *Decision:* **Fine-Tuning (On-Premise/Private Model)**.
*   **Scenario:** The model understands the content but sounds too robotic. You want it to sound **friendlier**.
    *   *Analysis:* Tone adjustment.
    *   *Decision:* **Fine-Tuning**.
*   **Scenario:** You have **limited budget** and need a prototype running by the end of the week.
    *   *Analysis:* Speed and Cost.
    *   *Decision:* **RAG** (Faster to set up).
*   **Scenario:** The model answers correctly but hallucinates facts when it doesn't know the answer.
    *   *Analysis:* Needs grounding in facts.
    *   *Decision:* **RAG** (Reduces hallucinations).

---

## ⚠️ Important Distinctions
*   **Vector Store vs. Vector Database:** A Store is a concept; a Database (like Weaviate) is the full system managing it.
*   **Precision vs. Recall (Metrics):**
    *   *BLEU (Precision):* Did the model say *only* the right things?
    *   *ROUGE (Recall):* Did the model say *all* the right things?
*   **Dynamic vs. Static:** RAG is dynamic (update the DB, update the knowledge). Fine-tuning is static (model is frozen after training).
