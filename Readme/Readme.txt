# Cryptocurrency Clustering Analysis

## Project Overview

This project aimed to analyze and cluster cryptocurrency market data using unsupervised learning techniques. We explored the impact of dimensionality reduction (Principal Component Analysis - PCA) on the clustering results and compared the outcomes of clustering on the original scaled data versus the PCA-transformed data.

## Project Objectives

* Load and preprocess cryptocurrency market data.
* Apply data scaling using `StandardScaler`.
* Perform dimensionality reduction using PCA.
* Determine the optimal number of clusters (`k`) using the elbow method.
* Cluster cryptocurrencies using K-means.
* Visualize and compare clustering results with and without PCA.
* Calculate and display correlation matrix.
* Use TSNE to visualize high dimensional data in 2d.
* Evaluate clustering performance using inertia, silhouette score, and Calinski-Harabasz score.

## Data

The dataset used in this project is `crypto_market_data.csv`, containing historical market data for various cryptocurrencies.

## Libraries Used

* `pandas`
* `sklearn` (specifically `StandardScaler`, `PCA`, `KMeans`, `TSNE`, `silhouette_score`, `calinski_harabasz_score`)
* `hvplot`
* `matplotlib.pyplot`

## Project Structure

1.  **Data Loading and Preprocessing:**
    * The `crypto_market_data.csv` file was loaded into a Pandas DataFrame.
    * The data was scaled using `StandardScaler` to normalize the features.

2.  **Dimensionality Reduction (PCA):**
    * PCA was applied to reduce the dimensionality of the scaled data to three principal components.
    * Explained variance ratios were calculated and visualized to determine the optimal number of components.

3.  **Determining the Optimal Number of Clusters (Elbow Method):**
    * The elbow method was used to find the optimal number of clusters (`k`) for K-means.
    * This was done for both the original scaled data and the PCA-transformed data.
    * Silhouette score and Calinski-Harabasz scores were also used to evaluate the best k value.

4.  **K-means Clustering:**
    * K-means clustering was performed on both the original scaled data and the PCA-transformed data, using the optimal `k` value.
    * The cluster assignments were added as a new column to the respective DataFrames.

5.  **Visualization and Comparison:**
    * Scatter plots were created to visualize the clusters in the PCA space and the original scaled data space.
    * Elbow curves were plotted to compare the optimal `k` values.
    * Correlation matrix was created and visualized as a heatmap.
    * TSNE was used to visualize the high dimensional scaled data in 2d.
    * The impact of using PCA on the clustering results was analyzed.

## Key Findings

* PCA can significantly impact the clustering results by simplifying the clusters and potentially changing the optimal number of clusters.
* Using fewer features (after PCA) can improve computational efficiency and make visualizations easier.
* The optimal `k` value may differ between the original scaled data and the PCA-transformed data.
* The correlation matrix allows us to see how each cryptocurrency feature relates to each other.
* TSNE allows us to see how the high dimensional data relates in a 2d space.
* Silhouette score and Calinski-Harabasz scores allow for better k-means cluster evaluation.

## How to Run the Code

1.  Ensure you have all the required libraries installed.
2.  Place the `crypto_market_data.csv` file in the `Resources` folder.
3.  Run the Python scripts in the provided order.
4.  Analyze the generated plots and output.

## Conclusion

This project provided valuable insights into clustering cryptocurrency market data and the impact of dimensionality reduction. The results can be used to better understand the relationships between different cryptocurrencies and identify potential investment opportunities.