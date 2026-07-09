# Movie Recommendation Systems

This repository contains two recommendation system implementations using different approaches:

1. **Content-Based Recommendation**
2. **Collaborative Filtering using Matrix Factorization**

The goal of this project is to implement, explore and compare different recommendation techniques on two public movie datasets.


# 1. Content-Based Recommendation

### Dataset

* Netflix Movies and TV Shows Dataset

### Overview

This notebook implements a **content-based movie recommendation system**.

Instead of treating all textual information as a single feature, each column is processed independently. Different text representation techniques are evaluated for each feature to determine the most suitable embedding method.

The following approaches are explored:

* TF-IDF
* Word Embeddings
* Sentence Transformers (SBERT)

For every relevant column, the best-performing embedding technique is selected. The resulting feature vectors are then concatenated into a single representation for each movie.

Finally, **Cosine Similarity** is used to measure the similarity between movie vectors.

### Recommendation Process

Given a movie title:

1. Retrieve its feature vector.
2. Compute cosine similarity with all other movie vectors.
3. Rank movies based on similarity scores.
4. Recommend the most similar movies.

---

# 2. Collaborative Filtering using Matrix Factorization

### Dataset

* MovieLens 100K

### Overview

This notebook implements a recommendation system using **Matrix Factorization** trained with **Stochastic Gradient Descent (SGD)**.

The implementation is built step by step, starting from the mathematical formulation of matrix factorization and gradually adding model optimization.

The model is trained by experimenting with different hyperparameters, including:

* Number of latent factors (K)
* Learning rate
* Number of training epochs

The objective is to minimize the prediction error (RMSE) on unseen ratings.

### Prediction

After training, the model predicts ratings for movies that users have not yet rated.

These predicted ratings can then be used to recommend movies with the highest estimated preference for each user.

---

## Methods Used

### Content-Based Filtering

* TF-IDF
* Word Embeddings
* Sentence-BERT (SBERT)
* Cosine Similarity

### Collaborative Filtering

* Matrix Factorization
* Stochastic Gradient Descent (SGD)
* RMSE Evaluation

---

## Datasets

* Netflix Movies and TV Shows Dataset
* MovieLens 100K

---

## Technologies

* Python
* NumPy
* Pandas
* Scikit-learn
* Spacy
* Transformers
* Jupyter Notebook

---

## Future Improvements


* Two-Tower (Currently Developing this model)
* Hybrid Recommendation System
* Neural Collaborative Filtering
