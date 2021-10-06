# Hierarchical-Clustering
This is python implementation of hierarchical clustering use dynamic programming (top-down and bottom-up) approach.

## Steps Involved -
 - Start by assigning each item to its own cluster, so that if you have N items, you now have N clusters, each containing just one item. 
 - Find the closest pair of clusters and merge them into a single cluster, so that now you have one less cluster.
 - Compute distances between the new cluster and each of the old clusters.
 - Repeat steps 2 and 3 until all items are clustered into a single cluster of size N.


## Linkages:
Linkages are the distances(distance is directly proportional to similarity) between clusters. As stated in above algorithm, we go on merging the 2 nearest clusters. But the problem here is how to find the distance between 2 clusters?

There are multiple ways to find the clusters:
### Single Linkage:
 - The distance considered is minimum distance between 2 clusters. Minimum distance between 2 datapoints in 2 clusters.

### Centroid Linkage:
 - The distance considered here is, the distance between centroids of two clusters.

### Average Linkage:
 - The distance considered is average of distances between 2 clusters. Average of distances between all the datapoints in 2 clusters.

### Complete Linkage:
 - The distance considered is maximum distance between 2 clusters. Maximum distance between 2 datapoints in 2 clusters.

## Implementation
We use the concept of dynamic programming (Memoization technique) which is also known as Divisive approach to clustering to achieve better time complexity. We will be maintaining the distance matrix which will maintain the distances between all the datapoints present. Thus, if we have "n" number of datapoints our distance matrix will be of order nxn. This matrix will be symmetric matrix. Since we want to merge the two closest datapoints, we find the minimum distance and we will merge the 2 clusters updating the clusters distance from all other datapoints. We repeat the above step until all the datapoints are under one cluster.  

