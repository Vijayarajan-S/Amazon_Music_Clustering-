Here's a clean, professional report you can use:

---

# **Amazon Music Clustering & Visualization Report**

## **1. Objective**

The goal of this project was to perform **unsupervised learning** on Amazon Music data to group similar songs together based on audio features, visualize the clusters, and create a basic recommendation system.

---

## **2. Data Preprocessing**

* **Dataset Used:** `single_genre_artists.csv`
* **Steps Performed:**

  * Removed irrelevant columns: `id_songs`, `id_artists`, `release_date`, etc.
  * Checked and handled missing values and duplicates.
  * Selected **key audio features** for clustering:

    * `danceability`, `energy`, `loudness`, `speechiness`,
      `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`.

---

## **3. Feature Scaling**

* Applied **StandardScaler** to standardize audio features.
* Ensured all features were on the same scale to improve clustering performance.

---

## **4. Clustering (KMeans)**

* Implemented **KMeans Clustering** on scaled data.
* **Optimal Number of Clusters:**

  * Used **Elbow Method (WCSS)** and **Silhouette Score** to determine the best number of clusters.
* Assigned cluster labels to each song for further analysis.

---

## **5. Dimensionality Reduction & Visualization**

* Applied **Principal Component Analysis (PCA)** to reduce features to **3 dimensions** for visualization.
* Re-ran KMeans on PCA-transformed data to validate clustering structure.
* Used **Plotly** to create **interactive 3D cluster plots**.

---

## **6. Genre Imputation**

* Cleaned and standardized genre column.
* **Filled missing genres** by assigning the most common genre within the corresponding cluster.
* Improved dataset completeness for better analysis.

---

## **7. Text-Based Clustering**

* Created a **profile column** combining `genre + artist name`.
* Applied **TF-IDF Vectorization** to convert text profiles into numerical representations.
* Performed **KMeans clustering** on TF-IDF vectors to group songs based on textual similarity.

---

## **8. Recommendation System**

* Built a **content-based recommendation system**:

  * Used **cosine similarity** on TF-IDF vectors.
  * Returned top N most similar songs for a given input song.
* Enabled a simple way to explore music recommendations.

---

## **9. Visualization**

* Plotted:

  * **Feature distributions** (Matplotlib, Seaborn).
  * **Cluster assignments** and **PCA projections** (Plotly).
* Visualizations provided insights into:

  * Feature patterns across clusters.
  * Separation of songs in reduced-dimensional space.

---

## **10. Key Libraries Used**

* **Data Processing:** pandas, numpy
* **Clustering & Modeling:** scikit-learn
* **Visualization:** matplotlib, seaborn, plotly
* **Dimensionality Reduction:** PCA (scikit-learn), UMAP (optional exploration)

---

## **Outcome**

✅ Successfully clustered songs based on **audio features** and **text profiles**
✅ Generated clear **3D visualizations** for cluster insights
✅ Imputed missing genres based on cluster majority
✅ Built a **content-based recommender system** to suggest similar songs

This project demonstrates how **unsupervised learning + visualization techniques** can be combined to explore music datasets and create meaningful recommendations.


