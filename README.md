 
### Reliable Retrieval-Augmented Generation (RAG) for Aviation Documents

This project implements a **grounded, citation-based Retrieval-Augmented Generation (RAG) system** over aviation PDFs.  
The focus is on **accuracy, safety, and refusal behavior**, rather than free-form generation or UI complexity.

The system is implemented entirely in **Python**, runs **locally**, and is structured as a **Jupyter Notebook** with a minimal **FastAPI** interface.

---

## Project Overview

The solution is organized into three parts:

### Level 1 (Compulsory)
- PDF ingestion and text extraction
- Chunking using **LangChain RecursiveCharacterTextSplitter**
- Vector embeddings with **Sentence Transformers**
- Semantic search using **FAISS**
- Grounded answering with **citations**
- Strict refusal when information is not supported by documents
- Minimal FastAPI endpoints (`/ingest`, `/ask`, `/health`)

### Level 2 (Optional – Option 1)
- Hybrid retrieval:
  - Vector similarity search
  - BM25 keyword-based retrieval
- Cross-encoder reranking for precision
- Confidence-based refusal to reduce hallucination

### Evaluation
- 50-question evaluation set
- Automatic comparison of Level 1 vs Level 2
- Metrics:
  - Answer rate
  - Refusal rate
  - Retrieval hit-rate
  - Faithfulness
  - Hallucination rate
- Qualitative analysis:
  - 5 best answers
  - 5 worst answers
- Auto-generated `report.md`

---

## Key Design Principles

- **Reliability over coverage**
- **No hallucination**
- **Answers only from retrieved text**
- **Clear citations**
- **Exact refusal message when unsupported**

