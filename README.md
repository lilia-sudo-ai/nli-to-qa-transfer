# README

## Author
Lilia Maiorova

## Project Summary

This project explores how knowledge learned from Natural Language Inference (NLI) transfers to Question Answering (QA) tasks. 
I compare multilingual XLM-R models trained directly on QA (extractive and general) with models that are first trained on NLI (in English or Russian) and then fine-tuned for QA. 
The results show that transfer learning improves performance, especially for general QA tasks that rely more on reasoning.

Model checkpoints and full outputs are available upon request / via external storage.

## Directory Structure

nli-to-qa-transfer/
│── README.md
│── nli_to_qa_transfer_learning.ipynb
│── results/
│   ├── compare_EM_QAonly_vs_transfer
│   ├── compare_F1_QAonly_vs_transfer
│   ├── compare_boolqa_accuracy
│   ├── compare_boolqa_f1

## Versions
Python: 3.12
Transformers: 4.x
Datasets: 3.x
PyTorch: 2.x
NumPy: 2.x
Matplotlib: 3.x
Evaluate: latest 

## Runtime
All experiments were run in Google Colab (GPU runtime).

Approximate runtimes:

NLI fine-tuning (EN / RU): ~1–2 hours
QA training: ~30–60 minutes per run
Transfer learning experiments: ~30 minutes
Plot generation: ~5–10 seconds
Total: ~ 12-14 hours

All outputs (models, plots, logs) are saved using relative paths, so the project can run on any machine.

## External Material
- XNLI dataset (cross-lingual NLI; translated from English)
- SQuAD-style QA datasets (for extractive QA)
- BoolQA-style dataset (for general yes/no QA)
- Hugging Face Transformers & Datasets libraries


## Additional Features
- Full pipeline for **cross-lingual and cross-task transfer learning (NLI → QA)**  
- Comparison of:
  - Baseline QA training  
  - Transfer from English NLI  
  - Transfer from Russian NLI  
  - Monolingual RuBERT model  
- Experiments on both:
  - **Extractive QA (span prediction)**  
  - **General QA (yes/no classification)**  
- Custom post-processing for QA predictions (token → text conversion)  
- Evaluation using **F1 and Exact Match (SQuAD metric)**  
- Training curves and comparison plots:
  - validation EM / F1  
  - accuracy / loss  
  - transfer vs baseline comparisons  
- Analysis of transfer effects:
  - stronger gains for general QA vs extractive QA  
  - comparison of English vs Russian NLI transfer  