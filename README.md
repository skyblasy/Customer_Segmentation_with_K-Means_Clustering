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

A fundamental question in marketing is knowing who the target consumer segment is to maximize return on marketing spent. This project is an example of how to answer that question and solve that problem.

This project takes customer transaction data and uses feature engineernig to transform them to  purchasing frequency, recency, and monetary amount as relevant dimensions and factors segmentation and separates the accounts with two different strategies. 

## Binning on a given number of quantiles

This first method is more arbitrary but allows greater discretion on part of management  in defining segments. This is achieved by ranking each customers’ purchase recency, frequency, and monetary amount for a given quantile and then summing those values together to get a value associated with a certain rank of customer; Platinum, Gold, Silver, Bronze. 

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Binned.png)

This approach offers a lot of flexibility in deciding how many groups can be formed. But, for that same reason, that is also a potential pitfall; the categories are arbitrarily chosen, so can it really be certain that the highest segment really represents all the best customers? Or, is the number of segments really the appropriate amount? Could there be more or potentially fewer? Fortunately there is a more organic way to differentiate customers.

## K-means Clustering

K-means clustering is a popular unsupervised machine learning algorithm used for partitioning a dataset into a set of distinct, non-overlapping subgroups or 'clusters'. Each cluster is defined by the mean value of the data points within it. The primary goal of the K-means algorithm is to minimize the variance within each cluster and maximize the variance between the clusters.

When applied to customer and marketing segmentation, the benefits of using K-means clustering include:

Data-driven segmentation: K-means provides an objective approach to segmentation, based on actual data patterns rather than preconceived notions or biases. This can unveil hidden patterns in customer behavior and preferences.

Scalability: K-means can handle large datasets efficiently, making it suitable for businesses with vast amounts of customer data.

Customizable number of segments: By selecting the number of clusters 'K', businesses can tailor the granularity of their segmentation based on their specific needs.

Cost-effective: Instead of relying on expensive market research or external consultants, K-means offers an in-house, computational method to quickly identify and adapt to market segments.

Dynamic adaptation: As customer behavior changes or new data becomes available, K-means can be re-run to identify evolving segments and trends.

Improved targeting and personalization: With clearer segmentation, businesses can craft more targeted and personalized marketing campaigns, leading to higher engagement and conversion rates.

Resource optimization: Understanding distinct customer segments allows businesses to allocate resources more efficiently, targeting high-value segments or addressing the unique needs of each segment.

In summary, K-means clustering provides a powerful, scalable, and cost-effective method to discover and understand customer segments, leading to more insightful and effective marketing strategies.

![me](https://github.com/skyblasy/Customer_Segmentation_with_K-Means_Clustering/blob/main/Customer_Clustered.png)


