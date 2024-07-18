# Cryptocurrency Clustering Analysis

This project involves clustering cryptocurrencies based on their market performance data. The clustering analysis is conducted using K-Means, both on the original data and on data reduced by Principal Component Analysis (PCA).

## Project Structure

- `Resources/crypto_market_data.csv`: The dataset containing cryptocurrency market data.
- `analysis.py`: The main script performing data loading, preprocessing, clustering, and visualization.
- `README.md`: This document.

## Analysis Steps

### 1. Load and Explore the Data

* Load the data into a Pandas DataFrame.
* Display the first 10 rows of the data.
* Generate summary statistics.
* Plot the data to visualize initial trends.

### 2. Data Preprocessing

* Normalize the data using `StandardScaler` from scikit-learn.
* Create a DataFrame with the scaled data.

### 3. Find the Best Value for `k` Using the Original Data

* Create a list of `k` values ranging from 1 to 11.
* Compute the inertia for each `k` value using K-Means.
* Plot an Elbow Curve to determine the optimal `k`.

### 4. Cluster Cryptocurrencies with K-Means Using the Original Data

* Initialize the K-Means model with the best `k` value.
* Fit the model and predict the clusters.
* Add the predicted clusters to the DataFrame.
* Create a scatter plot to visualize the clusters.

### 5. Optimize Clusters with Principal Component Analysis (PCA)

* Reduce the data to three principal components using PCA.
* Compute the explained variance to understand the variance retained by the principal components.
* Create a new DataFrame with the PCA data.

### 6. Find the Best Value for `k` Using the PCA Data

* Repeat the process of finding the best `k` value using the PCA data.
* Plot an Elbow Curve to determine the optimal `k`.

### 7. Cluster Cryptocurrencies with K-Means Using the PCA Data

* Initialize the K-Means model with the best `k` value for PCA data.
* Fit the model and predict the clusters.
* Add the predicted clusters to the PCA DataFrame.
* Create a scatter plot to visualize the PCA clusters.

### 8. Composite Plots

* Plot Elbow Curves for both the original and PCA data for comparison.
* Create composite scatter plots to contrast the clusters formed by original and PCA data.

## Results

* **Best value for `k` using the original data** : 3
* **Total explained variance of the three principal components** : 89.5%.
* **Best value for `k` using the PCA data** : 3
* **Comparison of `k` values** : The best `k` value is the same (3) for both original and PCA data.
* **Impact of PCA on Clustering** : Using PCA simplifies the data, reduces noise, and can lead to more compact and better-separated clusters, but also involves some loss of information.

## Visualization

* The scatter plots visualize the clusters formed by the original and PCA data.
* The Elbow Curves help determine the optimal number of clusters.
