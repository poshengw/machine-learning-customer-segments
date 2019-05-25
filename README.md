## Machine Learning Engineer Nanodegree
## Unsupervised Learning
### Creating Customer Segments

### Project Summary:
- Performed **unsupervised algorithms** to best describe the variation in the different types of customers that a wholesale distributor interacts with.
- Analyzed the task that use unsupervised learning techniques to see if any similarities exist between customers, and how to best segment customers into distinct categories.
- **Data explore** by using **DecisionTreeRegressor** and **R^2 score** to find out Feature Relevance and determine if any product categories highly correlate with one another. R^2 score is between 0 and 1. The negative R^2 implies the model falls to fit the data. If you get a low score for a particular feature, that leads us to believe that this feature is hard to predict using the other features, therefore making it an important feature to consider when considering relevance. (can use PCA to fix it)
- **Data preprocessing:**<br/> 
&nbsp;1. Outlier detection and remove (data has no outlier) &rarr; <br/>
&nbsp;2. Logarithmic transformation (data is normalized) &rarr; <br/>
&nbsp;3. Standard/Normalize Scaling (data is scale) &rarr; <br/>
&nbsp;4. PCA <br/>
Applied a non-linear scaling natural logarithm transformation to reduce skewness, and then identified (and removing) unwanted outliers. The presence of outliers can often skew results which take into consideration these data points. . Skewness is the value not normally distributed within one feature, and we use natural logarithm transformation to fix this. The normalization issue is the scale of the value for one feature is different from the scale of the value for other features (the issue when features have different scale.).  We use minMaxScalar to fix this issue. Minmax or standard/normalize scaling are for centering data. Logarithmic transform is for removing skew. 
- Applied **PCA transformations** to the data.
- Implement **K-Means and Gaussian Mixture clustering algorithms** to segment and use **lhouette score** to measure the clustering performance. The shilhouette coefficient for a data point meatures how similar it is to its assigned cluster from -1 (dissimilar) to 1(similar). Calculating the mean silhouette coefficient provides for a simple scoring method of a given clustering.
- Optimally **cluster** a set of data to find hidden patterns in a dataset.
- Assessed information given by cluster segmentation data and use it in a meaningful way.

## Data:

The customer segments data is included as a selection of 440 data points collected on data found from clients of a wholesale distributor in Lisbon, Portugal. More information can be found on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers).

Note (m.u.) is shorthand for *monetary units*.

**Features**
1) `Fresh`: annual spending (m.u.) on fresh products (Continuous); 
2) `Milk`: annual spending (m.u.) on milk products (Continuous); 
3) `Grocery`: annual spending (m.u.) on grocery products (Continuous); 
4) `Frozen`: annual spending (m.u.) on frozen products (Continuous);
5) `Detergents_Paper`: annual spending (m.u.) on detergents and paper products (Continuous);
6) `Delicatessen`: annual spending (m.u.) on and delicatessen products (Continuous); 
7) `Channel`: {Hotel/Restaurant/Cafe - 1, Retail - 2} (Nominal)
8) `Region`: {Lisbon - 1, Oporto - 2, or Other - 3} (Nominal) 
