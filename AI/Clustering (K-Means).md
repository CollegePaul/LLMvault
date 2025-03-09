### Clustering (K-Means) in AI

Clustering is a type of unsupervised learning technique used in artificial intelligence to group similar data points together into clusters. The goal of clustering is to identify patterns or structures within the data without prior knowledge of the categories or labels.

One of the most popular algorithms for clustering is K-Means. K-Means aims to partition a dataset into 'K' distinct, non-overlapping subsets (clusters) where each data point belongs to the cluster with the nearest mean (centroid). The algorithm works through an iterative process:

1. **Initialization**: Randomly select 'K' points as initial centroids.
2. **Assignment**: Assign each data point to the closest centroid based on Euclidean distance, forming 'K' clusters.
3. **Update**: Recalculate the centroids of the clusters as the mean of all data points assigned to each cluster.
4. **Convergence Check**: Repeat steps 2 and 3 until the centroids do not change significantly or a maximum number of iterations is reached.

### Example in Python

Below is an example using Python with the `scikit-learn` library to perform K-Means clustering on a simple dataset:

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.datasets import make_blobs

# Generate synthetic data
X, y = make_blobs(n_samples=300, centers=4, cluster_std=0.60, random_state=0)

# Visualize the generated data
plt.scatter(X[:, 0], X[:, 1], s=50)
plt.title('Generated Data')
plt.show()

# Apply K-Means clustering
kmeans = KMeans(n_clusters=4)
kmeans.fit(X)

# Get cluster centers and labels
y_kmeans = kmeans.predict(X)
centers = kmeans.cluster_centers_

# Visualize the clusters and their centroids
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50, cmap='viridis')
plt.scatter(centers[:, 0], centers[:, 1], c='red', s=200, alpha=0.75)
plt.title('K-Means Clustering Results')
plt.show()
```

In this example:
- We generate a synthetic dataset using `make_blobs` with 4 clusters.
- We apply K-Means clustering to partition the data into 4 clusters.
- The resulting clusters and their centroids are visualized.

#Clustering (K-Means) #AI