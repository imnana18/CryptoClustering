# CryptoClustering Project 🚀💰

## Project Overview

The main goal of this project is to utilize both `Python` and `unsupervised learning techniques` to predict the influence of 24-hour or 7-day price changes on cryptocurrencies. The following sections provide a comprehensive overview of the steps taken to achieve the project's objectives.

## Project Map

- Reference `Crypto_Clustering.ipynb` in 📁`Unsolved` for full code, visualizations, & reflection.
- CSV data is stored as `crypto_market_data.csv` in 📁`Resources`.
- Note that `hvPlot` visualizations fail to load in GitHub but can be viewed in `Visual Studio Code`. Screenshots of the graphs can also be referenced in this README section.

## Project Files

Downloaded essential files from the [Module 19 Challenge files](https://static.bc-edx.com/data/dl-1-2/m19/lms/starter/Starter_Code.zip).

## Data Preparation and Exploration

- Loaded the cryptocurrency market data from `crypto_market_data.csv` into a DataFrame.
- Conducted a comprehensive analysis of summary statistics and plotted the data for inspection.

  ![Screenshot 2024-03-12 at 17 21 20](https://github.com/imnana18/CryptoClustering/assets/147445115/6ced2a9a-157d-4d0b-991b-6385e89295a8)


## Standardization for Consistency

- Utilized `scikit-learn's StandardScaler() module` to normalize the dataset, ensuring consistent data scales.
- Created a DataFrame with the scaled data, setting "coin_id" as the index.

## Determining Optimal Clustering (Original Scaled DataFrame)

- Applied the `elbow method` to discern the most suitable value for `k` (number of clusters):
   
   ![Screenshot 2024-03-12 at 17 21 01](https://github.com/imnana18/CryptoClustering/assets/147445115/4bb4e8ee-1648-43a8-a75c-4b39e51c4ee0)
   

## K-means Clustering (Original Scaled Data)

- Initialized the `K-means model` with the determined optimal value for `k`.
- Fitted the `K-means model` to the original scaled DataFrame.
- Predicted clusters and created scatter plot using `hvPlot`:

   ![Screenshot 2024-03-12 at 17 20 44](https://github.com/imnana18/CryptoClustering/assets/147445115/1b8840b7-3aa0-46ea-9609-c6b01b2a71a6)


## Principal Component Analysis (PCA)

- Conducted `Principal Component Analysis` on the original scaled DataFrame, condensing features to three principal components.
- Found the `cumulative explained variance` of the three principal components.
- Constructed a new DataFrame with PCA data, "coin_id" serving as the index.

## Identifying Optimal Clustering (PCA Data)

- Utilized the `elbow method` on PCA data to identify optimal value for `k`:
   
   ![Screenshot 2024-03-12 at 17 20 18](https://github.com/imnana18/CryptoClustering/assets/147445115/3adf42fd-56e7-4225-aa83-00289efd5807)


## K-means Clustering (PCA Data)

- Initialized the `K-means model` with the determined optimal value for `k`.
- Executed model fitting using the PCA data.
- Predicted clusters and created scatter plot using `hvPlot`:

   ![Screenshot 2024-03-12 at 17 19 57](https://github.com/imnana18/CryptoClustering/assets/147445115/f2736994-e9b7-4214-81aa-d0ed0662fb75)


## Original vs. PCA Data Comparison 

Created composite plots to compare both elbow and clustering `hvPlots` of `original vs. PCA data`:

![Screenshot 2024-03-12 at 17 19 36](https://github.com/imnana18/CryptoClustering/assets/147445115/0bf2d85f-4074-4abd-9407-8d79972fa73e)

![Screenshot 2024-03-12 at 17 19 07](https://github.com/imnana18/CryptoClustering/assets/147445115/873a176e-349c-4177-976c-ee6161fd0df7)

## References

Data for this dataset was generated by edX Boot Camps LLC and is intended for educational purposes only.
