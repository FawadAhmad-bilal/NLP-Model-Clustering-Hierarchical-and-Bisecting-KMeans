# NLP Model Clustering — Hierarchical & Bisecting KMeans

Unsupervised clustering analysis on the GLUE benchmark dataset, comparing **Agglomerative Hierarchical Clustering** and **Bisecting KMeans** to group NLP models based on their performance patterns across multiple tasks.

## Overview

The GLUE (General Language Understanding Evaluation) benchmark tracks how well NLP models perform across diverse language tasks. This project applies unsupervised learning to discover natural groupings among models like BERT, RoBERTa, T5, and ERNIE — without using score labels.

## Dataset

**Source:** Seaborn built-in `glue` dataset  
**Size:** 64 rows × 5 columns

| Column | Type | Description |
|--------|------|-------------|
| Model | Categorical | NLP model name (BERT, T5, RoBERTa, etc.) |
| Year | Numeric | Year the model was released |
| Encoder | Categorical | Architecture type (Transformer / LSTM) |
| Task | Categorical | GLUE benchmark task (CoLA, SST-2, MRPC, etc.) |
| Score | Numeric | Benchmark performance score |

## Methodology

1. **Exploratory Data Analysis** — value counts, pairplot visualization
2. **Preprocessing** — LabelEncoder for categorical features (Model, Encoder, Task)
3. **Agglomerative Hierarchical Clustering** — bottom-up merging with dendrogram
4. **Bisecting KMeans** — divisive approach, splitting clusters recursively
5. **Comparison** — cluster assignments from both methods analyzed side by side

## Tech Stack

| Library | Purpose |
|---------|---------|
| Pandas | Data manipulation |
| Seaborn / Matplotlib | Visualization & pairplot |
| Scikit-learn | LabelEncoder, AgglomerativeClustering, BisectingKMeans |

## Results

Both clustering methods successfully grouped NLP models into meaningful clusters based on architecture type (Transformer vs LSTM) and release year, reflecting real-world performance tiers in the GLUE benchmark.

## Author

**Fawad Ahmad**  
BSAI Student — University of Haripur, Pakistan  
[github.com/FawadAhmad-bilal](https://github.com/FawadAhmad-bilal)
