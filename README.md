# 🎬 Hybrid Movie Recommender System

This repository contains a Jupyter Notebook (`MovieRecomendationSystem.ipynb`) that implements a **Hybrid Movie Recommender System**.

---

## 📌 Overview

The system recommends movies from the **MovieLens** catalog by providing a ranked **Top-N list** of unseen movies per user.

It uses a **Cascade Hybrid Strategy**, combining both:

- **Content-Based Filtering**
- **Collaborative Filtering**

---

## ⚙️ System Details

| Feature | Description |
|---|---|
| **Domain** | Movies |
| **Dataset** | `ml-latest-small` MovieLens |
| **Content-Based Filtering** | TF-IDF + Cosine Similarity |
| **Collaborative Filtering** | SVD |
| **Algorithm Strategy** | Cascade Hybrid Content-Based → Collaborative Filtering |

---

## 🧠 How It Works

### Stage 1 — Content-Based Filter

Uses **TF-IDF** on genre features and **Cosine Similarity** to generate an initial pool of candidate movies.

### Stage 2 — Collaborative Filter

**Singular Value Decomposition (SVD)** predicts the rating for each candidate movie from Stage 1 to produce the final ranked **Top-N recommendations**.

### Cold-Start Fallback

If a user has no prior history, the system falls back to a **Bayesian Popularity model**.

---

## 📦 Requirements

To run the notebook, you need the following libraries:

```txt
numpy<2.0.0
pandas
matplotlib
seaborn
scikit-learn
scikit-surprise
tabulate
```


## 🛠️ Installation

```bash
pip install "numpy<2.0.0" scikit-surprise pandas matplotlib seaborn scikit-learn tabulate
```

---

## ▶️ Usage

Make sure you have the `ml-latest-small` MovieLens dataset available in your working directory under the folder:

```txt
ml-latest-small
```

Open and run:

```txt
MovieRecomendationSystem.ipynb
```
