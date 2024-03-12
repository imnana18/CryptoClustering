# CryptoClustering Project

## Project Overview

This project was initiated to leverage Python and unsupervised learning techniques, aiming to predict the influence of 24-hour or 7-day price changes on cryptocurrencies. The following sections provide a comprehensive overview of the systematic steps taken to achieve the project's objectives.

Note that hvplot visualizations fail to load in GitHub but can be viewed in Visual Studio Code. Screenshots of the graphs can also be referenced in this README section.

## Project Files

Downloaded essential files from the [Module 19 Challenge files]([#](https://static.bc-edx.com/data/dl-1-2/m19/lms/starter/Starter_Code.zip)) external link.

## Data Preparation and Exploration

1. Renamed the primary notebook, Crypto_Clustering_starter_code.ipynb, to a more concise Crypto_Clustering.ipynb.
2. Loaded the cryptocurrency market data from crypto_market_data.csv into a DataFrame.
3. Conducted a comprehensive analysis of summary statistics and visually inspected the dataset to extract insights into its intrinsic structure.

## Standardization for Consistency

1. Employed scikit-learn's StandardScaler() module to normalize the dataset, ensuring consistent data scales.
2. Created a refined DataFrame with the scaled data, setting "coin_id" as the index.

## Determining Optimal Clustering (Original Scaled DataFrame)

1. Applied the elbow method to discern the most suitable value for k (number of clusters):
   
   ![Screenshot 2024-03-12 at 17 21 01](https://github.com/imnana18/CryptoClustering/assets/147445115/4bb4e8ee-1648-43a8-a75c-4b39e51c4ee0)

3. Found optimal value of k as 4. 

## K-means Clustering (Original Scaled Data)

1. Initialized the K-means model with the determined optimal value for k.
2. Fitted the K-means model to the original scaled DataFrame.
3. Predicted clusters and crafted a visually appealing scatter plot using hvPlot:

   ![Screenshot 2024-03-12 at 17 20 44](https://github.com/imnana18/CryptoClustering/assets/147445115/1b8840b7-3aa0-46ea-9609-c6b01b2a71a6)


## Principal Component Analysis (PCA)

1. Conducted Principal Component Analysis on the original scaled DataFrame, condensing features to three principal components.
2. Explored the explained variance to ascertain the information encapsulated in each principal component.
3. Found the cumulative explained variance of the three principal components.
4. Constructed a refined DataFrame with PCA data, with "coin_id" serving as the index.

## Identifying Optimal Clustering (PCA Data)

1. Leveraged the elbow method on the PCA data to pinpoint the optimal value for k:
   
   ![Screenshot 2024-03-12 at 17 20 18](https://github.com/imnana18/CryptoClustering/assets/147445115/3adf42fd-56e7-4225-aa83-00289efd5807)


## K-means Clustering (PCA Data)

1. Instantiated the K-means model with the determined optimal value for k.
2. Executed model fitting using the PCA data.
3. Predicted clusters and adorned the findings with an informative scatter plot using hvPlot:

   ![Screenshot 2024-03-12 at 17 19 57](https://github.com/imnana18/CryptoClustering/assets/147445115/f2736994-e9b7-4214-81aa-d0ed0662fb75)


## Insightful Reflection

Created composite plots to compare hvPlots of original vs. PCA data:

![Screenshot 2024-03-12 at 17 19 36](https://github.com/imnana18/CryptoClustering/assets/147445115/0bf2d85f-4074-4abd-9407-8d79972fa73e)

![Screenshot 2024-03-12 at 17 19 07](https://github.com/imnana18/CryptoClustering/assets/147445115/873a176e-349c-4177-976c-ee6161fd0df7)


Answered the following question for reflection: Based on visually analyzing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?

Please refer to `Crypto_Clustering.ipynb` for detailed code, analysis, visualizations, and summary. 
