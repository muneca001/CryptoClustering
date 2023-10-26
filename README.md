# Cryptocurrency Price Change Prediction

## Overview
Welcome to the Cryptocurrency Price Change Prediction project! In this challenge, I used Python and unsupervised learning techniques to predict whether cryptocurrencies are affected by 24-hour or 7-day price changes.

## Introduction
Cryptocurrencies are known for their price volatility, making them a fascinating subject of analysis. This project focuses on using unsupervised learning techniques to predict how cryptocurrencies are affected by price changes over different time intervals. I will employ StandardScaler from scikit-learn to normalize the data, the elbow method to find the optimal number of clusters (k), and K-means clustering to group cryptocurrencies. Additionally, I will explore Principal Component Analysis (PCA) to optimize my clusters and find the best value of k for the reduced dataset.

## 1. Data Preprocessing
In this section, I prepared the data for analysis. I used the StandardScaler module from scikit-learn to normalize the data obtained from the CSV file. Normalization is a crucial step to ensure that features are on the same scale and do not bias my clustering algorithm.

## 2. Finding the Optimal k
One of the key steps in K-means clustering is determining the optimal number of clusters (k). I employed the elbow method to find the best value for k. This involves creating a list of k values, computing the inertia (within-cluster sum of squares) for each value of k, and plotting an elbow curve to identify the inflection point where the rate of change of inertia starts to slow down. The value of k at this point is my optimal choice for clustering.

## 3. Clustering with K-means
With the optimal k value determined, I clustered cryptocurrencies using the original scaled data. I initialized the K-means model, fit it using the scaled dataset, predict the clusters for each cryptocurrency, and create a scatter plot to visualize the results. This step grouped cryptocurrencies based on their price change characteristics.

## 4. Optimizing Clusters with Principal Component Analysis
In this section, I employed Principal Component Analysis (PCA) to reduce the dimensionality of the dataset. PCA helps determine which features are most informative and reduce computational complexity. I also retrieved the explained variance to understand how much information each principal component contributes.

## 5. Finding the Best Value for k Using the PCA Data
Similar to the previous section, the elbow method was used to find the best value for k, but this time with the reduced dataset obtained from PCA. A comparison was done in order to find the optimal k value from PCA with the one obtained from the original data.

## 6. Clustering with K-means Using the PCA Data
With the best k value identified, I clustered cryptocurrencies using the PCA-transformed data. The clustering process is similar to the previous K-means clustering but applied to the PCA dataset. I visualized the results to understand how using fewer features affect the clusters.

