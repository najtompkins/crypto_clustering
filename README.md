# Crypto Clustering
Resources found in repo.

## Step 1: Find the best K value with scaled data
  - Scaled the data.
  - Coded the elbow method algorithm to find the best value for k, testing between values 1 and 11.
  - Plotted a line chart of all the inertia values computed with the different values of k.
  - Determined that the best value is 4, with a good argument for 3, depending on what you want out of the data.

## Step 2: Clustered the data with the K-Means value.
  - Initialized the K-means model with the best value (4) for the number of clusters, fit the model, and then predicted the clusters.
  - Visualized the array of clusters.
  - Created a copy of the original data, then added a new column of the predicted clusters.
  - Used hvPlot to visulaize the clusters, creating a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Colors and crypto names added for clarity.

## Step 3: Optimized the Clusters with Principal Component Analysis.
  - Created a PCA model with 3 components requested.
  - Used the PCA model to reduce the features of the standardized data set to three principal components then visualizing the first 5.
  - Calculated the explained variance to determine how much information can be attributed to each principal component.
  - The total explained variance is about 88%.
  - Created a Pandas dataframe with the PCA data and index set from the original dataframe and reviewed it.

## Step 4: Found the Best Value for k by Using the PCA Data.
  - Coded the elbow method algorithm and used the PCA data to find the best value for k.
  - Plotted a line chart of all the inertia values computed with the different values of k.
  - The best value for K is four, like the non-PCA data. It does not differ in any meaningful way.
  - Clustered the Cryptocurrencies with K-means by Using the PCA Data.

## Step 5: Initialized the K-means model with four clusters by using the best value for k.
  - Fit the K-means model by using the PCA data.
  - Predicted the clusters for grouping the cryptocurrencies by using the PCA data, and reviewed the array.
  - Created a copy of the DataFrame with the PCA data, and then added a new column to store the predicted clusters.
  - Used hvPlot tp create a scatter plot by setting x="PC1" and y="PC2". Colors and labels included, the latter as a hover-opver text.
  - Visualized and Compared the Results

## Step 6: Created a composite plot by using hvPlot for both the elbow and scatter plots.
  - Created a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.
  - The impact of using fewer features: The clusters are distributed in a much more comprehensive way, allowing for clear delineations and better understanding of what the clusters represent.
