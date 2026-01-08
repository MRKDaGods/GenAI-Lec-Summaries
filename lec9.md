Here is the **Lecture 9 Summary**.

This lecture is the technical deep-dive into **RAG vs. Fine-Tuning**. This is the most complex lecture, so expect questions asking you to **choose between the two approaches** based on a scenario (Cost, Speed, Control, or Data Frequency).

***

# 📘 Lecture 9: RAG vs. Fine-Tuning

## 🎯 Concept Match (Reverse Dictionary)
*Read the description $\to$ Write the Term*

### RAG Concepts (Retrieval-Augmented Generation)
*   The maximum number of tokens an LLM can process in one go $\to$ **Context Window**
*   The problem where too much context dilutes the quality of the answer $\to$ **Noise (or Dilution)**
*   The phase of RAG where raw documents are transformed into a searchable format $\to$ **Indexing**
*   Splitting long text into smaller, manageable sections (200-1000 tokens) $\to$ **Chunking**
*   Repeating a small portion of text between chunks (10-20%) to preserve context $\to$ **Overlap**
*   A mathematical representation of text meaning as a list of numbers $\to$ **Embedding (Vector)**
*   A specialized database optimized for storing and searching vectors $\to$ **Vector Database**
*   Search method that finds matches based on *meaning* rather than keywords $\to$ **Semantic Similarity Search**
*   Metric measuring similarity based on the **direction/angle** of vectors (-1 to 1) $\to$ **Cosine Similarity**
*   Metric measuring similarity based on the **actual distance** in space $\to$ **Euclidean Distance**
*   Metric measuring how much vectors "line up" (faster, used in Transformers) $\to$ **Dot Product**

### Fine-Tuning Concepts
*   Training an *already-trained* model with additional datasets to bias its behavior $\to$ **Fine-Tuning**
*   Data generated artificially to expand small datasets or create edge cases $\to$ **Synthetic Data**
*   Tool used to streamline fine-tuning (e.g., built-in tokenization support) $\to$ **Axolotl**
*   Risk of sending proprietary code to an external public LLM $\to$ **IP Exposure (Intellectual Property)**
*   Metric measuring how far predicted probabilities are from the correct answer (Lower is better) $\to$ **Cross-Entropy Loss**
*   Metric measuring **precision** (how many words in output are in correct answer) $\to$ **BLEU Score**
*   Metric measuring **recall** (how many words from correct answer appear in output) $\to$ **ROUGE Score**
*   Metric comparing the **meaning** of the answer using embeddings $\to$ **BERTScore**

---

## 📋 Classifications & Processes
*   **3 Phases of RAG:** Indexing $\to$ Retrieval $\to$ Generation.
*   **Steps in Indexing:** Document Prep $\to$ Chunking $\to$ Embedding $\to$ Vector Store.
*   **Similarity Metrics:** Cosine Similarity, Dot Product, Euclidean Distance.
*   **Fine-Tuning Evaluation Metrics:** Cross-Entropy Loss, BLEU, ROUGE, BERTScore.
*   **Fine-Tuning Infrastructure:** Local Hardware (Buy GPUs) vs. Cloud Computing (Rent GPUs).

---

## 🧠 Case Study Triggers (Decision Making)
*If the exam gives you a scenario $\to$ Identify the Solution/Decision*

*   **Scenario:** You need the AI to know about facts that change **daily** (e.g., stock prices, daily news).
    *   **Decision:** RAG (Dynamic knowledge update)
*   **Scenario:** You need the AI to speak in a specific **tone** (e.g., "Pirate mode") or follow a strict code style.
    *   **Decision:** Fine-Tuning (Behavior/Style modification)
*   **Scenario:** You have a **limited budget** and need a solution ready in 2 days.
    *   **Decision:** RAG (Cheaper, Faster setup)
*   **Scenario:** You are a bank with strict **privacy** laws; data cannot leave your servers, and you need full control over the model's weights.
    *   **Decision:** Fine-Tuning (On-premise/Private)
*   **Scenario:** A user queries "login failure," but the documentation uses the term "authentication error." Keyword search fails.
    *   **Solution:** Semantic Similarity Search (Embeddings)
*   **Scenario:** The LLM cuts off the answer because the input document was too long.
    *   **Problem:** Exceeded Context Window (Solution: Chunking)
*   **Scenario:** You fine-tuned a model, but now it answers *too* creatively and ignores facts.
    *   **Diagnosis:** Poor Alignment (Needs better Goal Setting/Data)

---

## ⚠️ Important Distinctions (RAG vs. Fine-Tuning)

| Feature | RAG | Fine-Tuning |
| :--- | :--- | :--- |
| **Primary Goal** | **Accuracy/Knowledge** (Fact Retrieval) | **Behavior/Style** (Tone, Format) |
| **Data Freshness** | **Dynamic** (Update DB = Instant update) | **Static** (Requires retraining) |
| **Cost** | **Lower** (pay per token/query) | **Higher** (hardware/training costs) |
| **Knowledge Source**| External Database (Open book) | Internal Parameters (Memorized) |
| **Hallucinations** | **Low** (Grounded in retrieved data) | **Medium** (Can still hallucinate if data bad) |