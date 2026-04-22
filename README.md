# AI-Powered Health Assistant using Retrieval-Augmented Generation (RAG)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![RAG](https://img.shields.io/badge/Technique-RAG-green)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-purple)
![Gemini](https://img.shields.io/badge/LLM-Gemini-yellow)
![NLP](https://img.shields.io/badge/NLP-LLM-orange)
![Framework](https://img.shields.io/badge/HuggingFace-Transformers-red)
![Project](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Overview

This project implements a **Retrieval-Augmented Generation (RAG)** system that answers health-related queries by combining **semantic retrieval** with **LLM-based generation**.

Instead of relying solely on a language model, the system first retrieves relevant documents and then generates responses grounded in that context — improving reliability and reducing hallucination.

---

## 🎯 Motivation

Modern AI systems (search engines, assistants, recommendation systems) rely heavily on:

- 🔍 Retrieval  
- 📊 Ranking  
- 🤖 Context-aware generation  

This project explores these core ideas in a simplified, beginner-friendly setup while focusing on **understanding how retrieval affects final outputs**.

---

## System Architecture

1. User inputs a query  
2. Query is converted into embeddings  
3. FAISS performs similarity search  
4. Top-k relevant documents are retrieved  
5. Context is combined with query  
6. Gemini generates the final grounded answer  

---

## ⚙️ System Components

### 🔹 Embedding Layer
- Model: `sentence-transformers/all-MiniLM-L6-v2`  
- Converts text into dense vector representations for semantic similarity  

### 🔹 Vector Database
- FAISS enables efficient similarity search over embeddings  

### 🔹 Retrieval Mechanism
- Uses similarity-based ranking  
- Returns top-k most relevant documents  

### 🔹 Generation Layer
- Google Gemini generates answers using retrieved context  
- Prompt ensures responses are grounded in retrieved knowledge  

---

## 📊 Example

### Query:
> How can I reduce risk of heart disease?

### Retrieved Documents:
- Heart disease is a leading cause of death worldwide. Regular exercise helps reduce risk.  
- High blood pressure can lead to serious complications if untreated.  

### Final Answer:
> Regular exercise helps reduce risk.

![Rag Reply](image/rag_reply.png)

---

## 🔬 Experiments & Analysis

This project goes beyond basic implementation by exploring how retrieval behaves:

### 🔍 1. Query Quality Impact

- Specific queries → highly relevant results  
- Vague queries → less precise retrieval  

**Insight:** Retrieval quality depends heavily on how queries are formulated.

![Good Bad Query](image/good_bad_query.png)

---

### 📊 2. Ranking Behavior

- Documents are ranked based on similarity scores  
- Top-ranked document is most relevant  

**Insight:** Ranking directly affects the quality of generated answers.

![Retrieval Relevant Document](image/retrieval_relevant_document.png)
------
![Retrieval Score](image/retrieval_score.png)

---

### ⚙️ 3. Top-K Tradeoff

- Smaller k → more precise results  
- Larger k → more context but potential noise  

**Insight:** Selecting the right k is critical for balancing precision and completeness.

![Top K Retrieval](image/top_k_retrieval.png)

---

## Key Learnings

Through this project, I explored:

- How semantic search retrieves relevant information  
- The importance of ranking in search systems  
- How query formulation impacts retrieval quality  
- Trade-offs in selecting top-k documents  
- How RAG reduces hallucination in LLM outputs  

These concepts are fundamental to modern AI systems such as search engines and intelligent assistants.

---

## 🚀 Key Features

- Semantic document retrieval using FAISS  
- Dense embeddings using HuggingFace models  
- Context-aware response generation using Gemini  
- Retrieval analysis with similarity scores  
- Query comparison experiments  
- Top-k retrieval experimentation  

---

## Tech Stack

- Python  
- LangChain  
- FAISS (Vector Database)  
- Sentence Transformers  
- Google Gemini API  

---

## ⚙️ Installation

pip install -r requirements.txt---

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

This project demonstrates a simple but effective RAG pipeline while emphasizing retrieval behavior, ranking, and system design considerations.

It highlights how modern AI systems depend not only on models, but on how information is retrieved and structured before generation.

## 👤 Author

Muhammad Ali Waris Khan
