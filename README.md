# Customer Segmentation with K-Means Clustering
## Tehnologies Used
- Python
- Jupyter notebook
- Scikit-learn
- K-means clustering
- Pandas
- Numpy
- Seaborn
- Matplotlib

## Who are the top performing customers and how can we determine that? 

Market segmentation is a fundamental business strategy that allows companies to cater more effectively to the diverse needs and preferences of their customers. By dividing a broad market into subsets of consumers with similar characteristics or behaviors, businesses can design and deliver more personalized products, marketing messages, and service offerings. This tailored approach not only drives customer satisfaction and loyalty but also optimizes resource allocation, enhances competitive positioning, and increases the likelihood of success in new product launches. In an increasingly crowded marketplace, market segmentation is crucial for businesses seeking to maintain relevance and maximize profitability.

## Binning on a given number of quantiles

This first method is more arbitrary but allows greater discretion on part of management  in defining segments. This is achieved by ranking each customers’ purchase recency, frequency, and monetary amount for a given quantile and then summing those values together to get a value associated with a certain rank of customer; Platinum, Gold, Silver, Bronze. 

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Binned.png)

This approach offers a lot of flexibility in deciding how many groups can be formed. But, for that same reason, that is also a potential pitfall; the categories are arbitrarily chosen, so can it really be certain that the highest segment really represents all the best customers? Or, is the number of segments really the appropriate amount? Could there be more or potentially fewer? Fortunately there is a more organic way to differentiate customers.

## K-means Clustering

K-means clustering is a popular unsupervised machine learning algorithm used for partitioning a dataset into a set of distinct, non-overlapping subgroups or 'clusters'. Each cluster is defined by the mean value of the data points within it. The primary goal of the K-means algorithm is to minimize the variance within each cluster and maximize the variance between the clusters.

#### Understanding Within Sum of Squares (WSS):
WSS is a measure of the total squared distance between each point in a cluster and the centroid of that cluster. Lower WSS values indicate that data points are closer to the centroids of their respective clusters, signifying a better clustering.

As you increase the number of clusters, the WSS typically decreases because there are more centroids, so points are, on average, closer to their respective centroid. However, after a certain point, adding more clusters leads to diminishing returns in the reduction of WSS. The "elbow" of the curve represents an inflection point where the decrease in WSS begins to slow down. Choosing the number of clusters at this "elbow" balances the trade-off between having too many or too few clusters.

The elbow method is visually intuitive. A plot of the number of clusters against the corresponding WSS allows decision-makers to quickly identify the optimal number of clusters without getting lost in complex computations or metrics, and often produces a number of clusters that is reasonable and interpretable in a business context. This ensures that the derived customer segments are actionable and can be effectively communicated to marketing teams.

In ths workflow, I used the Yellowbrick API to automatically find and allocate the correct number of clusters based on the WWS, in this case it was three. 

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Clustered.png)

In summary, K-means clustering provides a powerful, scalable, and cost-effective method to discover and understand customer segments, leading to more insightful and effective marketing strategies.

