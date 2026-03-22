# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Choose the number of clusters (K). 2.Randomly initialize K centroids. 3.Assign each data point to the nearest centroid. 4.Recalculate the centroids. Repeat steps 3 and 4 until centroids do not change.
## Program:
```
/*
Pro/*
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]
print(data.head())
kmeans = KMeans(n_clusters=5, random_state=42)
y_kmeans = kmeans.fit_predict(X)


data['Cluster'] = y_kmeans

print("\nClustered Data:")
print(data.head())


plt.figure()
plt.scatter(X[y_kmeans == 0]['Annual Income (k$)'], 
            X[y_kmeans == 0]['Spending Score (1-100)'], label='Cluster 0')

plt.scatter(X[y_kmeans == 1]['Annual Income (k$)'], 
            X[y_kmeans == 1]['Spending Score (1-100)'], label='Cluster 1')

plt.scatter(X[y_kmeans == 2]['Annual Income (k$)'], 
            X[y_kmeans == 2]['Spending Score (1-100)'], label='Cluster 2')

plt.scatter(X[y_kmeans == 3]['Annual Income (k$)'], 
            X[y_kmeans == 3]['Spending Score (1-100)'], label='Cluster 3')

plt.scatter(X[y_kmeans == 4]['Annual Income (k$)'], 
            X[y_kmeans == 4]['Spending Score (1-100)'], label='Cluster 4')

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:,0], 
            kmeans.cluster_centers_[:,1], 
            s=200, label='Centroids')

plt.title("Customer Segmentation using K-Means")
plt.xlabel("Annual Income (k$)")
plt.ylabel("Spending Score (1-100)")
plt.legend()
plt.show()
program to implement the K Means Clustering for Customer Segmentation.
Developed by:ABDUL RAHMAN A R  
RegisterNumber: 25008775 
*/
```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)
<img width="723" height="118" alt="image" src="https://github.com/user-attachments/assets/4a93f557-3a8d-43d9-9354-80c14493344f" />
<img width="736" height="257" alt="image" src="https://github.com/user-attachments/assets/d6ff8346-4ca4-4925-9dd6-858f9bdd6c36" />
<img width="620" height="453" alt="image" src="https://github.com/user-attachments/assets/d3f078c4-16ae-4513-9773-8ca01a0127c0" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
