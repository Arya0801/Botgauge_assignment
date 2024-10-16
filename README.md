# Multi-Stage Retrieval Pipeline for Question Answering
This project implements a multi-stage text retrieval pipeline using embedding and ranking models for question-answering tasks. The application is built with Streamlit.
There are two embedding models are used (one small and one lagre) and for each of them two ranking models are used to understand trade-offs related to model size, accuracy, and performance.
Embedding models:
1) sentence-transformers/all-MiniLM-L6-v2 (Small)
2) sentence-transformers/all-distilroberta-v1 (Large)
Ranking models:
1) cross-encoder/ms-marco-TinyBERT-L-6 
2) cross-encoder/ms-marco-MiniLM-L-12-v2

# Features
Stage 1: Candidate retrieval using embedding models.
Stage 2: Reranking the retrieved passages with ranking models.
Custom Evaluation: Performance measured using custom metrics (no BEIR).
# Setup Instructions
Prerequisites
Python 3.8+ installed.

# Steps
Install Dependencies:

pip install -r requirements.txt
Run the Application:

streamlit run [file name].py
# Usage
Input a question, and the system retrieves and reranks relevant passages from the dataset.
Custom evaluation metrics like NDCG@10.
# Dataset
Natural Questions (NQ) dataset from the BEIR benchmark.
