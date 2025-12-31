# Applied LLM & ML Systems — Case Studies (Client / Confidential)

This repository documents the architecture, system design, and engineering decisions behind
multiple real-world ML and LLM-based systems built for clients.

> ⚠️ Source code, datasets, and client identifiers are private due to confidentiality.
> This repository intentionally contains no production code.

---

## Case Study 1: LLM-Based Retrieval & Question Answering System

### Problem
The client required a reliable system to answer domain-specific questions over internal documents,
with minimal hallucinations and consistent response quality.

### Solution
- Retrieval-Augmented Generation (RAG) architecture
- Embedding-based semantic search using a vector database
- LLM-based response generation grounded in retrieved context
- Output validation and fallback logic

### Architecture
Ingestion → Cleaning → Chunking → Embeddings → Indexing  
Query → Retrieval → Context Assembly → LLM Inference → Validation → Response

### Quality & Reliability
- Prompt versioning and regression testing
- Evaluation of accuracy, relevance, and failure modes
- Guardrails to handle missing or weak retrieval results

---

## Case Study 2: Policy Navigation & Recommendation System

### Problem
Small businesses needed clear, actionable guidance on relevant policies based on
location, business type, and operational constraints.

### Solution
- Semantic retrieval over local, state, and federal policy documents
- LLM-based interpretation and summarization of policy content
- Rule-aware prompts to produce actionable, non-ambiguous outputs

### Architecture
Document ingestion → Embeddings → Policy retrieval  
User inputs → Context filtering → LLM reasoning → Validated recommendations

### Quality & Reliability
- Output validation for clarity and relevance
- Handling ambiguous or overlapping policy scenarios
- Manual review loops during early iterations

---

## Tech Stack (Shared)
- Python
- Large Language Model APIs
- Vector Databases (Embeddings & Similarity Search)
- API-based ML services (FastAPI-style)
- Docker

---

## Interview Notes
I am happy to discuss:
- Architecture trade-offs
- Retrieval strategies
- Evaluation methods
- Reliability challenges
- What went wrong and how it was fixed

However, source code and client details cannot be shared publicly.
