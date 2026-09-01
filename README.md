# GenAI RAG & Hybrid RAG Projects

A collection of **production-oriented Retrieval-Augmented Generation (RAG) projects** built with LangChain, Gemini, vector databases, Hugging Face embeddings, retrieval evaluation, reranking, and conversational memory.

## 🚀 Projects

### 1. Conversational RAG Chatbot

RAG chatbot with **ChromaDB and conversational memory** for context-aware question answering.

**Tech Stack / Features**

* PDF + WebBase document loaders
* Hugging Face Embeddings
* ChromaDB Vector Store
* Chat-history-aware Retriever
* `create_stuff_documents_chain()`
* `with_structured_output()`
* Custom `get_session_history()`
* Gemini Flash (`ChatGoogleGenerativeAI`)
* Retrieval + Generation Evaluation

**Retrieval Evaluation**

| Metric      |   Score |
| ----------- | ------: |
| Recall@2    | **1.0** |
| Precision@2 | **1.0** |
| MRR         | **1.0** |

---

### 2. Hybrid RAG with Reranking

Hybrid RAG system combining **semantic and keyword search**, followed by **Cross-Encoder reranking** to improve retrieval relevance.

**Tech Stack / Features**

* Pinecone Vector Database
* Hugging Face Embeddings
* BM25 Retriever
* Hybrid Search
* Cross-Encoder Reranker
* `with_structured_output()`
* `Refine` Chain
* Gemini Flash (`ChatGoogleGenerativeAI`)

## 🏗️ Architectures

### Conversational RAG

```text
Documents → Embeddings → ChromaDB
                         ↓
              History-Aware Retriever
                         ↓
                  Document Chain
                         ↓
                    Gemini Flash
                         ↓
              Structured Response
```

### Hybrid RAG

```text
Query
  ↓
 ┌───────────────┐
 │ Semantic Search│ → Pinecone
 │ Keyword Search │ → BM25
 └───────────────┘
          ↓
    Hybrid Retrieval
          ↓
  Cross-Encoder Reranker
          ↓
      Refine Chain
          ↓
      Gemini Flash
          ↓
 Structured Response
```

## 🛠️ Tech Stack

**Python · LangChain · Gemini Flash · ChromaDB · Pinecone · Hugging Face · BM25 · Cross-Encoder · RAG · Hybrid Search · Reranking**

## 🎯 Key Outcomes

* Built both **standard RAG and Hybrid RAG** pipelines.
* Implemented **conversational memory and context-aware retrieval**.
* Improved retrieval using **BM25 + semantic search + Cross-Encoder reranking**.
* Evaluated retrieval using **Recall@K, Precision@K and MRR**.
* Implemented structured generation and generation evaluation.
* Implemented **structured generation and generation evaluation**.
