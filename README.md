# 🧠 AI-Powered Health Assistant using Retrieval-Augmented Generation (RAG)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![LangChain](https://img.shields.io/badge/LangChain-RAG-green)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-orange)

---

## 📌 Overview

This project implements a **Retrieval-Augmented Generation (RAG) system** that answers health-related questions by combining:

- 🔍 Semantic search (FAISS vector database)  
- 🔢 Text embeddings (Sentence Transformers)  
- 🤖 Large Language Model (Google Gemini)  

Instead of relying only on a language model, the system retrieves relevant knowledge first and then generates grounded responses using that context.

---

## 🎯 Problem Statement

Large Language Models often:
- Generate hallucinated or unverified answers  
- Lack grounding in real factual data  
- Struggle with domain-specific accuracy without context  

This project solves these issues using a **retrieval + generation pipeline (RAG)** to improve factual reliability.

---

## 🧠 RAG Architecture

1. User inputs a query  
2. Query is converted into embeddings  
3. FAISS performs similarity search over stored documents  
4. Top-k relevant documents are retrieved  
5. Retrieved context + query are sent to LLM  
6. Google Gemini generates final grounded response  

---

## ⚙️ System Design

### 🔹 Embedding Layer
- Model: `sentence-transformers/all-MiniLM-L6-v2`  
- Converts text into dense vector representations  

### 🔹 Vector Database
- FAISS is used for efficient similarity search  
- Stores document embeddings for fast retrieval  

### 🔹 Retrieval Mechanism
- Cosine similarity-based search  
- Returns most relevant documents for the query  

### 🔹 Generation Layer
- Google Gemini API generates final answer  
- Uses retrieved context in prompt  

---

## 📊 Example

### Query:
> How can I reduce risk of heart disease?

### Retrieved Context:
- Heart disease is a leading cause of death worldwide. Regular exercise helps reduce risk.  
- High blood pressure can lead to serious complications if untreated.

### Final Answer:
> Regular exercise helps reduce the risk of heart disease.

---

## 🚀 Key Features

- Semantic document retrieval using FAISS  
- Dense embeddings using HuggingFace models  
- Context-aware responses using Google Gemini  
- Reduced hallucination through retrieval grounding  
- Modular RAG pipeline design  

---

## 🧪 Tech Stack

- Python  
- LangChain  
- FAISS (Vector Database)  
- Sentence Transformers  
- Google Gemini API  

---

## 📈 Results & Insights

FAISS effectively retrieves semantically relevant documents
Embedding-based search outperforms keyword matching
LLM responses are more accurate and grounded
Demonstrates real-world RAG architecture used in modern AI systems

---

## ⚠️ Limitations

Small dataset (limited knowledge base)
No re-ranking mechanism
No UI or API deployment
Basic prompt engineering

---

## 🚀 Future Improvements

Expand dataset with real medical sources
Add re-ranking models (Cross-Encoders)
Build UI using Streamlit or React
Deploy as API using FastAPI
Add user feedback loop for retrieval optimization

---

## 📌 Conclusion

This project demonstrates a basic but complete RAG pipeline, showing how retrieval improves reliability and factual grounding in LLM-based systems.

It serves as a foundation for building production-level AI search and assistant systems.

## 👤 Author

Muhammad Ali Waris Khan
