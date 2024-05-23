# Workshop Incident Analysis/Prediction

## About
**Where**: Workshop                       
**Who**: Superior                                 
**What**: The purpose of this project is to predict individual technician risk percentage. Thus, superior able to select/allocate technician to the task based on their risk percentage. 
For detailed walkthrough, please view the source code in order from:
- [Data Preparation](https://github.com/TanGuiShan/Safety/blob/main/Safety_Data%20Preparation.ipynb)
- [Data Analysis](https://github.com/TanGuiShan/Safety/blob/main/Safety_Data%20Analysis.ipynb)

## Explanation of Key Steps
### Data Preprocessing
- Load the dataset and convert the 'Date' column to datetime format.
- Select numerical features for scaling.
- Standardize the features using `StandardScaler`.

### Data Visualization
- Visualize the distributions of features using count plots and box plots.
- Use pair plots to visualize relationships between features.

### Clustering
- Apply KMeans clustering to the scaled data.
- Calculate distances of each data point to its cluster centroid and score the data points.

### Clustering Evaluation
- Compute the silhouette score, Davies-Bouldin Index, and Mean Squared Error (MSE) to evaluate clustering performance.
- Perform robustness testing by running the clustering multiple times with different random states and subsampling.

### Principal Component Analysis (PCA)
- Use PCA to reduce the dimensionality of the data for visualization.
- Visualize clusters in 2D and 3D using PCA.

### Risk Scoring (Not perfect still editing)
- Calculate risk weights for features using PCA loadings.
- Compute individual feature scores and aggregate them to calculate the total risk score.
- Normalize the total risk score to a range of 0-100.

### Anomaly Detection
- Set an anomaly threshold based on distances to cluster centroids.
- Flag data points as anomalies if their distance exceeds the threshold.
- Provide explanations for why each anomaly was detected.

### New Data Point Analysis
- Functions to preprocess new data points, check for anomalies, and score the new data points.
- Example usage to input new data points interactively.

## Results
- The analysis provides visualizations, clustering results, risk scores, and anomaly detection outputs.
- The results help identify patterns and potential anomalies in the dataset.


