
# 📄 PDF Retriever with Chroma and Embeddings

This project demonstrates how to build a **PDF Semantic Search System using ChromaDB and Embeddings**, enabling users to retrieve the most relevant chunks of information from a PDF document based on semantic similarity.

---

## 📚 Project Overview

The goal is to implement a **Retrieval-Augmented Generation (RAG)**-like pipeline using **ChromaDB** and various **embedding models** to search content from a PDF file. It involves:

- Loading PDF documents
- Splitting into chunks
- Embedding chunks
- Storing in ChromaDB
- Performing similarity-based search queries

---
## 📁 Files Included

- `PDF Retriever with Chroma and 3 Embeddings.ipynb` — All embedding experiments
- `PDF Retriever with Chroma and best Embeddings.ipynb` — Refined version with best-performing embedding

---
## 🧠 Embeddings Used

In this project, I experimented with **three different embeddings** to observe and compare the quality of retrieval:

1. `all-MiniLM-L6-v2` Embeddings (lightweight, fast)
2. `intfloat/e5-large-v2` Embeddings (high-performance, retrieval-optimized)
3. `GloVe Embeddings` (classical word vector-based)

These experiments are documented in:

👉 **`PDF Retriever with Chroma and 3 Embeddings.ipynb`**

---

## 💎 Refined Code Using Best Embedding

After evaluating results, the **best performance** was observed using:

✅ **`intfloat/e5-large-v2` Embeddings**

The refined and cleaner version of the code using this embedding is provided in:

👉 **`PDF Retriever with Chroma and best Embeddings.ipynb`**

---

## 🔧 Setup Instructions

Before running the notebooks, install the required packages:

```bash
!pip install langchain chromadb openai tiktoken
!pip install -U langchain-community
!pip install -U unstructured
!pip install -U langchain-huggingface
!pip install pypdf
```

---

## 🔍 Example Query

```text
Q: Who are the authors of "Attention is All You Need"?
```

✅ The system will return top 3 most semantically similar chunks from the document.

---


## ✅ Key Learnings

- Transformer-based embeddings (especially E5) outperform traditional ones like GloVe for semantic search
- ChromaDB provides fast and efficient storage and retrieval for embedding vectors
- PDF semantic retrieval enables smarter document search beyond keyword-based approaches

---

## 📈 Future Improvements

- Integrate a conversational chatbot interface using LangChain agents
- Add evaluation metrics to compare embeddings more formally
- Experiment with hybrid retrieval (BM25 + Vector Search)
- Deploy this as a simple Streamlit or Flask app

---

## 🙌 Contribution

Feel free to fork this project and improve the retrieval pipeline or test it with different types of documents and embeddings.
