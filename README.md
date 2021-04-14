# Clustering
In Unsupervised Learning we have different type of algorithms such as:

Clustering
Association Rules
Recommendation Engine
PCA
Text mining
NLP

In Clustering we have :

Hierarchial Clustering
K-Means Clustering
DBSCAN Clustering

A) Hierarchial Clustering:-

This is mainly used for Numerical data, it is also called as bottom-up approach. In this, among all the records two records which are having less Euclidean distance are merged in to one cluster and again this cluster inturn with which it is having less euclidean distance that record is merged with the cluster. Now how to calculate distance between 2 clusters or distance between cluster and record ?

 For this we have different methods:

1. Single linkage method : *It will consider minimum distance*
2. Complete linkage method : *It will consider maximum distance*
3. Average linkage method : *It will consider average of all distances*
4. centroid linkage method : *It will consider centroid of records of one cluster and centroid of records of other cluster and now distance between these two centroids is considered.*
Summarization of entire cluster process is done using Dendogram

Advantages :

Best suitable for smaller datasets.
Dendogram gives best understanding of clustered data.

Disadvantages :

It is slower for large datasets.

B) K means Clustering:-

 step 1: K= 3, we can take different values for K, here K=3 so entire data is randomly divided in to 3 parts need not be equal.
 step 2: Centroid computation - calculate centroid for each part.
 step 3: find distance from centroid to all datapoints in each part.
 step 4: Move data point in to nearest centroid.
 step 5: Recompute centroids.
 step 6: Repeat steps from 3 to 5 until there is no need to move data points from one cluster to other cluster.

By using Elbow graph or screw plot we will decide proper K-value.

Advantages:

Partition of data accurately fast
Suitable for larger datasets

Diasadvantages:

If we have outliers, it will give false clusters

C) DBSCAN Clustering :-

There are some disadvantages in Hierarchial clustering and K - means Clustering, among them main disadvantages are that they doesnt perform well with non-spherical shapes of clusters and sensitive to noise or outliers.

To deal with this we have Density Based Spatial Clustering (DBSCAN) :

    -It is mainly used to find outliers and merge them and to deal with non-spherical data
    -Clustering is mainly done based on density of data points (where more number of data points are present).
  
step 1: Mainly we have 2 parameters:
        1. eps
        2. Min points
        
step 2: eps >0 => compulsary

    Suppose eps=2 which means it randomly chooses a point x from that point it draws a circle with radius=2 that is nothing but cluster with eps=2
    
step 3: Min points, to know neighbourhood is dense enough or not we use min points.

        Suppose minpoints = 8, which means neighbourhood has atleast >= 8 data points then it is denser and forms cluster, if < 8 data points then not denser and outliers.
      
step 4: Border points

        In eps neighbourhood that contains less than min points but it belongs to eps neighbourhood of another core point
      
Note:If not core point and not border point then it is noise or outliers
Data used:

Crime Dataset
Airlines Dataset
Programming language:Python

The Codes regarding this Clustering with two different business problems of Crime dataset and Airlines dataset are present in this Repository in detail.
