# ✈️ San Francisco Airport Passenger Clustering

## Project Overview

This project analyzes passenger traffic at **San Francisco International Airport (SFO)** and applies **K-Means clustering** to identify groups with similar passenger traffic characteristics.

The project combines exploratory data analysis, passenger traffic visualization, feature preparation, the **Elbow Method**, K-Means clustering, silhouette evaluation, and cluster analysis.

---

## Dataset

The dataset contains passenger traffic statistics from San Francisco International Airport.

- **Rows:** 18,885
- **Columns:** 12

The data includes information such as:

- Activity Period
- Operating Airline
- GEO Summary
- GEO Region
- Activity Type Code
- Price Category Code
- Terminal
- Boarding Area
- Passenger Count

The dataset file is included in this repository.

---

## Project Workflow

1. Load and explore the dataset
2. Check dataset structure and missing values
3. Remove unnecessary columns
4. Analyze passenger traffic patterns
5. Visualize traffic by terminal, geographic region, boarding area, and time
6. Select features for clustering
7. Convert categorical variables into numerical variables
8. Standardize the selected features
9. Apply the Yellowbrick Elbow Method
10. Train a K-Means clustering model
11. Evaluate the clusters using the Silhouette Score
12. Analyze and visualize the final clusters

---

## Passenger Traffic Analysis

The exploratory analysis includes:

- Passenger traffic by terminal and activity type
- Passenger traffic by geographic region and terminal
- Passenger traffic by boarding area
- Passenger traffic over time

These visualizations provide an overview of passenger activity before clustering.

---

## Data Preparation

The following features were selected for clustering:

- **Passenger Count**
- **GEO Summary**
- **Activity Type Code**
- **Price Category Code**

Categorical variables were converted into numerical dummy variables using `pd.get_dummies()`.

The features were standardized using **StandardScaler** before applying K-Means clustering.

---

## Elbow Method

The **Yellowbrick KElbowVisualizer** was used to estimate a suitable number of clusters.

The Elbow Method identified:

**Optimal number of clusters: 6**

This value was used for the final K-Means model.

---

## K-Means Clustering

The final K-Means model was trained using:

- **Number of clusters:** 6
- **Random state:** 42
- **n_init:** 10

Each passenger traffic record was assigned to one of the six clusters.

---

## Cluster Evaluation

The clustering result was evaluated using the **Silhouette Score**.

| Metric | Result |
| --- | ---: |
| Number of Clusters | **6** |
| Silhouette Score | **0.7127** |

The Silhouette Score indicates a clear separation between the clusters for the selected feature representation.

---

## Cluster Analysis

The final analysis compares the clusters using passenger traffic statistics such as:

- Number of records
- Mean passenger count
- Median passenger count
- Total passenger count

The clusters are also visualized to compare passenger traffic patterns over time.

---

## Technologies

- Python
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn
- Yellowbrick
- Jupyter Notebook

---

## Project Structure

**san-francisco-airport-clustering**

- `san_francisco_airport_clustering.ipynb` — Complete clustering analysis
- `air-traffic-passenger-statistics.csv` — Dataset
- `README.md` — Project documentation

---

## Conclusion

This project applies **K-Means clustering** to passenger traffic data from San Francisco International Airport.

The **Yellowbrick Elbow Method** identified **6 clusters** as a suitable solution, and the final clustering model achieved a **Silhouette Score of 0.7127**.

The project presents a simple and structured clustering workflow including exploratory analysis, feature preparation, cluster selection, K-Means modeling, evaluation, and visualization.
