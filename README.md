# CryptoClustering Project Report

## Introduction

In this project, we aim to predict if cryptocurrencies are affected by 24-hour or 7-day price changes using Python and unsupervised learning techniques. This document serves as a summary of the steps taken and the results achieved during the assignment.

## Data Preparation

1. Utilized the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file.
2. Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Finding the Best Value for k (Using Original Scaled Data)

1. Applied the elbow method to find the optimal value for k using the following steps:
   - Created a list with k values from 1 to 11.
   - Computed the inertia (within-cluster sum of squares) for each k.
   - Plotted an elbow curve to identify the best k value.

## Clustering Cryptocurrencies with K-means (Using Original Scaled Data)

1. Initialized the K-means model with the best value for k.
2. Fit the K-means model using the original scaled DataFrame.
3. Predicted the clusters and added a new column with the predicted clusters.
4. Created a scatter plot using `hvPlot` to visualize the clusters.

## Optimizing Clusters with Principal Component Analysis (PCA)

1. Performed PCA on the original scaled DataFrame to reduce the features to three principal components.
2. Retrieved the explained variance for each principal component.

## Finding the Best Value for k (Using PCA Data)

1. Applied the elbow method on the PCA data to find the best value for k, following similar steps as before.

## Clustering Cryptocurrencies with K-means (Using PCA Data)

1. Initialized the K-means model with the best value for k obtained using PCA.
2. Fit the K-means model using the PCA data.
3. Predicted the clusters and added a new column to store the predicted clusters.
4. Created a scatter plot using `hvPlot` to visualize the clusters.

## Impact of Using Fewer Features for K-Means Clustering

**Answer:** Using fewer features (in this case, the three principal components from PCA) to cluster the data using K-Means can impact the results. It may lead to a different grouping of cryptocurrencies, as the PCA components capture the most significant variance in the data. This can result in more meaningful and efficient clustering when dealing with high-dimensional data.

## Conclusion

This project successfully applied unsupervised learning techniques, including K-means clustering and Principal Component Analysis, to analyze and cluster cryptocurrency data. It demonstrated the importance of feature selection and the impact of dimensionality reduction on the clustering results. The optimal value for k was determined both using the original data and PCA, and the results were compared to gain insights into the clustering process.

For more detailed code implementation and visualizations, please refer to the `Crypto_Clustering.ipynb` notebook in this repository.
