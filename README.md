# GenAI RAG Chatbot with Conversational Memory

A **Retrieval-Augmented Generation (RAG) chatbot** built using **LangChain, ChromaDB, Hugging Face Embeddings, and Gemini Flash**. The system retrieves relevant document context, maintains conversation history, and generates structured responses.

## 🚀 Key Features

* 📄 **Document ingestion:** PDF and WebBase loaders
* 🔍 **Vector Database:** ChromaDB
* 🧠 **Embeddings:** Hugging Face Embeddings
* 🤖 **LLM:** Gemini Flash (`ChatGoogleGenerativeAI`)
* 📌 **Structured Output:** `with_structured_output()`
* 💬 **Conversational RAG:** Chat-history-aware retriever
* 🧾 **History Management:** Custom `get_session_history()` function
* 🔗 **Document Chain:** `create_stuff_documents_chain()`
* 📊 **Retrieval Evaluation:** Recall@2, Precision@2, MRR
* 🎯 **Generation Evaluation:** Tested generated responses for quality
* 🧪 **Evaluation Result:** Recall@2 = **1.0**, Precision@2 = **1.0**, MRR = **1.0**

## 🏗️ Architecture

```text
PDF / Web Documents
        ↓
Document Loaders
        ↓
Text Splitting
        ↓
Hugging Face Embeddings
        ↓
ChromaDB Vector Store
        ↓
Chat-History-Aware Retriever
        ↓
Relevant Documents
        ↓
Create Stuff Documents Chain
        ↓
Gemini Flash
        ↓
Structured Response
        ↓
Conversation History
```

## 📊 Evaluation

| Metric                |    Score |
| --------------------- | -------: |
| Recall@2              |  **1.0** |
| Precision@2           |  **1.0** |
| MRR                   |  **1.0** |
| Generation Evaluation | ✅ Passed |

## 🛠️ Tech Stack

**Python · LangChain · Gemini Flash · ChromaDB · Hugging Face · RAG · PyPDF · WebBaseLoader**

## 🎯 Outcome

The chatbot successfully **retrieves relevant context, maintains conversation history, remembers previous context, and generates evaluated responses**.

ython app.py
```
