## Worked on 3 Different Projects of Clustering as Follows:

# Cluster Analysis on Global Development Measurement Dataset

## Business Objective

The goal of this project is to perform clustering on a global development measurement dataset. By clustering countries based on their economic and development metrics, we aim to identify groups of countries with similar characteristics. This can help in understanding global development trends, identifying potential areas of improvement, and guiding policy or investment decisions.

## Dataset Details

The dataset contains important economic and development metrics for various countries across the globe, including:

- **Birth Rate**
- **Business Tax Rate**
- **CO2 Emissions**
- **Country**
- **Days to Start a Business (dtos_business)**
- **Ease of Doing Business**
- **Energy Usage**
- **GDP**
- **Healthcare Expenditure (% of GDP)**
- **Healthcare Expenditure per Capita**
- **Hours to Do Tax**
- **Infant Mortality Rate**
- **Internet Usage**
- **Lending Interest Rate**
- **Life Expectancy (Female)**
- **Life Expectancy (Male)**
- **Mobile Phone Usage**
- **Number of Records**
- **Population (Age Groups: 0-14, 15-64, 65+)**
- **Urban Population**
- **Tourism (Inbound and Outbound)**

### Key Observations from the Dataset:
- **Positive Correlations**: 
  - Birth Rate and Population (0-14 years)
  - Birth Rate and Infant Mortality Rate
  - CO2 Emissions and Energy Usage
  - Life Expectancy (Male) and Life Expectancy (Female)
  
- **Negative Correlations**:
  - Birth Rate and Population (15-64 years)

## Clustering Models and Methodology

We have implemented and evaluated three popular clustering algorithms: **Hierarchical Clustering**, **K-Means Clustering**, and **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**.

### 1. **Hierarchical Clustering**:
   - The **Agglomerative Clustering** model was used with 4 clusters as the optimal number.
   - **Silhouette Score**: 0.27925 (indicating moderate cluster separation)
   - **Number of iterations**: 8
   - **Optimal Number of Clusters**: 4

### 2. **K-Means Clustering**:
   - The optimal number of clusters was found to be **2**.
   - **Silhouette Score**: 0.385 (indicating good clustering performance)
   - **Number of iterations**: 9
   - **Optimal Number of Clusters**: 2

### 3. **DBSCAN**:
   - The optimal **epsilon** (neighborhood size) was determined to be **1.2** based on the k-distance graph.
   - **Silhouette Score**: 0.54 (highest among the three models, indicating the best clustering performance)
   - **Minimum Samples**: 35
   - **Number of iterations**: 85

## Model Evaluation

We used three evaluation metrics to assess the performance of the clustering models:

1. **Silhouette Score**:
   - Measures how well an observation is clustered.
   - Ranges from -1 to 1, where 1 indicates well-separated clusters and -1 indicates poor clustering.
   
2. **Calinski-Harabasz Index**:
   - Measures the ratio of between-cluster dispersion to within-cluster dispersion.
   - A higher value indicates better clustering.

3. **Davies-Bouldin Index**:
   - Measures the average similarity of each cluster with its most similar cluster.
   - A lower value indicates better clustering.

### Evaluation Results:

| Model                | Silhouette Score | Calinski-Harabasz Score | Davies-Bouldin Index |
|----------------------|------------------|-------------------------|----------------------|
| **Hierarchical**      | 0.27925          | 746.24                  | 1.36                 |
| **K-Means**           | 0.385            | 890.25                  | 1.32                 |
| **DBSCAN**            | 0.54             | 84.14                   | 0.53                 |

### Conclusion:
- **DBSCAN** outperforms the other two models with the highest **Silhouette Score** (0.54) and the lowest **Davies-Bouldin Index** (0.53). This indicates that DBSCAN is the best model for clustering the global development data, as it achieves well-separated and dense clusters.
- **K-Means** follows closely behind, performing well with a **Silhouette Score** of 0.385.
- **Hierarchical Clustering** offers the least favorable results with a **Silhouette Score** of 0.27925.

## Deployment

The final clustering model (DBSCAN) will be deployed using **Streamlit** (or **Flask**, depending on the framework you choose). The web application will allow users to interact with the dataset and visualize the clusters. 

To run the deployment:

1. Clone the repository:
   ```bash
   https://github.com/shubhangidoltade/Clustering-Algorithm/blob/main/Clustering%20Project.ipynb
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   # Crime Data Clustering (Hierarchical, KMeans, DBSCAN)

## Project Overview

The objective of this project is to perform clustering on a crime dataset for different places in the United States. We will apply three popular clustering algorithms — **Hierarchical Clustering**, **K-Means**, and **DBSCAN** — to group the data points based on the rates of crime in various locations. By the end of this project, we aim to identify the number of clusters formed by each algorithm and draw meaningful inferences from them.

## Data Description

The dataset contains information about the crime rates in different locations across the United States. The dataset has the following variables:

- **Murder**: Murder rates in different places.
- **Assault**: Assault rates in different places.
- **UrbanPop**: Percentage of urban population in different places.
- **Rape**: Rape rates in different places.

## Problem Statement

Perform clustering (Hierarchical, KMeans, and DBSCAN) on the crime data to identify the number of clusters formed. Based on the clustering results, draw inferences regarding crime patterns across different regions.

### Steps:
1. **Exploratory Data Analysis (EDA)**
2. **Hierarchical Clustering** (using Dendrogram to identify the optimal number of clusters)
3. **K-Means Clustering** (identifying the optimal number of clusters using the Elbow method)
4. **DBSCAN Clustering** (tuning epsilon and minimum samples for optimal results)

## Exploratory Data Analysis (EDA)

Before performing clustering, conducted a basic EDA on the dataset to check for null values, data distribution, correlations between variables, and any other observations.

### Key EDA Tasks:
- Handle missing values (if any).
- Analyze statistical summary and distribution of variables.
- Visualize pairwise correlations (using heatmaps).
- Check for outliers and address them if necessary.
  
## Clustering Methodologies Used

### 1. **Hierarchical Clustering**

Performed agglomerative clustering and visualized the results using a dendrogram to identify the optimal number of clusters.

### 2. **K-Means Clustering**

K-Means is a partition-based clustering algorithm. Determined the optimal number of clusters using the **Elbow Method** 

### 3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**

Applied DBSCAN to identify arbitrarily shaped clusters and handled outliers.
- **Epsilon (ε)**: The maximum distance between two samples to be considered as neighbors.
- **MinPts (minimum number of points)**: The minimum number of points to form a dense region.
- Used **Epsilon (ε)** method in this project to determine number of clusters.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Crime Data Clustering (Hierarchical, KMeans, DBSCAN)

## Project Overview

The objective of this project is to perform clustering on a dataset of passengers from an airline's frequent flyer program. By applying three popular clustering algorithms — Hierarchical Clustering, K-Means Clustering, and DBSCAN — the goal is to identify clusters of passengers with similar characteristics. These clusters can be used to tailor marketing and loyalty programs, segment customers for targeted offers, and improve customer engagement.
## Data Description
The dataset EastWestAirlines contains information on frequent flyers of an airline. For each passenger, the dataset includes various features that describe their behavior, mileage history, and transaction activities. The features are as follows:

- **ID**: Unique ID of each passenger.
- **Balance**: Number of miles eligible for award travel.
- **Qual_mile**: Number of miles counted as qualifying for Topflight status.
- **cc1_miles**: Number of miles earned with frequent flyer credit card in the past 12 months.
- **cc2_miles**: Number of miles earned with Rewards credit card in the past 12 months.
- **cc3_miles**: Number of miles earned with Small Business credit card in the past 12 months.
- **Bonus_miles**: Number of miles earned from non-flight bonus transactions in the past 12 months.
- **Bonus_trans**: Number of non-flight bonus transactions in the past 12 months.
- **Flight_miles_12mo**: Number of flight miles in the past 12 months.
- **Flight_trans_12**: Number of flight transactions in the past 12 months.
- **Days_since_enrolled**: Number of days since the passenger enrolled in the frequent flyer program.
- **Award**: Whether the person had an award flight (free flight) or not (binary value).
- 
## Problem Statement

Perform clustering (Hierarchical, KMeans, and DBSCAN) on the airlines data to identify segments of passengers. Analyze the clusters formed by each algorithm and draw meaningful inferences to help the airline tailor their marketing and loyalty programs effectively.
### Steps:
1. **Exploratory Data Analysis (EDA)**
2. **Hierarchical Clustering** (using Dendrogram to identify the optimal number of clusters)
3. **K-Means Clustering** (identifying the optimal number of clusters using the Elbow method)
4. **DBSCAN Clustering** (tuning epsilon and minimum samples for optimal results)

## Exploratory Data Analysis (EDA)

Before performing clustering, conducted a basic EDA on the dataset to check for null values, data distribution, correlations between variables, and any other observations.

### Key EDA Tasks:
- Handle missing values (if any).
- Analyze statistical summary and distribution of variables.
- Visualize pairwise correlations (using heatmaps).
- Check for outliers and address them if necessary.
  
## Clustering Methodologies Used

### 1. **Hierarchical Clustering**

Performed agglomerative clustering and visualized the results using a dendrogram to identify the optimal number of clusters.

### 2. **K-Means Clustering**

K-Means is a partition-based clustering algorithm. Determined the optimal number of clusters using the **Elbow Method** 

### 3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**

Applied DBSCAN to identify arbitrarily shaped clusters and handled outliers.
- **Epsilon (ε)**: The maximum distance between two samples to be considered as neighbors.
- **MinPts (minimum number of points)**: The minimum number of points to form a dense region.
- Used **Epsilon (ε)** method in this project to determine number of clusters.





  
