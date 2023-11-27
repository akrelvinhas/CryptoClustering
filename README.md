# CryptoClustering

**Project Focus:**
Cryptocurrencies, renowned for their price volatility, present an intriguing subject for analysis. This project specifically delves into employing unsupervised learning techniques to anticipate how cryptocurrencies respond to price fluctuations across different time intervals. The methodology encompasses the use of StandardScaler from scikit-learn to normalize the data, leveraging the elbow method to discern the optimal number of clusters (k), and implementing K-means clustering to categorize cryptocurrencies. Additionally, Principal Component Analysis (PCA) is explored to optimize clusters and identify the best value of k for the reduced dataset.

**1. Data Preprocessing:**
This initial phase involved preparing the data for analysis. StandardScaler from scikit-learn was applied to normalize the data extracted from the CSV file. Normalization is pivotal to ensure that features are consistently scaled, preventing any bias in the clustering algorithm.

**2. Finding the Optimal k:**
A critical step in K-means clustering is determining the optimal number of clusters (k). The elbow method was employed for this purpose. This technique involves generating a list of k values, calculating the inertia (within-cluster sum of squares) for each k, and plotting an elbow curve to pinpoint the inflection point where the rate of inertia change slows down. The value of k at this juncture is the optimal choice for clustering.

**3. Clustering with K-means:**
Armed with the optimal k value, cryptocurrencies were clustered using the original scaled data. The K-means model was initialized, fitted using the scaled dataset, predictions were made for each cryptocurrency, and a scatter plot was created for visualization. This step facilitated grouping cryptocurrencies based on their distinctive price change characteristics.

**4. Optimizing Clusters with Principal Component Analysis:**
This phase incorporated Principal Component Analysis (PCA) to reduce the dimensionality of the dataset. PCA aids in identifying the most informative features and reducing computational complexity. The explained variance was also retrieved to understand the contribution of each principal component.

**5. Finding the Best Value for k Using the PCA Data:**
Similar to the previous section, the elbow method was employed to determine the best value for k, but this time using the reduced dataset obtained from PCA. A comparative analysis was conducted to identify the optimal k value from PCA in comparison to the one obtained from the original data.

**6. Clustering with K-means Using the PCA Data:**
With the best k value determined, cryptocurrencies were clustered using the PCA-transformed data. The clustering process mirrored the previous K-means clustering but was applied to the PCA dataset. Visualizations were generated to comprehend the impact of using fewer features on the resulting clusters.
