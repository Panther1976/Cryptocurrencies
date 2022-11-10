# Crytocurrencies

## Overview: Clustering Crypto

### Deliverable 1: Preprocessing the Data for PCA

<img width="338" alt="CryptoD1" src="https://user-images.githubusercontent.com/106631875/200981457-65fb7b1f-cb1d-4c01-8089-5a27ee3bb4fb.png">

The picture above is a snapshot of our original dataset. In order to preprocess the data, the following was done:
- Kept only the cryptocurrencies that were being traded which meant to retain all rows where the IsTrading Column was set to True.
- The IsTrading Column was then dropped.
- Rows with at least 1 null value were dropped.
- Kept only rows where coines are mined ie 'totalCoinsMined' is greater than zero.
- A new DataFrame was created that held only the cryptocurrencies names (CoinName) so that the CoinName column could be dropped but the DataFrame referenced later
- The CoinName column was dropped since it would not be used in the clustering

<img width="244" alt="CryptoD1_1" src="https://user-images.githubusercontent.com/106631875/200983380-9ee2a361-4662-4b82-9c36-01a7ecfda37c.png">

The picture above captures how the data was preprocessed prior to using pd.get_dummies()

-  pd.get_dummies() was used for the Algorithm and ProofType columns to convert the text to variables

### Deliverable 2: Reducing Data Dimensions Using PCA

In deliverable 2 we take the 532 rows and 98 columns that we were left with after preprocessing steps in Deliverable 1 and we use Principal Component Analysis (PCA) to 
reduce the data deminsions to 3 components as shown below. Using PCA transforms our data into 532 rows and 3 columns.

<img width="145" alt="CryptoD2" src="https://user-images.githubusercontent.com/106631875/200985155-3ff7ec39-f23b-4314-8f29-58498e65ffcb.png">

### Deliverable 3: Clustering Cryptocurrencies using K-Means

- Finding the Best Value for k Using the Elbow Curve

In the picture below you can clearly see that the "elbow" of the curve is at 4. We'll use that information and run K-means with k=4.

<img width="347" alt="CryptoD3_1" src="https://user-images.githubusercontent.com/106631875/200991050-6542ceed-3ee7-4596-be31-411750b8e062.png">

- Running K-Means with k=4 provides the array with the following predictions below:

<img width="293" alt="CryptoD3_2" src="https://user-images.githubusercontent.com/106631875/200991830-888f7ad7-7506-46dd-8714-692e1e2b0347.png">

- We create a new DataFrame with the predicted clusters and cryptocurrency features, combine our DataFrames and add back in the CoinName column that was dropped above. 
- Our results are shown below:

<img width="462" alt="CryptoD3_3" src="https://user-images.githubusercontent.com/106631875/200992425-28e59a6b-8275-472d-87ab-ea9f1b76a92a.png">


### Deliverable 4: Visualizing Cryptocurrencies Results with a 3D Scatter with Clusters

The picture below is a 3D-scatter plot with the PCA data and clusters.

<img width="366" alt="CryptoD4_1" src="https://user-images.githubusercontent.com/106631875/200994477-a088811c-8902-4e6b-9cfc-b1a02b428d65.png">

The picture below is a table of the tradable cryptocurrencies with column headers of CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined and Class.

<img width="352" alt="CryptoD4_2" src="https://user-images.githubusercontent.com/106631875/200994522-f18d3abe-9c78-43e6-9f13-1c55dcebc13d.png">

The picture below is the scatter plot using x as TotalCoinsMined and y as Total CoinSupply which gives us insight to the supply and demand and potential investment opportunity.

<img width="358" alt="CryptoD4_4" src="https://user-images.githubusercontent.com/106631875/200994558-d167feed-9f92-40a1-8d9b-e40417ace756.png">

