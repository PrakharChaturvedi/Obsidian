Tags : #Ai-ML-DL
## *Clustering* 
- **Clustering** is the task of dividing the population or data points into a number of groups such that data points in the same groups are more similar to other data points in the same group and dissimilar to the data points in other groups.
- It is basically a collection of objects on the basis of similarity and dissimilarity between them.
- <font color="#ffc000">Why clustering?</font>
	- Clustering is very much important as it determines the intrinsic grouping among the unlabeled data present. There are no criteria for good clustering. 
	- It depends on the user, and what criteria they may use which satisfy their need.
- <font color="#ffc000">Applications of clustering </font>
	- **Marketing:** It can be used to characterize & discover customer segments for marketing purposes.
	- **City Planning:** It is used to make groups of houses and to study their values based on their geographical locations and other factors present.
	- **Libraries:** It is used in clustering different books on the basis of topics and information.
	- **Insurance:** It is used to acknowledge the customers, their policies and identifying the frauds.
	- **Customer Service:** Clustering is used to group customer inquiries and complaints into categories, identify common issues, and develop targeted solutions.
	- **Fraud detection:** Clustering is used to identify suspicious patterns or anomalies in financial transactions, which can help in detecting fraud or other financial crimes.
## *K means clustering*
- K-Means Clustering is an <font color="#ffc000">Unsupervised Learning algorithm</font>, which groups the unlabeled dataset into different clusters. Here k define the number of clusters that need to be created in the process, as k = 2 (2 clusters) and for k = 3 (3 clusters), there will be 3 clusters and so on. 
- The k-means clustering algorithm mainly performs two tasks:
	- Determines the best value for k center points or centroids by an iterative process.
	- Assigns each data point to its closest k-center. Those data points which are near to the particular k-center, create cluster.
- Example :![[Pasted image 20231117160004.png]] 
## *Agglomerative Clustering* :
- Agglomerative Clustering is **a type of hierarchical clustering algorithm**. It is an unsupervised machine learning technique that divides the population into several clusters such that data points in the same cluster are more similar and data points in different clusters are dissimilar.
- Initially we have some data points, we keep on making clusters in hierarchy format until we get the final cluster which comprises of all the data points that we were considering initially.
- Youtube link => (https://www.youtube.com/watch?v=G_Ob1k28ZJo)

## *Regression* :
- Regression analysis is a statistical method to model the relationship between a dependent (target) and independent (predictor) variables with one or more independent variables.
- More specifically, Regression analysis helps us to understand how the value of the dependent variable is changing corresponding to an independent variable when other independent variables are held fixed. It predicts continuous/real values such as **temperature, age, salary, price,** etc.
- Related term
	- **Multicollinearity:** If the independent variables are highly correlated with each other than other variables, then such condition is called Multicollinearity. It should not be present in the dataset, because it creates problem while ranking the most affecting variable. 
## *Linear Regression* :
- Linear regression is also a type of supervised machine-learning algorithm that learns from the labeled datasets and maps the data points to the most optimized linear functions, which can be used for prediction on new datasets.
- It computes the linear relationship between a dependent variable and one or more independent features/variables.
- The goal of the algorithm is to find the best linear equation that can predict the value of the dependent variable based on the independent variables. The equation provides a straight line that represents the relationship between the dependent and independent variables. The slope of the line indicates how much the dependent variable changes for a unit change in the independent variable(s).
- Linear regression is used in many different *fields, including finance, economics, and psychology,* to understand and predict the behavior of a particular variable.![[Pasted image 20231117192828.png]]

## *Linear v/s Logistic Regression*:
![[Pasted image 20231117193019.png]]

## *Support Vector Machine (SVM)*
- It lies in supervised learning used for classification and regression analysis.
- The main objective of the SVM algorithm is to find the optimal <font color="#ffc000">hyperplane</font> in an N-dimensional space that can separate the data points in different classes in the feature space.
- The hyperplane tries that the margin between the closest points of different classes should be as maximum as possible. The dimension of the hyperplane depends upon the number of features.
- <font color="#92d050">How it works?</font>
	- First we draw a line in between of 2 categories without intersecting any object which is called hyperplane.
	- Then we make 2 new lines parallel to the hyperplane touching the nearest part of object to the hyperplane. (we get 2 distance Hyperplane to L1 and L2, we call it D+ and D- respectively).
	- Margin = (D-) + (D+), now higher the width better the classification. 
- Types of SVM's :
	- Simple or linear SVM
		- When a dataset can be segregated into categories or classes with the help of a single straight line, it is termed a linear SVM, and the data is referred to as linearly distinct or separable
	- Kernel or non-linear SVM
		- The classifier is referred to as a non-linear classifier. The classification can be performed with a non-linear data type by adding features into higher dimensions rather than relying on 2D space. Here, the newly added features fit a hyperplane that helps easily separate classes or categories.

## <font color="#ffc000">Basic Questions</font> :
- <font color="#00b050">Manhattan Distance Formula</font> = |x2-x1|  + |y2-y1|
- <font color="#00b050">Euclidean distance formula</font> = Root[(x2-x1)^2 + (y2-y1)^2]
- <font color="#00b050">Frequent data sets  </font>
	- A frequent item set is **a set of items that occur together frequently in a dataset**. The frequency of an item set is measured by the support count, which is the number of transactions or records in the dataset that contain the item set.
- <font color="#00b050">What is Support in ML? </font>
	- Support refers to how often a given rule appears in the database being mined.
- <font color="#00b050">What is Confidence in ML?</font>
	- Confidence refers to the amount of times a given rule turns out to be true in practice.
- <font color="#00b050">Association rule mining</font>
	- Association rule mining finds interesting associations and relationships among large sets of data items. This rule shows how frequently a itemset occurs in a transaction. A typical example is a Market Based Analysis.
- <font color="#00b050">Partitioned-based clustering</font>
	- Partition-based clustering is a type of clustering algorithm that divides a dataset into non-overlapping subsets or partitions. 
	- Each partition represents a cluster, and the goal is to group similar data points together within the same partition while keeping dissimilar points in different partitions.
	- Partition-based clustering methods do not require a predefined number of clusters, making them flexible and suitable for various types of datasets.
- <font color="#00b050">Density based clustering</font>
	- Density-based clustering is a type of clustering algorithm that identifies clusters based on the density of data points in the feature space.
	- Unlike partition-based methods such as K-means, density-based clustering methods do not require specifying the number of clusters beforehand and can discover clusters of arbitrary shapes.

Next - [[The Vault/AI-ML-DL/Machine learning/My Notes 2|My Notes 3]]
