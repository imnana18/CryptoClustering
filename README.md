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

3. Considered the question: What is the optimal value for k?

## K-means Clustering (Original Scaled Data)

1. Initialized the K-means model with the determined optimal value for k.
2. Fitted the K-means model to the original scaled DataFrame.
3. Predicted clusters and crafted a visually appealing scatter plot using hvPlot.

## Principal Component Analysis (PCA)

1. Conducted Principal Component Analysis on the original scaled DataFrame, condensing features to three principal components.
2. Explored the explained variance to ascertain the information encapsulated in each principal component.
3. Addressed the question: What is the cumulative explained variance of the three principal components?
4. Constructed a refined DataFrame with PCA data, with "coin_id" serving as the index.

## Identifying Optimal Clustering (PCA Data)

1. Leveraged the elbow method on the PCA data to pinpoint the optimal value for k.
2. Reflectively answered the query: What is the most fitting value for k when utilizing PCA data? Does it diverge from the optimal k value obtained with the original data?

## K-means Clustering (PCA Data)

1. Instantiated the K-means model with the determined optimal value for k.
2. Executed model fitting using the PCA data.
3. Predicted clusters and adorned the findings with an informative scatter plot using hvPlot.

## Insightful Reflection

Delved into the impact of using fewer features in the clustering process using K-Means, unraveling the nuanced subtleties within the data.

For a more immersive exploration of the project intricacies and outcomes, please refer to the detailed notebook (`Crypto_Clustering.ipynb`).
