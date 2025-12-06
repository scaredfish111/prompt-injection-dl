# Prompt Injection Detection with Unsupervised Deep Learning

Detecting prompt injection attacks using unsupervised anomaly detection with autoencoders.

## Research Question

Can unsupervised anomaly detection achieve comparable performance to supervised classification for prompt injection detection?

## Key Results

| Model | Type | Recall | ROC-AUC |
|-------|------|--------|---------|
| Autoencoder (Embeddings) | Unsupervised | 97.89% | 99.65% |
| Autoencoder (TF-IDF) | Unsupervised | 7.33% | 44.85% |
| DistilBERT | Supervised | 96.94% | 99.39% |
| Gradient Boosting | Supervised | 89.57% | 96.18% |

**Finding:** The unsupervised embedding autoencoder achieved 97.89% recall without any labeled malicious examples—comparable to supervised methods.

## Approach

- Train autoencoder on benign prompts only
- Malicious prompts produce high reconstruction error (anomalies)
- Compare TF-IDF vs sentence embeddings

## Dataset

[Malicious Prompt Detection Dataset (MPDD)](https://www.kaggle.com/datasets/mohammedaminejebbar/malicious-prompt-detection-dataset-mpdd) - 39,234 labeled prompts

## Files

- `Prompt-Injection-DL.ipynb` - Main notebook with EDA, model training, and analysis

## Previous Work

[Supervised ML approach](https://github.com/scaredfish111/prompt-injection)
