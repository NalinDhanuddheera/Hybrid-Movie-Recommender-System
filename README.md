# 🎬 Hybrid Movie Recommender System

This repository contains a Jupyter Notebook (`MovieRecomendationSystem.ipynb`) that implements a **Hybrid Movie Recommender System**.

---

## 📌 Overview

The system recommends movies from the **MovieLens** catalog by providing a ranked **Top-N list** of unseen movies per user.

It uses a **Cascade Hybrid Strategy**, combining both **Content-Based Filtering** and **Collaborative Filtering**.

---

## ⚙️ System Details

| Feature | Description |
|---|---|
| **Domain** | Movies |
| **Dataset** | `ml-latest-small` (MovieLens) |
| **Content-Based Filtering** | TF-IDF on genre features + Cosine Similarity |
| **Collaborative Filtering** | SVD (100 latent factors) via `scikit-surprise` |
| **Algorithm Strategy** | Cascade Hybrid (Content-Based → Collaborative Filtering) |

---

## 🧠 How It Works

| Stage | Description |
|---|---|
| **Stage 1 — Content-Based Filter** | Encodes movie genres using TF-IDF and computes Cosine Similarity to build a candidate pool of the 60 most similar movies to a given seed movie. |
| **Stage 2 — Collaborative Filter** | SVD predicts the rating each user would give to every candidate movie from Stage 1, and returns the final Top-N ranked recommendations. |

---

## 📦 Requirements

To run the notebook, you need the following libraries:

| Library |
|---|
| `numpy<2.0.0` |
| `pandas` |
| `matplotlib` |
| `seaborn` |
| `scikit-learn` |
| `scikit-surprise` |
| `tabulate` |

---

## 🛠️ Installation

```bash
pip install "numpy<2.0.0" scikit-surprise pandas matplotlib seaborn scikit-learn tabulate
```

---

## ▶️ Usage

1. Make sure you have the `ml-latest-small` MovieLens dataset available in your working directory under the folder `ml-latest-small`. The notebook can also download it automatically via `wget`.

2. Open and run `MovieRecomendationSystem.ipynb` to see the data preparation, model training, and recommendation generation.
