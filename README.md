# Human-in-the-Loop Healthcare Information Identification Using BioBERT

A biomedical Named Entity Recognition (NER) project that uses BioBERT to identify disease-related healthcare information from biomedical text.

## Project Overview

This project fine-tunes BioBERT for healthcare information identification using an annotated biomedical text dataset based on the NCBI Disease Research Abstracts dataset.

The model identifies four healthcare entity categories:

- SpecificDisease
- DiseaseClass
- Modifier
- CompositeMention

The project also introduces a Human-in-the-Loop layer. Predictions below a selected confidence threshold are flagged for human review rather than being automatically accepted.

## Model Performance

Final held-out test results:

| Metric | Result |
|---|---:|
| Precision | 45.18% |
| Recall | 58.59% |
| F1-Score | 51.02% |

The strongest entity category was **SpecificDisease**, with approximately **85% recall** and an **F1-score of 0.64**.

## Technology Stack

- Python
- Google Colab
- BioBERT
- Hugging Face Transformers
- PyTorch
- scikit-learn
- Seqeval
- Matplotlib

## Key Features

- Biomedical Named Entity Recognition
- BioBERT transfer learning
- BIO token labeling
- WordPiece tokenization
- Long-document chunking
- Precision, Recall and F1 evaluation
- Confidence-aware predictions
- Human-in-the-Loop review

## Dataset

The project uses a prepared subset based on the NCBI Disease Research Abstracts dataset for healthcare entity extraction.

Dataset:
https://storage.googleapis.com/cloud-samples-data/language/ucaip_ten_dataset.jsonl

## Human-in-the-Loop Approach

The model produces a confidence score for detected healthcare entities.

High-confidence predictions can be accepted, while lower-confidence predictions can be flagged for human review.

The confidence threshold used in the project demonstration is experimental and is not a clinically validated threshold.

## Disclaimer

This project is an educational and research prototype. It is not intended for clinical diagnosis, treatment decisions, or other medical decision-making.
