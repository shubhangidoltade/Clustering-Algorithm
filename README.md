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
  
