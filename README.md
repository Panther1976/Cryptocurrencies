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

### Deliverable 3: Clustering Cryptocurrencies using K-Means

- Finding the Best Value for k Using the Elbow Curve

Insert Picture

- Running K-Means with k=4

Insert Picture

### Deliverable 4: Visualizing Cryptocurrencies Results with a 3D Scatter with Clusters

Insert Picture 



# Summary
