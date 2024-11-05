- ##  *What is machine learning?*
	- It is a branch of artificial intelligence and computer science which focused on the use of data and algorithms to imitate the way that humans learns, gradually improving the accuracy.
- *When do we use AI?*
	- Human expertise does not exist (Mars navigation)
	- Humans can't explain their expertise (Speech recognition)
	- Models must be customized (personalized medication)
	- Models based on huge amount of data (Genomics)
## *Production system* 
- Production systems are **computer programmer that give AI**. It consists of a set of rules about behavior's and includes the mechanism required to follow those rules as the system reacts to external conditions. In AI, a production system consists of a global database, production rules, and a control system.
- Types  
	-  **Monotonic system** This system allows the simultaneous application of rules. This means that the application of one rule does not prevent another rule from being applied at the same time.
	- **Partially commutative system** Here, the order of operation is important. If a given set of rules is employed to convert a start state A into a different state B, then the same results can be attained using any permutation of these production rules.
	- **Non-monotonic system** This system helps in solving problems that were ignored. It can be executed without backtracking to initial states when an incorrect path was taken. The Non-monotonic system provides an efficient way of solving problems.
	- **Commutative system** This system is used when the order of operation is not an important issue of consideration. It is ideal for solving problems in a situation where changes can be reversed. This is unlike in a partially commutative system, where the order of operation is crucial and changes are irreversible.
## *Data*
- It is information that has been translated into a form that is efficient for processing. 
- Types of data 
	- Qualitative 
		- Description of anything 
	- Quantitative 
		- Numerical information (Numbers)
		- Types 
			- Discreate : Data can only take certain values (like whole numbers)
			- Continuous : Data can take any value (within a range)

## *How does machine learning work* 
- Step 1 : Input data 
- Step 2 : Analyze data 
- Step 3 : Find patterns
- Step 4 : Prediction/Decision
- Step 5 : Learns from feedback.
## *Applications of ML* 
- Virtual assistance : Intelligent agents, NLP, etc... 
- Social media :  Sentiment analysis, filtering spam, etc...
- Transport : Safety monitoring, air traffic control, etc...
- Financial Services : Algorithm trading, portfolio management, fraud detection.
- Healthcare : Drug discovery, Disease diagnosis, robotic surgery
- eCommerce : Customer support, product recommendation, advertising

## *Machine learning process*
- Import raw data 
- Apply preprocessing to data 
- Data preparation (Iterations b/w 2 steps for achieving ready data for training)
	- Data pre-processing modules are introduced to apply
	- To get Prepared data
- Model choosing (Iterations b/w steps to find the best model)
	- Applying machine learning algorithms to data 
	- Candidate model 
- Deploy chosen model 
- The chosen model is used for application

## Types of Machine Learning Algorithms
- Four types of ML algorithms:
	- <font color="#ffc000">Supervised Learning Algorithms :</font>
		- Definition:
			- It is based on supervision 
			- Training of machine using **"labelled"** dataset, and based on the training, the machine predicts the output.
			- <font color="#9bbb59">Labelled data</font> specifies that some of the inputs are already mapped to the output. 
			- <font color="#92d050">More preciously, we can say; first, we train the machine with the input and corresponding output, and then we ask the machine to predict the output using the test dataset.</font>
		- Example:
			- Suppose we have an input dataset of cats and dog images. So, first, we will provide the training to the machine to understand the images, such as the shape & size of the tail of cat and dog, Shape of eyes, color, height (dogs are taller, cats are smaller), etc.
			- After completion of training, we input the picture of a cat and ask the machine to identify the object and predict the output. Now, the machine is well trained, so it will check all the features of the object, such as height, shape, color, eyes, ears, tail, etc., and find that it's a cat. So, it will put it in the Cat category. This is the process of how the machine identifies the objects in Supervised Learning.
		- <font color="#8db3e2"><font color="#4bacc6">The main goal of the supervised learning technique is to map the input variable(x) with the output variable(y). Some real-world applications of supervised learning are Risk Assessment, Fraud Detection, Spam filtering, etc.</font></font>
		- Supervised problems can be divided into the following two types: 
			- <font color="#00b050">Classification</font>:
				- Classification algorithms are used to solve the classification problems in which the output variable is categorical, such as *"Yes" or No*, *Male or Female*, *Red or Blue*, etc. 
				- The classification algorithms predict the categories present in the dataset.
				- Some real-world examples of classification algorithms are *Spam Detection, Email filtering, etc.*
				- Some popular classification algorithms are given below: 
					- <font color="#4bacc6">Random Forest Algorithm</font> 
					- <font color="#4bacc6">Decision Tree Algorithm </font>
					- <font color="#4bacc6">Logistic Regression Algorithm </font>
					- <font color="#4bacc6">Support Vector Machine Algorithm</font>
			- <font color="#00b050">Regression</font>:
				- Regression algorithms are used to solve regression problems in which there is a linear relationship between input and output variables. 
				- These are used to predict continuous output variables, such as market trends, weather prediction, etc. 
				- Some popular Regression algorithms are given below: 
					- <font color="#4bacc6">Simple Linear Regression Algorithm</font>
					- <font color="#4bacc6">Multivariate Regression Algorithm </font>
					- <font color="#4bacc6">Decision Tree Algorithm </font>
					- <font color="#4bacc6">Lasso Regression</font>
	- <font color="#ffc000">Unsupervised Learning Algorithms</font>
		- Different from supervised learning technique.
		- It does not require supervision.
		- The machine is trained using the **unlabeled data**, and machine predicts the output without any supervision.
		- The models are trained with the data that is neither classified nor labelled, and the model acts on that data without any supervision.
		- <font color="#4bacc6">The main aim of the unsupervised learning algorithm is to group or categories the unsorted dataset according to the similarities, patterns, and differences.</font>
		- Example
			- Suppose there is a basket of fruit images, and we input it into the machine learning model. The images are totally unknown to the model, and the task of the machine is to find the patterns and categories of the objects. 
			- So, now the machine will discover its patterns and differences, such as color difference, shape difference, and predict the output when it is tested with the test dataset.
		- Unsupervised leanings can be classified into two types
			- Clustering 
				- The clustering technique is used when we want to find the inherent groups from the data. It is a way to group the objects into a cluster such that the objects with the most similarities remain in one group and have fewer or no similarities with the objects of other groups.
				- Some popular clustering algorithms is given below
					- K-Means Clustering algorithm 
					- Mean-shift algorithm 
					- DBSCAN Algorithm 
					- Principal Component Analysis 
					- Independent Component Analysis
			- Association
				- Association rule learning is an unsupervised learning technique, which finds interesting relations among variables within a large dataset. 
				- The main aim of this learning algorithm is to find the dependency of one data item on another data item and map those variables accordingly so that it can generate maximum profit.
				- Some popular algorithms of Association rule learning are 
					- Apirori algorithm
					- Eckat FP-growth algorithm
	- <font color="#ffc000">Semi-Supervised Learning Algorithms</font>	
		- Falls in b/w supervised and unsupervised ML technique by incorporating elements of both methods. 
		- Used when we have limited set of data available to train the system.
		- As a result the machine is only partially trained.
		- First uses unsupervised learning to predict class labels then goes to supervised learnings. 
		- The information the machine generates during this partial training is called *pseudo data* and later on computer combines both labeled and the pseudo-data to make predictions. 
		- Has wide variety of usage like *healthcare industry, speech identification, and analysis*.
	- <font color="#ffc000">Reinforcement Learning Algorithms</font>
		- Reinforcement learning works on a feedback-based process, in which an AI agent (A software component) automatically explore its surrounding by hitting & trail, taking action, learning from experiences, and improving its performance.
		- Agent gets rewarded for each of good action and get punishment for each bad action.
		- Hence the goal of reinforcement learning agent is to maximize the rewards.
## *AI v/s ML*
  ![[Pasted image 20231019235927.png]]

## **Overfitting vs underfitting**
- Overfitting : 
	- Overfitting is **a concept in data science, which occurs when a statistical model fits exactly against its training data**. When this happens, the algorithm unfortunately cannot perform accurately against unseen data, defeating its purpose.
- Underfitting : 
	- **When a model has not learned the patterns in the training data well and is unable to generalize well on the new data**, it is known as underfitting. An underfit model has poor performance on the training data and will result in unreliable predictions. 

## *KNN* : 
- k nearest neighbor
- It is a lazy algorithm
- Classifies new points based on a similarity measure.
- Identifies data points that are separated into several classes to predict the classification of a new sample point.

Next - [[The Vault/AI-ML-DL/Machine learning/My Notes 2|My Notes 2]]
