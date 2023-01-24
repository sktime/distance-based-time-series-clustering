# Distance Based Time Series Clustering

Repository to support the paper https://arxiv.org/abs/2205.15181

this repo is a work in progress, we will tidy it up in due course

Abstract

Time series clustering is the act of grouping time series data without recourse to a label. Algorithms that cluster time series can be classified into two groups: those that employ a time series specific distance measure; and those that and cluster based on these. Both approaches usually rely on traditional clustering algorithms such as k-means. Our focus is on distance based time series that employ elastic distance measures, i.e. distances that perform some kind of realignment whilst measuring distance. We describe nine commonly used elastic distance measures and compare their performance with k-means and k-medoids clustering. Our findings are surprising. With a maximum warping window of 20\%, dynamic time warping (DTW), performs worse than Euclidean distance with $k$-means on the UCR time series archive. Using a 5\% window or tuning the window improves DTW performance, but it is still not significantly different to Euclidean distance with k-means. 

We find that using k-medoids rather than k-means improves the clusterings for all eight elastic distance measures, including DTW. However, DTW with k-medoids is not significantly better on average than Euclidean distance with k-medoids on the UCR archive problems. Generally, distance measures that employ editing in conjunction with warping perform better, and one distance measure, the move-split-merge (MSM) method, is the best performing measure of this study. We also compare to clustering with DTW using barycentre averaging (DBA). We find that DBA does improve DTW k-means, but that the standard DBA is still worse than using MSM with k-medoids, and is much slower. MSM is less well known than DTW, and our conclusion is that MSM with k-medoids should be considered as a good alternative to DTW for clustering time series with elastic distance measures. We provide implementations, extensive results and guidance on reproducing results on the associated GitHub repository.
