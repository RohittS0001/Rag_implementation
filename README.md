# RAG Implementation from Scratch

A beginner-friendly implementation of **Retrieval-Augmented Generation (RAG)** using pure Python. This project demonstrates the core concepts behind RAG without relying on frameworks such as LangChain or LlamaIndex.

## 📌 Project Overview

This project implements the basic RAG pipeline:

1. User enters a query.
2. Documents are stored in a small corpus.
3. Cosine Similarity is used to retrieve the most relevant document.
4. The retrieved document is passed to a local **Llama 2** model through **Ollama**.
5. The model generates a response based only on the retrieved context.

The goal is to understand how a RAG system works internally before using production-grade tools.

---

# Project Structure

```
RAG-Implementation/
│
├── rag.ipynb           # Complete notebook implementation
├── requirements.txt    # Python dependencies
├── README.md
```

---

# Features

* Manual implementation of Cosine Similarity
* Tokenization using Python
* Word Frequency (Counter)
* Document Retrieval
* Retrieval-Augmented Generation (RAG)
* Local LLM inference with Ollama
* Beginner-friendly implementation

---

# Technologies Used

* Python 3.x
* Jupyter Notebook
* Requests
* Math
* Collections (Counter)
* Ollama
* Llama 2

---

# How It Works

### Step 1 — Create a Document Corpus

A small collection of text documents is stored in memory.

```
Corpus
│
├── Document 1
├── Document 2
├── Document 3
└── ...
```

---

### Step 2 — User Query

The user asks a question.

Example:

```
"What is the meaning of life?"
```

---

### Step 3 — Tokenization

Both the query and documents are converted into lowercase tokens.

Example:

```
"What is the meaning of life?"

↓

["what","is","the","meaning","of","life"]
```

---

### Step 4 — Cosine Similarity

The project calculates similarity between the user query and every document using Cosine Similarity.

Formula:

```
Similarity = Dot Product / (|Query| × |Document|)
```

The document with the highest similarity score is selected.

---

### Step 5 — Retrieval

The most relevant document is retrieved from the corpus.

```
User Query
      │
      ▼
Cosine Similarity
      │
      ▼
Best Matching Document
```

---

### Step 6 — Generation

The retrieved document is sent to a locally running **Llama 2** model through **Ollama**.

The LLM generates an answer using the retrieved context.

```
User Query
      │
      ▼
Retrieved Document
      │
      ▼
Llama 2 (Ollama)
      │
      ▼
Generated Answer
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/RAG-Implementation.git
```

Move into the project directory

```bash
cd RAG-Implementation
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# Install Ollama

Download Ollama from:

https://ollama.com

Pull the Llama 2 model

```bash
ollama pull llama2
```

Run the model

```bash
ollama run llama2
```

---

# Run the Notebook

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
rag.ipynb
```

Run all cells.

---

# Future Improvements

* TF-IDF Retrieval
* Sentence Transformers Embeddings
* Vector Databases (FAISS / ChromaDB / Qdrant)
* Semantic Search
* Chunking
* Metadata Filtering
* Hybrid Search (BM25 + Dense Retrieval)
* Streaming Responses
* Production-ready API using FastAPI
* LangChain Integration
* Evaluation Metrics

---

# Learning Objectives

This project helps understand:

* Tokenization
* Bag of Words
* Cosine Similarity
* Information Retrieval
* Context Retrieval
* Retrieval-Augmented Generation (RAG)
* Local Large Language Models
* Prompt Engineering
* End-to-End RAG Workflow

---

# Disclaimer

This project is built for educational purposes to demonstrate the fundamentals of Retrieval-Augmented Generation. It uses a small in-memory corpus and simple word-frequency retrieval instead of production-grade embedding models and vector databases.
