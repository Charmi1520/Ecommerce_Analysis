# Ecommerce Customer Behaviour Analysis

In this project, we will use unsupervised machine learning to categorize clients based on features of their purchase behavior. Predictive marketing may help businesses by finding clients that have similar demands or respond similarly to particular marketing activity. Furthermore, owing to our research, we can undoubtedly help business in determining the suitable categories to direct their targeted marketing campaigns.
**PHASES OF PROCESS FOLLOWED**
BUISINESS UNDERSTANDING
DATA UNDERSTANDING
DATA PREPARATION
MODELING:K-MEANS
MODELING:PRINCIPAL COMPONENT ANALYSIS(PCA)


*BUSINESS UNDERSTANDING*
Hunter's e-grocery is a well-known new generation lifestyle brand. That has a brand presence in ten countries and is continually seeking for new methods to better and anticipate the demands of their customers. Black swan events such as Covid-19, the Ukraine crisis, and the gas scarcity have all had an influence on the purchasing behaviour of clients. Therefore, using an unsupervised machine learning model and Principal component analysis (PCA) for dimensionality reduction, We will develop a business values proposition for predictive marketing in order to target our customers based on features of their purchasing behavior.

*DATA UNDERSTANDING*
The dataset consists of 2019501 Rows & 12 Columns which are as follows :

order_id – (A unique number to identity the order)
user_id - (A unique number to identify the user)
order_number – (Number of the order)
order_dow – (Day of the Week the order was made)
order_hour_of_day – (Time of the order)
days_since_prior_order - (History of the order)
product_id – (Id of the product)
add_to_cart_order – (Number of items added to cart)
reordered – (If the reorder took place)
department_id - (Unique number allocated to each department)
department – (Names of the departments)
product_name – (Name of the products)

Steps to further understand the data:

Importing packages
Loading data
Get information on the data
Conducting summary statistics
Taking care of Null values
Converting data types

**K-MEANS MODELING**

K-Means Clustering:
K-means clustering is an unsupervised learning algorithm that divides a dataset into k clusters, where k is the number of clusters specified by the researcher. The goal of the algorithm is to minimize the sum of squared distances between the points in a cluster and the centroid of the cluster.

Here is an example of how K-means clustering might work:

Suppose we have a dataset with two features (x and y) and we want to use K-means to divide the data into two clusters. We start by randomly initializing two points (centroids) in the data. We then assign each data point to the cluster corresponding to the nearest centroid. Once all of the points have been assigned to a cluster, we compute the new centroids for each cluster by taking the mean of all of the points in the cluster. We then re-assign each data point to the cluster corresponding to the nearest centroid. This process is repeated until the centroids stop moving or the assignment of points to clusters stops changing.

Therefore, the following are the methodological steps we will be taking to build our model:

First step we will be training & experimenting K-means with 6 clusters (testing version)
Second step we will try to run the K-means on a rang of 2 -10 clusters (to find optimal number of cluster)
Creat Scree plot to visualize the inertia using Elbow method (for visualization)

**PCA MODELING**
PCA:
Principal component analysis (PCA) is a statistical technique that is used to analyze the patterns in data. It involves finding a set of directions, or "principal components," that capture as much of the variation in the data as possible. These principal components can be visualized as lines or planes in the data, and are typically chosen so that they are mutually orthogonal (i.e., perpendicular to one another).

One way to visualize PCA is to plot the data in a scatterplot, with the principal components as the axes. This can help to reveal patterns in the data that are not immediately apparent when looking at the raw data. For example, if the data points form a clear cluster in the scatterplot, this may indicate that there is some underlying structure to the data that can be captured by the principal components.

Another way to visualize PCA is to plot the data in a lower-dimensional space, such as a 2D or 3D plot. This can be particularly useful when dealing with high-dimensional data, as it can be difficult to visualize patterns in data with more than 3 dimensions. In this case, the principal components can be used to "project" the data onto a lower-dimensional space, allowing the patterns in the data to be more easily visualized.

Therefore, the following are the methodological steps we will be taking to plot PCA in 2D:

Running Principal Component Analysis (PCA) to visualize & improve results for 5 clusters
Identifying the "best" number of components
Running PCA again with 9 components
Finally re-running K-means with 5 clusters & PCA with 9 components
Re-running K-means with 5 cluster
