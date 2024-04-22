## Sensitivity Analysis 
- Sensitivity analysis is a tool used to assess the impact of changes in different input variables on a specific output variable, especially in complex or opaque processes. It is used in various fields for different purposes, including:
	- Financial Modeling
	- Biology
	- Geography
	- Economics
	- Engineering 
- This is used in process called "Black Box" where output = opaque function of several inputs. Opaque functions are those functions which can not be studied or analyzed. 
	- **Example :** 
		- For example, climate models in geography are usually very complex. As a result, the exact relationship between the inputs and outputs is not well understood.

## What-if analysis 
- Mostly used by financial analysts to predict the outcome of a specific action when performed under certain conditions.
- Here boundaries are set by independent variables, hence the the conditions are rigid.
- **Example :**
	- **What** would happen to the price of a bond **If** interest rates went up by 1%?”. This question can be answered with sensitivity analysis
	- The analysis is performed in Excel, under the Data section of the ribbon and the “What-If Analysis” button, which contains both “Goal Seek” and “Data Table”.

## Data Analytics 
- It is the science of analyzing raw data to make conclusions about that information, it helps a business optimize its performance, preform more efficiently,  maximize profit, or make more strategically-guided decisions.
- **Data** : 
	- It is a valuable resource in today’s ever-changing marketplace. For business professionals, knowing how to interpret and communicate data is an indispensable skill that can inform sound decision-making.
- **Business Analytics :**
	- Business analytics involves using math and statistics to collect, analyze, and interpret data for making better business decisions.
	- Types :
		- **Descriptive**: Interpreting historical data to identify trends and patterns.
		- **Predictive**: Using historical data to forecast future outcomes.
		- **Diagnostic**: Identifying the root cause of a problem by analyzing data.
		- **Prescriptive**: Testing and employing techniques to determine the best outcome in a given scenario.
	- Business analytics aids in decision-making across industries and contributes to organizational success.
	- Examples : 
		1. **Microsoft**:
		    - **Objective**: Improve productivity and collaboration.
		    - **Strategy**: Relocated an engineering group to increase face-to-face interactions.
		    - **Outcome**: Reduced meeting travel time by 46%, saved 100 hours per week across all relocated staff, and improved collaboration and operational efficiency.
		2. **Uber**    
		    - **Objective**: Enhance customer support.
		    - **Strategy**: Implemented Customer Obsession Ticket Assistant (COTA) to assist customer service agents using machine learning and natural language processing.
		    - **Outcome**: Reduced ticket resolution time by 10%, led to faster service, improved accuracy, and improved customer satisfaction scores.
		3. **Blue Apron**
		    - **Objective**: Forecast orders and recipes to avoid product spoilage and fulfill orders.
		    - **Strategy**: Utilized predictive analytics and algorithms based on customer preferences and seasonality.
		    - **Outcome**: Achieved a high level of forecasting accuracy, with a root-mean-square error consistently below 6%, improving user experience and understanding customer behavior.
		4. **PepsiCo**
		    - **Objective**: Target specific consumers to improve product merchandising.
		    - **Strategy**: Developed a cloud-based data and analytics platform called Pep Worx.
		    - **Outcome**: Identified specific households interested in certain products (e.g., Quaker Overnight Oats) and targeted those households, resulting in 80% of the product’s sales growth in its first 12 months.
- **Business Analytics vs. Data Science**:
	- **Focus**:
	    - **Business Analytics**: Extracting meaningful insights from data to guide organizational decisions.
	    - **Data Science**: Turning raw data into meaningful conclusions through algorithms and statistical models.
	- **Roles**:
	    - **Business Analysts**: Participate in tasks like budgeting, forecasting, and product development.
	    - **Data Scientists**: Focus on data wrangling, programming, and statistical modeling.

## Feature Engineering overview 
- **Feature :**
	- It's an individual measurable property of a data point used as input for a machine learning algorithm. Features can be numerical, categorical, or text-based, and they represent different aspects of the data that are relevant to the problem at hand.
- The process of creating new features or transforming existing features to improve the performance of a machine learning model. The goal is to improve model accuracy by providing more meaningful and relevant information to the model.
- **Need for Feature Engineering**:
	- **Improve User Experience**: Enhance user experience by creating intuitive, efficient features.
	- **Competitive Advantage**: Differentiate products from competitors by offering unique features.
	- **Meet Customer Needs**: Create features based on customer feedback and market trends.
	- **Increase Revenue**: Create features that can streamline processes or offer additional functionality.
	- **Future-Proofing**: Develop features that anticipate future trends and customer needs.
- **Processes Involved in Feature Engineering**:
	- 1. **Feature Creation**: Generating new features based on domain knowledge or patterns in the data.
	1. **Feature Transformation**: Transforming features to a suitable representation for the model.
	2. **Feature Extraction**: Creating new features from existing ones to provide more relevant information.
	3. **Feature Selection**: Selecting a subset of relevant features for a machine learning model.
	4. **Feature Scaling**: Transforming features so that they have a similar scale.
- **Steps in Feature Engineering**:
	- 1. Data Cleansing: Identifying and correcting errors in the dataset.
	1. Data Transformation: Transforming data to be more suitable for the model.
	2. Feature Extraction: Creating new features from existing ones.
	3. Feature Selection: Selecting the most relevant features from the dataset.
	4. Feature Iteration: Refining and improving the features based on the model's performance.
- **Techniques Used in Feature Engineering**:
	- **One-Hot Encoding**: Transforming categorical variables into binary values.
	- **Binning**: Transforming continuous variables into categorical variables by dividing them into bins.
	- **Scaling**: Techniques like standardization and normalization to scale features.
	- **Feature Split**: Splitting single features into multiple sub-features based on criteria.
	- **Text Data Preprocessing**: Techniques for preparing text data such as removing stop words and stemming.
- **Feature Engineering Tools**:
	1. **Featuretools**:
    - An open-source Python library for automated feature engineering. It allows you to extract features from multiple data sources and create features based on user-defined primitives.
	1. **TPOT (Tree-based Pipeline Optimization Tool)**:
	    - Uses genetic programming to optimize machine learning pipelines, including feature engineering, to find the best combination of features and models.
	2. **DataRobot**:
	    - An automated machine learning platform that provides tools for feature engineering, including creating new features and selecting the best ones for a model.
	3. **Alteryx**:
	    - A data preparation and automation tool that offers a visual interface for creating data pipelines, including feature extraction and transformation.
	4. **H2O.ai**:
	    - An open-source machine learning platform that provides both automatic and manual feature engineering capabilities, such as scaling, imputation, and encoding, as well as tools for handling text and image data.
- By focusing on the most relevant features and transforming them effectively, machine learning models can learn from data more effectively and produce better outcomes.


## 