# Track 1 – BM25-based Medical Retrieval Baseline

This project implements a classical BM25 retrieval baseline for medical question answering using the PubMedQA dataset. The goal is to establish a strong sparse-retrieval baseline and evaluate its effectiveness using standard information retrieval metrics.

---

## Dataset
- **PubMedQA (pqa_labeled subset)**
- Each sample consists of a medical question paired with a gold evidence context.

---

## Preprocessing
- Extracted question and context fields
- Normalized structured contexts into flat text
- Chunked documents using:
  - Chunk size: 400 words
  - Overlap: 50 words
- Lowercasing and whitespace tokenization

---

## Retrieval Method
- **BM25 (rank-bm25)**
- Documents indexed at chunk level
- Queries tokenized using simple whitespace splitting

---

## Evaluation
Retrieval performance is evaluated using:
- Recall@5
- Recall@10
- MRR@10
- nDCG@10

### Results
| Metric     | Score |
|-----------|-------|
| Recall@5  | 0.988 |
| Recall@10 | 0.993 |
| MRR@10    | 0.964 |
| nDCG@10   | 0.971 |

---

## Error Analysis
Only two failure cases were observed due to strong lexical overlap in PubMedQA.

Common failure patterns:
1. Lexical mismatch between query and gold context terminology
2. Relevant evidence spread across multiple chunks

These failures highlight limitations of sparse retrieval and motivate future dense or hybrid approaches.

---

## Reproducibility

### Setup
```bash
pip install -r requirements.txt
