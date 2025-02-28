# CryptoClustering
Module 19 Challenge

![download](https://github.com/user-attachments/assets/3a86f7da-61ad-4216-a501-e243898a4648)

In this challenge, I used my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

# **Prepare the Data**
•	Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

•	Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# **Find the Best Value for k Using the Original Scaled DataFrame**

Use the elbow method to find the best value for k using the following steps:

•	Create a list with the number of k values from 1 to 11.

•	Create an empty list to store the inertia values.

•	Create a for loop to compute the inertia with each possible value of k.

•	Create a dictionary with the data to plot the elbow curve.

•	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

## Answer the following question: 

**Question:** What is the best value for `k`?

**Answer:** Based on the elbow rule, 4 would be the best value for 'k'!

# **Cluster Cryptocurrencies with K-means Using the Original Scaled Data**

Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

•	Initialize the K-means model with the best value for k.

•	Fit the K-means model using the original scaled DataFrame.

•	Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.

•	Create a copy of the original data and add a new column with the predicted clusters.

•	Create a scatter plot using hvPlot as follows:

o	Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".

o	Color the graph points with the labels found using K-means.

o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

# **Optimize Clusters with Principal Component Analysis**

•	Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

•	Retrieve the explained variance to determine how much information can be attributed to each principal component and then 

## Answer the following question:

**Question:** What is the total explained variance of the three principal components?

**Answer:**  Total Explained Variance:0.3719856+0.34700813+0.17603793=0.89503166

Total Explained Variance = 0.89503166

The total explained variance of the three principal components is approximately 0.8950 or 89.50%.

•	Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# **Find the Best Value for k Using the PCA Data**

Use the elbow method on the PCA data to find the best value for k using the following steps:

•	Create a list with the number of k-values from 1 to 11.

•	Create an empty list to store the inertia values.

•	Create a for loop to compute the inertia with each possible value of k.

•	Create a dictionary with the data to plot the Elbow curve.

•	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

##	Answer the following question:

* **Question:** What is the best value for `k` when using the PCA data?

  * **Answer:** The best value for `k` when using the PCA data is 4. 


* **Question:** Does it differ from the best k value found using the original data?

  * **Answer:** No, it does not differ from the best k value found when using the original data

# **Cluster Cryptocurrencies with K-means Using the PCA Data**

Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

•	Initialize the K-means model with the best value for k.

•	Fit the K-means model using the PCA data.

•	Predict the clusters to group the cryptocurrencies using the PCA data.

•	Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

•	Create a scatter plot using hvPlot as follows:

o	Set the x-axis as "PC1" and the y-axis as "PC2".

o	Color the graph points with the labels found using K-means.

o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Answer the following question: 

* **Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

  * **Answer:** Using fewer features to cluster the data can simplify the model and improve interpretability and readability by making clusters easier to visualize and understand. However, this reduction can lead to the loss of important data and, potentially result in less accurate clusters and more overlapping groups. 
