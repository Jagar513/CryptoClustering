# CryptoClustering
---
# Files
[Challenge 19 Starter Code](https://static.bc-edx.com/data/dl-1-2/m19/lms/starter/Starter_Code.zip)

---
# Instructions
1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

2. Load the crypto_market_data.csv into a DataFrame.

3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

---
# Prepare The Data
- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

- Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

  - The first five rows of the scaled DataFrame should appear as follows:
  ![image](https://github.com/user-attachments/assets/4d5159c0-99c0-4d24-be59-170f11772b71)

---
# Find the Best Value for k Using the Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:
  - Create a list with the number of k values from 1 to 11.
  - Create an empty list to store the inertia values.
  - Create a for loop to compute the inertia with each possible value of k.
  - Create a dictionary with the data to plot the elbow curve.
  - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following question in your notebook: What is the best value for k?

---
# Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
Use the following steps to cluster the cryptocurrencies for the best value for k on the scaled DataFrame:
  - Initialize the K-means model with the best value for k.
  - Fit the K-means model using the scaled DataFrame.
  - Predict the clusters to group the cryptocurrencies using the scaled DataFrame.
  - Create a copy of the scaled DataFrame and add a new column with the predicted clusters.
  - Create a scatter plot using hvPlot as follows:
    - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
    - Color the graph points with the labels found using K-means.
    - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point

---
# Optimize Clusters with Principal Component Analysis
- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

- Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
  - What is the total explained variance of the three principal components?

- Create a new DataFrame with the scaled PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
  - The first five rows of the scaled PCA DataFrame should appear as follows:
    ![image](https://github.com/user-attachments/assets/d8e72200-9a9d-4021-b11d-08861a3e6b84)

---
# Find the Best Value for k Using the PCA DataFrame
Use the elbow method on the scaled PCA DataFrame to find the best value for k using the following steps:
  - Create a list with the number of k-values from 1 to 11.
  - Create an empty list to store the inertia values.
  - Create a for loop to compute the inertia with each possible value of k.
  - Create a dictionary with the data to plot the Elbow curve.
  - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following question in your notebook:
- What is the best value for k when using the scaled PCA DataFrame?
- Does it differ from the best k value found using the original scaled DataFrame?

---
#  Cluster Cryptocurrencies with K-means Using the PCA DataFrame
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA DataFrame:
  - Initialize the K-means model with the best value for k.
  - Fit the K-means model using the scaled PCA DataFrame.
  - Predict the clusters to group the cryptocurrencies using the scaled PCA DataFrame.
  - Create a copy of the scaled PCA DataFrame and add a new column to store the predicted clusters.
  - Create a scatter plot using hvPlot as follows:
    - Set the x-axis as "PC1" and the y-axis as "PC2".
    - Color the graph points with the labels found using K-means.
    - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

Answer the following question:
  - What is the impact of using fewer features to cluster the data using K-Means?

--- 
# REWIND
Recall that you learned how to create composite plots in a previous module. If you need a refresher on how to create these plots, review that module. You can also check [Composing PlotsLinks](https://holoviz.org/tutorial/Composing_Plots.html) in the hvPlot documentation.





