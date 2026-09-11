




🛍️ Mall Customer Segmentation using K-Means Clustering

📌 Project Overview
This project performs customer segmentation on the Mall Customers dataset using K-Means Clustering, an unsupervised machine learning algorithm.

The goal is to divide mall customers into meaningful groups based mainly on their Annual Income and Spending Score, so that the business can create more targeted marketing strategies.

The notebook contains a complete workflow including:

Data loading and understanding

Data cleaning and validation

Exploratory Data Analysis (EDA)

Feature engineering

Feature scaling

K-Means clustering

Optimal cluster selection

Cluster visualization

Cluster profiling

Hierarchical Clustering comparison

DBSCAN comparison

PCA visualization

Model evaluation

Business insights and recommendations

🎯 Business Problem
A mall wants to understand its customers better instead of treating every customer in the same way.

The objective is to identify groups of customers with similar spending behavior and income levels. These customer segments can then be used for:

Targeted marketing campaigns

Personalized offers

Customer retention

Premium product promotion

Discount and loyalty strategies

Better business decision-making

This is an unsupervised learning problem because the dataset does not contain predefined customer segment labels.

📊 Dataset
The project uses the Mall_Customers.csv dataset.

Dataset Information
Rows: 200

Columns: 5

Missing Values: 0

Duplicate Rows: 0

Features
Column	Description
CustomerID	Unique customer identifier
Gender	Male / Female
Age	Customer age
Annual Income (k$)	Annual income in thousands of dollars
Spending Score (1-100)	Mall-assigned spending behavior score
🛠️ Technologies & Libraries
Programming Language
Python

Libraries
Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

SciPy

Machine Learning Techniques
K-Means Clustering

Agglomerative / Hierarchical Clustering

DBSCAN

PCA (Principal Component Analysis)

StandardScaler

🔍 Project Workflow
1. Data Loading
The dataset is loaded using Pandas.

2. Data Understanding
The notebook checks:

First and last rows

Dataset shape

Column names

Data types

Statistical summaries

Unique values

Gender categories

3. Data Quality Check
The dataset is checked for:

Missing values

Duplicate rows

Possible outliers

The notebook found 0 missing values and 0 duplicate rows.

4. Feature Engineering
The original income and spending-score column names are simplified for easier coding.

Gender is also encoded numerically:

Male → 0

Female → 1

5. Exploratory Data Analysis
Several visualizations are created, including:

Gender distribution

Age distribution

Income distribution

Spending Score distribution

Correlation heatmap

Pairplot

Age vs Income

Age vs Spending Score

Income vs Spending Score

Gender-wise average income and spending score

Outlier analysis

6. Feature Selection
For the main K-Means segmentation, the project focuses on customer behavioral features, especially:

Annual Income

Spending Score

7. Feature Scaling
StandardScaler is used before clustering so that features are placed on a comparable scale.

8. Finding the Optimal Number of Clusters
Two methods are used:

Elbow Method
The Elbow Method is used to analyze WCSS (Within-Cluster Sum of Squares).

Silhouette Score
The Silhouette Score is calculated for K values from 2 to 10.

The highest score in the notebook is:

K = 5 → Silhouette Score = 0.5547

Both the Elbow Method and Silhouette analysis support choosing:

K = 5

9. Final K-Means Model
A final K-Means model is trained with:

Number of clusters: 5

Initialization: k-means++

random_state = 42

n_init = 10

10. Cluster Visualization
The notebook visualizes the resulting customer groups using:

2D scatter plots

Cluster centroids

3D visualization

Silhouette plots

11. Cluster Profiling
The customer groups are interpreted using income, spending behavior, age, and other available information.

The project identifies five business-friendly segment types:

Target Customers – High Income, High Spending

Careful Spenders – High Income, Low Spending

Impulsive Spenders – Low Income, High Spending

Budget Customers – Low Income, Low Spending

Average Customers – Medium Income, Medium Spending

Note: K-Means cluster numbers are arbitrary and can change between runs. The business segment name should be interpreted using the cluster profile rather than the numeric cluster ID alone.

📈 Model Evaluation
The final K-Means model with K = 5 achieved:

Metric	Result
Inertia (WCSS)	65.57
Silhouette Score	0.5547
Davies-Bouldin Index	0.5722
Metric Meaning
Inertia (WCSS): Measures how compact the clusters are. Lower is generally better.

Silhouette Score: Measures how well-separated the clusters are. Higher is better; the score ranges from -1 to 1.

Davies-Bouldin Index: Measures similarity between clusters. Lower is generally better.

🔄 Additional Clustering Analysis
To validate the K-Means results, the project also compares the data using:

Hierarchical Clustering
Agglomerative Clustering and a dendrogram are used to inspect the natural grouping structure.

DBSCAN
DBSCAN provides another clustering perspective and can identify density-based groups and noise/outliers.

PCA
Principal Component Analysis is used to reduce the feature space to two principal components for visualization.

💡 Business Insights
The identified customer segments can support different marketing strategies.

🎯 Target Customers
High Income + High Spending

Recommended strategies:

Premium product launches

Loyalty programs

Personalized offers

VIP customer benefits

💰 Careful Spenders
High Income + Low Spending

Recommended strategies:

Engagement campaigns

Exclusive previews

Personalized recommendations

Special incentives

⚡ Impulsive Spenders
Low Income + High Spending

Recommended strategies:

Discounts

Flash sales

Installment / EMI options

Limited-time offers

🛒 Budget Customers
Low Income + Low Spending

Recommended strategies:

Value bundles

Affordable products

Discounts

Essential product promotions

👥 Average Customers
Medium Income + Medium Spending

Recommended strategies:

General marketing campaigns

Seasonal offers

Regular promotions

Product recommendations

📁 Project Structure
Mall-Customer-Segmentation/
│
├── Mall_Customer_Segmentation_KMeans_Full.ipynb
├── Mall_Customers.csv
├── Mall_Customers_Clustered.csv
└── README.md
Mall_Customers_Clustered.csv is generated by the notebook after the clustering process.

▶️ How to Run the Project
1. Clone the Repository
git clone <your-repository-link>
2. Open the Project
Open the project folder in:

Jupyter Notebook

JupyterLab

Google Colab

VS Code

3. Install Required Libraries
pip install pandas numpy matplotlib seaborn scikit-learn scipy
4. Run the Notebook
Open:

Mall_Customer_Segmentation_KMeans_Full.ipynb
Run the notebook cells from top to bottom.

📤 Output
The notebook saves the final clustered dataset as:

Mall_Customers_Clustered.csv
This file contains the customer data along with the generated cluster labels and segment names.

📌 Key Results
Dataset contains 200 customers

No missing values were found

No duplicate rows were found

K-Means was selected as the main clustering algorithm

5 customer segments were identified

Elbow Method and Silhouette Score supported K = 5

Final Silhouette Score: 0.5547

The results can be used for targeted marketing and customer strategy

🚀 Future Improvements
Possible extensions of this project include:

Building an interactive Power BI dashboard

Creating a Flask web application for customer segmentation

Adding new customer transaction history

Testing additional clustering algorithms

Automating customer segment assignment

Deploying the model as an API

Adding recommendation and personalization features

👨‍💻 Author

Naresh Yadav

GitHub: https://github.com/nareshyadav1234
