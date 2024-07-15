# Crypto Clustering Project

## Introduction
This project aims to utilize an unsupervised learning model to determine if cryptocurrencies are affected by 24-hour or 7-day price changes. The data preparation was done using the StandardScaler function, followed by determining the optimal value for 'k' using the original scaled data. Clusters were then plotted using the results.

Further optimization of the clusters was achieved through Principal Component Analysis (PCA). The optimal 'k' value was re-evaluated using the PCA data, and clusters were plotted based on this analysis. Finally, all charts were displayed side-by-side to determine the best approach.

## Files
The repository contains the following files:

**README.md:** This ReadMe file for the project.

**Crypto_Clustering_final.ipynb:** The completed Jupyter notebook.

**Crypto_Clustering_starter.ipynb:** The provided Jupyter notebook with starter code.

**Resources/crypto_market_data.csv:** The dataset used for the analysis.

**images/:** A folder containing images used in the README file.

## Data Preparation
Data preparation involved the use of the StandardScaler function to standardize the features in the dataset. This step ensures that each feature contributes equally to the distance calculations performed during clustering.

# K-Value Algorithm
## Find the Best Value for k Using the Original Scaled Data
The best K value was determined to be 4 after calculations using the elbow method.

## Apply the K-means Algorithm to Cluster Cryptocurrencies
Using the determined K value of 4, the K-means algorithm was applied to cluster the cryptocurrencies. The resulting clusters were plotted, but some overlap was observed, indicating that the clusters might not be well-separated.


# PCA & K-Value Algorithm
## Perform a PCA to Reduce the Features to Three Principal Components
PCA was performed to reduce the dataset's features to three principal components. This dimensionality reduction helps in visualizing the data more effectively and can improve clustering performance.

## Calculate the Total Explained Variance
The total explained variance was calculated to be approximately 89.5% (0.8950316570309841), indicating that the three principal components retained most of the original dataset's information.

## Find the Best Value for k After PCA
Using the PCA data, the best K value was re-evaluated and found to be 4, similar to the original scaled data.

## Apply the K-means Algorithm to Cluster Cryptocurrencies After PCA
The K-means algorithm was again applied using the PCA data, resulting in well-separated clusters, with much less overlap compared to the original scaled data.


# Summary
The best number of clusters was determined to be 4, both with the original scaled data and after applying PCA. PCA effectively reduced the dataset's dimensionality and combined the variables/features more tightly to generate new PCA variables. This provided better visualization for clustering. The market plot using K-Means from the scaled dataset showed some overlap, but after applying PCA, the dataset was divided clearly into 4 distinct clusters.

# Answered Questions
**What is the impact of using fewer features to cluster the data using K-Means?**
Using fewer features, as achieved through PCA, removes some of the variability and helps delineate the clusters more clearly for a better learning model. Using the original scaled data, there is a cluster that sits in the middle of another cluster. This is eliminated using PCA.

**What is the best value for k when using the PCA data?**
The best k value using PCA is clearly 4.

**Does it differ from the best k value found using the original data?**
No, the original data also showed 4, but the PCA data is a little more distinct, and total inertia is lower.

**What is the total explained variance of the three principal components?**
The total explained variance for the model is 89.5%.

**What is the best value for k?**
Judging from the graph, '4' is the best fit.
