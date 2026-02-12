Multimodal Product Recommendation System using BERT and ResNet50

This project builds a multimodal, content-based product recommendation system that combines visual and textual data using ResNet50 and BERT.
It identifies similar products based on image and text features — ideal for fashion retail and e-commerce platforms.

🚀 Overview

Uses ResNet50 for visual feature extraction (images)

Uses BERT (base-uncased) for textual feature extraction (product metadata)

Combines both into a unified 2816-dimensional feature vector

Computes cosine similarity to find similar products

Enables content-based recommendations without user interaction data

Includes visualizations for product trends, color preferences, and category performance

🧩 Methodology

<img width="392" height="387" alt="Screenshot 2026-02-13 000838" src="https://github.com/user-attachments/assets/bb6e66b0-2de3-4982-8a3f-d7c15ac2d9c3" />


Dataset:

Fashion Product Images (Small) Dataset (Kaggle)

44,419 items with images and metadata

Feature Extraction:

Text → 768-dim BERT embeddings

Image → 2048-dim ResNet50 embeddings

Fusion:

Normalized embeddings concatenated → 2816-dim vector

Similarity Computation:

Cosine similarity between product vectors

Top-K similar products retrieved using FAISS

📈 Results
Metric	Value
Mean Top-1 Similarity	0.9971
Mean Top-5 Similarity	> 0.99
Model Accuracy (MPSR)	64.39%
Fashion-GPT (Baseline)	63%
FashionLLM (Baseline)	62.17%
