# **Machine Learning Engineer Nanodegree**
# Unsupervised Learning
## Project: Creating Customer Segments

### Problem Statement
1.	Performed unsupervised algorithms to best describe the variation in the different types of customers that a wholesale distributor interacts with. The dataset is from https://archive.ics.uci.edu/ml/datasets/Wholesale+customers
2.	Feature Relevance with the usage of DecisionTreeRegressor
3.	R^2 score to look at feature relevance. R^2 score is between 0 and 1. The negative R^2 implies the model falls to fit the data. If you get a low score for a particular feature, that lends us to believe that feature point is hard to predict using the other features, thereb making it an important feature to consider when considering relevance. (can use PCA to fix it)
4.	If data is not normally distributed, especially if the mean and median vary significantly. It’s most often appropriate to apply a non-linear scaling -perform natural logarithm transformation – reduce skewness.
5.	Skewness is the value not normally distributed within one feature, and we use natural logarithm transformation to fix this. The normalization issue is the scale of the value for one feature is different from the scale of the value for other features (the issue when features have different scale.).  We use minMaxScalar to fix this issue. Minmax or standard/normalize scaling are for centering data. Logarithmic transform is for removing skew. 
6.	Outlier detection: The presence of outliers can often skew results which take into consideration these data points. 
7.	Outlier detection and remove (data has no outlier)-> Logarithmic transformation (data is normalized)- > Standard/Normalize Scaling (data is scale) -> PCA
8.	PCA
9.	Clustering: K-Means clustering algorithm or Gaussian Mixture model clustering algorithm and use silhouette score to measure the clustering performance. The shilhouette coefficient for a data point meatures how similar it is to its assigned cluster from -1 (dissimilar) to 1(similar). Calculating the mean silhouette coefficient provides for a simple scoring method of a given clustering.
