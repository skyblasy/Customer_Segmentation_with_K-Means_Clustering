# Customer_Segmentation_with_K-Means_Clustering
Customer segmentation analysis segmenting on frequency, recency, and monetary amount. This analysis is done with binning using quantiles and also unsupervised machine learning

# Who are the top performing customers and how can we determine that? 

A fundamental question in marketing is knowing who the target consumer segment is to maximize return on marketing spent. 

This project takes customer data including purchasing frequency, recency, and monetary amount as relevant dimensions and factors segmentation and separates the accounts with two different strategies.

### Binning on a given number of quantiles

This first method is more arbitrary but allows greater discretion on part of management  in defining segments. This is achieved by ranking each customers’ purchase recency, frequency, and monetary amount for a given quantile and then summing those values together to get a value associated with a certain rank of customer; Platinum, Gold, Silver, Bronze. 

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Binned.png)

This approach offers a lot of flexibility in deciding how many groups can be formed. But, for that same reason, that is also a potential pitfall; the categories are arbitrarily chosen, so can it really be certain that the highest segment really represents all the best customers? Or, is the number of segments really the appropriate amount? Could there be more or potentially fewer? Fortunately there is a more organic way to differentiate customers.

### K-means Clustering

K-means clustering is an unsupervised machine learning technique separating observations into clusters/groups  based on the relative distance or “closeness” of their characteristics. In this case, customers that have relatively close similarities in their characteristics would be put into the same cluster and those which are mutually further way would be in a different cluster.

The number of clusters can be chosen arbitrarily; however, a technique which takes the point where inflection occurs as the Within-Cluster-Sum of Squared Errors (WSS) diminishes can be selected as the most natural point of deciding how many clusters should exist. This is commonly known as "the elbow method" Why is that point used as the optimal amount of clusters, and in this case customer segements? 

Because at that cluster number, the diminishing marginal returns for adding more clusters to minimizing WSS begins to set in; i.e. you're gaining little information and nuance for added additions to cluster numbers relative to minimizing your errors. In this case it’s determined we should have 3 clusters/customer segments.

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Clustered.png)
