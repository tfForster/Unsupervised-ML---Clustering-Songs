# Spotify Song Clustering using PCA and K-Means

## Project Overview

This project explores whether Spotify's audio features can be used to identify **similar songs** and automatically create **playlist-like clusters** using machine learning.

The dataset contains **5000 songs** with Spotify audio features such as *danceability, energy, valence, tempo,* and others.
Using these features, songs are grouped into clusters that represent potential playlists with similar musical characteristics.

## Dataset

The dataset used in this project:

* **3_spotify_5000_songs.csv**
* Contains Spotify audio features for ~5000 tracks
* Includes metadata such as song name, artist, and Spotify link

Example features:

* danceability
* energy
* valence
* tempo
* acousticness
* instrumentalness
* liveness
* speechiness

## Methodology

The workflow follows these main steps:

1. **Data Cleaning**

   * Removed irrelevant columns
   * Kept relevant audio features

2. **Feature Scaling**

   * Used `MinMaxScaler`
   * Scaled all features to a **0–1 range** so no feature dominates the clustering

3. **Dimensionality Reduction**

   * Applied **Principal Component Analysis (PCA)**
   * Retained enough components to explain **95% of the variance**

4. **Clustering**

   * Used **K-Means clustering**
   * Grouped songs into clusters representing potential playlists

## Results

The clustering algorithm groups songs with **similar audio characteristics** together.
Each cluster can be interpreted as a **playlist with a similar mood or musical style**.

Examples of similarities captured:

* low danceability + low energy → calmer songs
* high energy + high danceability → more energetic tracks

However, some songs may still sound different to human listeners despite having similar feature values.

## Repository Structure

```
Unsupervised-ML---Clustering-Songs/
│
├── notebook/
│   └── spotify_song_clustering.ipynb
│
├── data/
│   └── 3_spotify_5000_songs.csv
│
└── README.md
```

## Technologies Used

* Python
* pandas
* NumPy
* scikit-learn
* matplotlib
* seaborn

## Goal of the Project

The goal of this project is to explore how **machine learning techniques such as PCA and clustering** can be applied to music data to discover patterns and generate playlist-like groupings automatically.
