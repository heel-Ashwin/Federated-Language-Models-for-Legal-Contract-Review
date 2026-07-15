# Federated LLM for Privacy-Preserving Legal Contract Review

## Overview

This project presents a hybrid framework for automated legal contract review using Federated Learning and Large Language Models. The proposed system combines LegalBERT for legal clause classification with Phi-2 and LoRA adapters for risk explanation and contract summarization. By adopting a federated learning approach, the framework enables collaborative model training without requiring raw legal contracts to be shared, helping preserve data privacy while maintaining strong predictive performance.

The project was developed as part of the B.Tech Major Project in Computer Science and Engineering (Artificial Intelligence and Machine Learning) at SRM Institute of Science and Technology.

---

## Objectives

- Develop a privacy-preserving legal contract review framework.
- Classify legal contract clauses using LegalBERT.
- Generate contextual risk explanations and contract summaries using Phi-2.
- Implement Federated Learning with FedAvg for decentralized model training.
- Compare centralized and federated model performance.

---

## Repository Structure

```
.
├── Centralized_Phi2.ipynb
├── Centralized_LegalBERT.ipynb
├── Federated_LegalBERT.ipynb
├── Federated_Phi2.ipynb
├── Hybrid_Model.ipynb
├── Model_Comparison.ipynb
├── LEDGAR Dataset
├── Project_Manuscript.pdf
└── README.md
```

---

## Project Workflow

The implementation is divided into six notebooks:

### 1. Centralized Phi-2
Implements a baseline Phi-2 model for legal contract summarization and risk explanation.

### 2. Centralized LegalBERT
Fine-tunes LegalBERT on the LEDGAR dataset for legal clause classification.

### 3. Federated LegalBERT
Simulates distributed client training using Federated Learning and aggregates local model updates using FedAvg.

### 4. Federated Phi-2
Fine-tunes Phi-2 using LoRA adapters in a federated setting to reduce memory and communication overhead.

### 5. Hybrid Model
Integrates the federated LegalBERT classifier with the federated Phi-2 generator to perform end-to-end legal contract analysis.

### 6. Model Comparison
Compares centralized and federated models using classification and text generation evaluation metrics.

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- PEFT (LoRA)
- Federated Learning (FedAvg)
- Scikit-learn
- LEDGAR Dataset
- Google Colab

---

## Evaluation Metrics

### Classification
- Accuracy
- Precision
- Recall
- F1-Score

### Text Generation
- ROUGE-1
- ROUGE-2
- ROUGE-L

---

## Results

| Model | Accuracy | F1 Score |
|------|---------:|---------:|
| Centralized LegalBERT | 0.88 | 0.7855 |
| Federated Hybrid Model | 0.85 | 0.7287 |

| Model | ROUGE-1 | ROUGE-2 | ROUGE-L |
|------|---------:|---------:|---------:|
| Base Phi-2 | 0.545 | 0.300 | 0.545 |
| Federated Hybrid Model | 0.571 | 0.316 | 0.571 |

The federated hybrid framework achieved performance close to centralized training while preserving data privacy by ensuring that raw legal contract data remained on local clients throughout training.

---

## Research Publication

This work was presented at the **3rd International Conference on Advances in Engineering and Management (ICAEM 2026)**.

**Paper Title:**  
**Federated Dual-Model Framework for Privacy-Preserving Legal Contract Analysis**

The complete manuscript is included in this repository.

---

## Future Work

- Improve performance under highly non-IID client distributions.
- Explore advanced federated aggregation algorithms.
- Extend support for multilingual legal documents.
- Integrate Retrieval-Augmented Generation (RAG) for improved legal reasoning.
- Develop a deployable web-based legal contract review application.

---

## Authors

**R. Ashwin**  
**A. Abijith**

Supervisor: **Dr. I. Varalakshmi**  
Assistant Professor  
Department of Computational Intelligence  
SRM Institute of Science and Technology
