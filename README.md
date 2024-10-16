# Multi-Stage Retrieval Pipeline for Question Answering
This project implements a multi-stage text retrieval pipeline for question-answering tasks, built using Streamlit. Two embedding models, one small and one large, are employed. For each embedding model, two ranking models are used to analyze trade-offs between model size, accuracy, and performance.

- **Embedding models:**
1) sentence-transformers/all-MiniLM-L6-v2 (Small)
2) sentence-transformers/all-distilroberta-v1 (Large)
- **Ranking models:**
1) cross-encoder/ms-marco-TinyBERT-L-6 
2) cross-encoder/ms-marco-MiniLM-L-12-v2

## Features
- **Stage 1:** Candidate retrieval using embedding models.
- **Stage 2:** Reranking the retrieved passages with ranking models.
Custom Evaluation: Performance measured using custom metrics (no BEIR).
## Setup Instructions
### Prerequisites
Python 3.8+ installed.

### Steps
**Install Dependencies:**
```bash
pip install -r requirements.txt
```
**Run the Application:**
```bash
streamlit run [file name].py
```
## Usage
Input a question, and the system retrieves and reranks relevant passages from the dataset.
Custom evaluation metrics like NDCG@10.
## Dataset
Natural Questions (NQ) dataset from the BEIR benchmark.
