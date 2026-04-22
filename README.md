![Python](https://img.shields.io/badge/Python-3.10-blue)
![LangChain](https://img.shields.io/badge/LangChain-RAG-green)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-orange)

- # 🧠 AI-Powered Health Assistant using RAG

## 📌 Overview
This project demonstrates a **Retrieval-Augmented Generation (RAG)** system that answers health-related queries using retrieved knowledge instead of relying solely on a language model.

The system combines:
- 🔍 Semantic search (FAISS)
- 🔢 Text embeddings (HuggingFace)
- 🤖 LLM-based response generation (Google Gemini)

---

## 🎯 Motivation

Traditional LLMs often hallucinate or provide unverified answers. This project demonstrates how Retrieval-Augmented Generation (RAG) improves factual accuracy by grounding responses in retrieved documents.

---

## 📌 What This Demonstrates

- Vector databases (FAISS)
- Embedding models
- RAG architecture
- Prompt engineering
- LLM integration (Gemini API)

---

## 🚀 Key Features

- Retrieves relevant documents based on user query
- Uses embeddings for semantic similarity
- Generates grounded responses using retrieved context
- Reduces hallucination in LLM outputs

---

## 🏗️ System Architecture

1. Input Query  
2. Convert query → embeddings  
3. Retrieve top-k relevant documents (FAISS)  
4. Combine context + query  
5. Generate answer using Gemini  

---

## 📊 Example Output

### Query:
> How can I reduce risk of heart disease?

### Retrieved Documents:
- Heart disease is a leading cause of death worldwide. Regular exercise helps reduce risk.  
- High blood pressure can lead to serious complications if untreated.

### Final Answer:
> Regular exercise helps reduce the risk of heart disease.

---

## 🧪 Tech Stack

- Python
- LangChain
- FAISS (Vector Database)
- Sentence Transformers
- Google Gemini API

---

## ⚙️ Installation

```bash
pip install -r requirements.txt
