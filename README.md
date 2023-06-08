# Unsupervised Machine Learning Challenge

### Prepare the Data
- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
- Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

<img width="1660" alt="Screenshot 2023-06-08 at 7 01 23 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/692d5321-a537-41db-90d9-e1754873b5e2">

### Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:

- Create a list with the number of k values from 1 to 11.
- Create an empty list to store the inertia values.
- Create a for loop to compute the inertia with each possible value of k.
- Create a dictionary with the data to plot the elbow curve.
- Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

<img width="935" alt="Screenshot 2023-06-08 at 7 29 38 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/05c9dd27-64cd-4e23-b4b8-ff6998051999">

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

- Initialize the K-means model with the best value for k.
- Fit the K-means model using the original scaled DataFrame.
- Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
- Create a copy of the original data and add a new column with the predicted clusters.
- Create a scatter plot using hvPlot as follows:
  - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

<img width="791" alt="Screenshot 2023-06-08 at 7 13 32 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/8703538b-0a98-47ee-b4ad-3229a7816ade">

## Optimize Clusters with Principal Component Analysis
- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
- Retrieve the explained variance to determine how much information can be attributed to each principal component
- Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

<img width="515" alt="Screenshot 2023-06-08 at 7 19 46 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/b7c052ad-fdd3-49f9-97d8-7e3d74eb9383">

### Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k using the following steps:

- Create a list with the number of k-values from 1 to 11.
- Create an empty list to store the inertia values.
- Create a for loop to compute the inertia with each possible value of k.
- Create a dictionary with the data to plot the Elbow curve.
- Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

<img width="798" alt="Screenshot 2023-06-08 at 7 23 01 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/750ade36-f4f4-4edb-a66d-a5b690745e09">

### Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

- Initialize the K-means model with the best value for k.
- Fit the K-means model using the PCA data.
- Predict the clusters to group the cryptocurrencies using the PCA data.
- Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
- Create a scatter plot using hvPlot as follows:
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

<img width="798" alt="Screenshot 2023-06-08 at 7 27 21 PM" src="https://github.com/margaretkhendre/Crypto-Clustering-vs-Unsupervised-Machine-Learning-Challenge/assets/121995835/8573e8c6-6872-431d-8b10-f6ff085076e1">


