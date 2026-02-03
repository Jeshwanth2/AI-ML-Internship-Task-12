# AI-ML-Internship-Task-12
 KMeans – Customer Segmentation
Mall Customer Segmentation using K-Means Clustering
Overview
This project aims to segment mall customers into distinct groups based on their annual income and spending score. By identifying these customer segments, businesses can tailor marketing strategies, personalize offers, and improve customer engagement.

Dataset
The dataset used is Mall_Customers.csv, containing information about mall customers including:

CustomerID: Unique identifier for each customer.
Gender: Gender of the customer.
Age: Age of the customer.
Annual Income (k$): Annual income of the customer in thousands of dollars.
Spending Score (1-100): A score assigned by the mall based on customer behavior and spending habits (1-100).
Methodology
The customer segmentation was performed using the K-Means clustering algorithm, following these steps:

Data Loading and Inspection: Loaded the Mall_Customers.csv dataset into a pandas DataFrame and inspected the Annual Income (k$) and Spending Score (1-100) columns.
Feature Preparation: The CustomerID column was dropped as it's not relevant for clustering. Annual Income (k$) and Spending Score (1-100) were selected as features and normalized using StandardScaler to ensure balanced distance calculations during clustering.
Optimal K Determination (Elbow Method): K-Means clustering was run for a range of K values (1 to 10) on the scaled data. The inertia (within-cluster sum of squares) was calculated for each K, and an elbow curve was plotted to visually identify the optimal number of clusters, which was determined to be K=5.
K-Means Model Training: A K-Means model was trained using the optimal K value of 5 on the scaled features.
Cluster Assignment and Data Saving: The generated cluster labels were assigned back to the original DataFrame as a new Cluster column. The segmented data was then saved to segmented_mall_customers.csv.
Cluster Visualization: A scatter plot was created to visualize the identified clusters, mapping 'Annual Income (k )′tothex−axisand′SpendingScore(1−100)′tothey−axis,withpointscolor−codedbytheirassignedclusterlabels.7.∗∗ClusterInterpretationandLabeling∗∗:Thecharacteristicsofeachclusterwereanalyzedbasedontheiraverage′AnnualIncome(k )' and 'Spending Score (1-100)'. Descriptive labels were provided for each cluster:
Cluster 0: Standard Customers (Moderate Income, Moderate Spending)
Cluster 1: Target Customers (High-Income, High-Spending)
Cluster 2: Low-Income, High-Spending
Cluster 3: High-Income, Low-Spending
Cluster 4: Low-Income, Low-Spending
Key Findings
Five distinct customer segments were identified, each with unique spending and income patterns:

Standard Customers: Represent a large group with average income and spending.
Target Customers: High-income individuals with high spending scores, representing a prime target for premium products.
Low-Income, High-Spending: Customers with lower income but high spending, potentially impulse buyers or value seekers.
High-Income, Low-Spending: Affluent individuals who do not spend much at the mall, indicating untapped potential.
Low-Income, Low-Spending: Budget-conscious customers with minimal income and spending.
Deliverables
Elbow Plot: Visual representation used to determine the optimal number of clusters.
Cluster Visualization: Scatter plot displaying the five customer segments.
Segmented Dataset CSV: segmented_mall_customers.csv file containing the original data with an added Cluster column.
Conclusion and Next Steps
The customer segmentation provides valuable insights into the mall's customer base. This information can be leveraged to:

Develop targeted marketing campaigns for each segment.
Optimize product placements and store layouts.
Create personalized loyalty programs and promotions.
Identify areas for improving customer engagement, especially for high-income, low-spending customers.
