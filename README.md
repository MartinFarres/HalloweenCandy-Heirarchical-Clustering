# Candy Hierarchical Clustering Project

This project explores hierarchical clustering techniques applied to a dataset of candy attributes to identify natural groupings of candies. The analysis includes data preprocessing, hierarchical clustering with different linkage methods, dimensionality reduction using PCA, and a comparison of the clustering results.

## Project Goal

The main goal is to understand the structure within the candy dataset by grouping similar candies together using hierarchical clustering. Additionally, the project investigates the impact of dimensionality reduction with PCA on the clustering results and compares different linkage methods.

## Dataset

The dataset used in this project is `candy-data.csv`, which contains various attributes for a selection of candies, including ingredients (chocolate, fruity, caramel, etc.), characteristics (hard, bar, pluribus), sugar percentage, price percentage, and win percentage.

## Methodology

1.  **Data Loading and Exploration**: The candy data is loaded into a pandas DataFrame. Initial exploration is performed to understand the data structure, data types, and identify any missing values.
2.  **Data Preprocessing**: The 'competitorname' column is dropped as it is not a numerical feature suitable for clustering. The remaining numerical features are scaled using `StandardScaler` to ensure they have a similar range, preventing features with larger values from dominating the clustering process.
3.  **Hierarchical Clustering (without PCA)**: Hierarchical clustering is applied to the scaled data using different linkage methods:
    *   Ward linkage
    *   Single linkage
    *   Complete linkage
    *   Average linkage
4.  **Dimensionality Reduction with PCA**: Principal Component Analysis (PCA) is applied to the scaled data to reduce its dimensionality to 2 components.
5.  **Hierarchical Clustering (with PCA)**: Hierarchical clustering is applied to the PCA-transformed data using the same linkage methods.
6.  **Results Analysis and Comparison**:
    *   Dendrograms are visualized for selected linkage methods (Ward and Average, with and without PCA) to observe the clustering structure.
    *   Silhouette scores are calculated for each clustering result to evaluate the quality of the clusters.
    *   The characteristics of the formed clusters (mean values of attributes within each cluster) are examined and compared for different methods and with/without PCA.

## Key Findings

*   The analysis revealed that different linkage methods can result in varying cluster structures.
*   Applying PCA before hierarchical clustering generally led to higher silhouette scores, suggesting improved cluster separation and cohesion.
*   The Average and Ward linkage methods often produced better clustering results based on the silhouette score in this analysis.
*   The formed clusters represent groups of candies with similar attributes, such as chocolatey bars, fruity hard candies, etc.
*   Comparing these clusters to candies from a different region (like Argentina) would require similar attribute data for those candies and could reveal interesting similarities or differences in candy preferences and characteristics across regions.

## How to Use

This project is implemented as a Python notebook. To run the analysis:

1.  Clone this repository.
2.  Ensure you have the necessary libraries installed (`pandas`, `scikit-learn`, `matplotlib`, `scipy`). 
