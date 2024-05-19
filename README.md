# Spotify Genre Hit Predictor Documentation

## Introduction

**Spotify Genre Hit Predictor** is a tool designed to forecast the popularity of songs based on their genres and audio features. This project leverages metadata to provide accurate predictions on whether a song will become a hit, specifically targeting the Billboard 100. By focusing on genre-specific trends, this predictor offers a nuanced understanding of musical success, which is beneficial for both artists and listeners.

## Problem Definition

The primary question addressed by this project is: *Given a certain genre, will a specific song be a hit (P(hit | genre))?* This involves analyzing patterns in song metadata to build classifiers capable of predicting a song's potential to reach the Billboard 100.

## Proposed Methods

Our approach is unique in that it considers per-genre variance for popularity prediction. The process includes:

1. **Data Preprocessing:** Removing duplicates and null values, creating histograms of numerical features, and encoding categorical data.
2. **Two-Step Prediction Pipeline:**
   - **Genre Prediction:** Using metadata to predict the genre of a song.
   - **Popularity Prediction:** Predicting if a song will be a hit based on its metadata and the predicted genre.

## Methodology

### Data Exploration and Preprocessing

- **Data Cleaning:** Removed duplicate rows and null values.
- **Feature Engineering:** Created histograms of numerical features, encoded categorical data, and performed exploratory data analysis.
- **Visualization:** Utilized heatmaps, box plots, and histograms to understand data distributions and correlations.

### Dimensionality Reduction

- **Principal Component Analysis (PCA):** Reduced feature dimensions while retaining maximum information.
- **Linear Discriminant Analysis (LDA):** Maximized genre separability by reducing feature space.

### Model Training and Evaluation

- **Genre Classification Models:** Implemented Random Forest, Naive Bayes, and Stochastic Gradient Descent (SGD) to classify songs by genre.
- **Popularity Prediction Models:** Utilized Random Forest, Naive Bayes, and SGD for predicting song popularity.

### Performance Metrics

- **Genre Classification:** Random Forest achieved the highest accuracy (F1 score: 0.879).
- **Popularity Prediction:** Random Forest also performed the best in popularity classification with about an 80% precision score.

## Experiments and Evaluation

### Key Findings

- **Genre Distinguishability:** Genres are distinguishable based on song metadata, with varying effects of musical factors on popularity.
- **Model Accuracy:** Random Forest outperformed other models in both genre classification and popularity prediction.
- **Visualization Component:** An interactive interface allows users to adjust audio features and predict song success dynamically.

## Visualization Interface

Implemented using the Streamlit Python package, the interface provides:

1. **Feature Sliders:** Users can adjust audio features to see their impact on song popularity.
2. **Song Similarity:** Compares user-created songs to popular songs in the dataset to provide actionable insights.

## Literature Survey

### Key References

- **Martin-Gutierrez et al. (2020):** Explored deep learning models for song popularity prediction.
- **Lex et al. (2020):** Investigated changing music preferences over time.
- **Nijkamp (2018):** Analyzed audio features for popularity prediction.
- **Lee et al. (2018):** Combined audio signals and lyrics for better prediction accuracy.
- **Bello (2021):** Emphasized cultural preferences in music consumption.

## Conclusions and Discussion

### Results

Our models accurately predict both genre and song popularity, providing valuable insights for artists and listeners. The tool can guide artists in tailoring their music to current trends and help listeners discover new music.

### Future Work

Future iterations will focus on refining the model to provide actionable steps for making a song popular. This includes conducting artist user studies to evaluate the model's effectiveness.

### Risks and Payoffs

- **Risks:** Potential discouragement for artists releasing songs with low popularity predictions.
- **Payoffs:** Increased recognition and popularity for songs predicted to be hits, providing strategic insights for artists.

All team members have contributed equally to this project.

## Bibliography

The bibliography section includes references to all the literature and studies that informed the development and methodology of this project. It is formatted according to the ACM citation style.
