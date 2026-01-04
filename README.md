# Track 1 – Medical Retrieval Baseline (BM25)

## Project
Explainable and Safe Medical Support Chatbot using Generative AI

## Description
This repository contains the Track 1 assignment for a medical retrieval system.
The project implements a BM25-based evidence retrieval pipeline using the PubMedQA dataset.

## Contents
- track1_bm25_clean.ipynb – Colab notebook with full implementation
- Explainable_Safe_Medical_Support_Chatbot_Track_1_BM25_Report.docx – Technical report

## Method
- Dataset: PubMedQA (labeled subset)
- Retrieval method: BM25 (rank-bm25)
- Top-k retrieval: k = 5

## Status
Track 1 completed successfully.
## Evaluation Summary
The BM25 baseline was evaluated using standard retrieval metrics on PubMedQA.

- Recall@5: 0.988
- Recall@10: 0.993
- MRR@10: 0.964
- nDCG@10: 0.971

Detailed evaluation results and error analysis are available in
[EVALUATION.md](./EVALUATION.md).
