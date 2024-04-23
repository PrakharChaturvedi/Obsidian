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
	1. **Feature Creation**: Generating new features based on domain knowledge or patterns in the data.
	2. **Feature Transformation**: Transforming features to a suitable representation for the model.
	3. **Feature Extraction**: Creating new features from existing ones to provide more relevant information.
	4. **Feature Selection**: Selecting a subset of relevant features for a machine learning model.
	5. **Feature Scaling**: Transforming features so that they have a similar scale.
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

## Scalable Computing 
- Scalable computing refers to the ability of a computer system, network, or infrastructure to expand and adapt its resources to accommodate growing demands for computing capabilities. This can be achieved by adding more nodes, upgrading hardware, or utilizing cloud resources. Scalability is important for ensuring the system can handle increasing loads without compromising performance.
- **Key aspects of scalable computing include:**
	- **Flexibility**
		- Scalable systems can expand or contract their resources based on current needs. This means adding or removing nodes, increasing storage, or reallocating resources as demand fluctuates.
	- **Cost-Effectiveness**
		- By only using the necessary resources at any given time, scalable computing allows businesses to manage costs effectively, avoiding over-provisioning and under-utilization.
	- **High-Speed Networks**
		- The availability of high-speed networks enables the connection of resources spread across geographical locations, making it possible to create computational grids and clusters that span countries and continents.
	- **Clusters and Grids**
		- Scalable computing often involves clustering, where multiple workstations are connected via a local area network (LAN) for low-cost, flexible, and easy scaling. Grid computing, on the other hand, combines geographically dispersed resources such as desktop computers, storage, data sources, and scientific instruments into computational grids.
	- **Geographical Spread**
		- Scalable computing doesn't need to be confined to a single location. Resources can be distributed across various geographical regions and interconnected to form a unified network, enabling collaboration and sharing of computing power globally.
- Applications of scalable computing include data warehousing, where scalability is essential to handle the growing volumes of data being stored and processed. Scalable computer architecture allows for efficient management and retrieval of data while ensuring the system can accommodate future growth.

## Parallel Computing 
- Parallel computing is a type of computing architecture where a large, complex problem is divided into smaller, independent parts that can be executed simultaneously by multiple processors. This allows for faster application processing and problem solving, as tasks can be completed concurrently.
- **Types of Parallel Computing**:
    - **Bit-level parallelism**: Increases processor word size to reduce the number of instructions needed for operations on variables larger than the processor word.
    - **Instruction-level parallelism**: Executes multiple instructions simultaneously, either dynamically decided by the processor at runtime (dynamic parallelism) or predetermined by the compiler (static parallelism).
    - **Task parallelism**: Runs different tasks concurrently on multiple processors using the same data.
    - **Superword-level parallelism**: A vectorization technique that exploits parallelism in inline code.
- **Parallel Applications**:
    - **Fine-grained parallelism**: Subtasks communicate frequently (several times per second).
    - **Coarse-grained parallelism**: Subtasks communicate less frequently.
    - **Embarrassingly parallel**: Subtasks rarely or never communicate with each other.
- **Parallel Computer Architecture**:
    - **Multi-core computing**: Processors with two or more cores that execute instructions in parallel, allowing for improved performance.
    - **Symmetric multiprocessing**: Uses multiple homogeneous processors controlled by a single operating system, sharing main memory and resources.
    - **Distributed computing**: Components are located on different networked computers that coordinate actions through communication.
    - **Massively parallel computing**: Involves many processors working together, either in a centralized cluster or through grid computing over the internet.
- **Parallel Computing Software Solutions**:
    - **Application checkpointing**: Records application state to provide fault tolerance and restore from failure.
    - **Automatic parallelization**: Converts sequential code to multi-threaded code to use multiple processors simultaneously.
    - **Parallel programming languages**: Include languages for distributed and shared memory programming.
- Parallel computing plays a crucial role in modern computing, especially with the rise of multicore processors and GPUs. By leveraging the power of parallelism, computations can be performed more efficiently, making it essential for high-performance computing, scientific research, and other demanding applications.


## Difference Between Parallel Computing and Cloud Computing
- Parallel computing and cloud computing are two distinct concepts, though they can work together to achieve greater computational power and efficiency.
- **Parallel Computing**:
    - **Definition**: Parallel computing is a computing architecture that involves dividing a larger, complex problem into smaller, independent tasks that can be executed simultaneously by multiple processors.
    - **Objective**: The goal of parallel computing is to increase computational power and speed by allowing multiple processors to work on different tasks simultaneously.
    - **Focus**: Focuses on optimizing performance and efficiency in computational tasks.
    - **Hardware**: Utilizes hardware such as multi-core processors, GPUs, and clusters of computers for computation.
- **Cloud Computing**:
    - **Definition**: Cloud computing is the delivery of scalable services such as databases, data storage, networking, servers, and software over the Internet on an as-needed, pay-as-you-go basis.
    - **Objective**: The goal of cloud computing is to provide scalable, on-demand access to resources and services, including storage, computing power, and software, to users anywhere with an Internet connection.
    - **Focus**: Focuses on providing access to resources and services through the cloud, allowing users to scale their operations without investing in additional hardware.
    - **Infrastructure**: Cloud computing providers manage the infrastructure and offer services such as Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS).

## Parallel processing v/s Parallel computing
- **Parallel processing**
	- It is a computing method where a complex task is divided into smaller parts and executed simultaneously on multiple CPUs or cores. The main focus is on dividing tasks efficiently across multiple processors to reduce overall processing time. Parallel processing often involves using computer science techniques and tools to manage workload distribution and task synchronization within a single computer system or networked systems.
- **Parallel computing** 
	- It encompasses the design and use of algorithms and software that exploit multiple processors or cores to perform tasks simultaneously. The focus is on optimizing software and algorithms to take full advantage of parallel processing capabilities. Parallel computing can apply to various contexts such as distributed systems, clusters, and grids, extending beyond a single computer system and leveraging parallel processing techniques for improved performance.

## Sequential v/s parallel computing
- **Sequential computing**, or serial computation, 
	- It involves using a single processor to execute a program in a linear fashion, where instructions are processed one after another without any overlap. This traditional programming approach is straightforward but is constrained by the speed of the processor and can be a bottleneck when handling complex tasks.
- **Parallel computing**, 
	- On the other hand, divides a task into smaller, independent parts that are processed simultaneously across multiple processors or cores. While this approach can be more complex and expensive initially, it offers significant advantages in terms of speed and efficiency, particularly in data-intensive applications like data science, machine learning, and artificial intelligence.

## Data Visualization 
- **Data visualization** is the technique used to deliver insights in data using visual cues such as graphs, charts, maps, and many others. This is useful as it helps in intuitive and easy understanding of the large quantities of data and thereby make better decisions regarding it.
- R is a language that is designed for statistical computing, graphical data analysis, and scientific research. It is usually preferred for data visualization as it offers flexibility and minimum required coding through its packages.
- Types of Data Visualizations 
	- **Bar Plot**
		- There are two types of bar plots- horizontal and vertical which represent data points as horizontal or vertical bars of certain lengths proportional to the value of the data item. They are generally used for continuous and categorical variable plotting. By setting the **horiz** parameter to true and false, we can get horizontal and vertical bar plots respectively.
		- Example :
			`arplot``(airquality$Ozone,`
		        `main =` `'Ozone Concenteration in air'``,`
		        `xlab =` `'ozone levels'``, horiz =` `TRUE``)` 
		- Diagram :  
		- ![[Pasted image 20240422204004.png]]
	- **Histogram**
		- A histogram is like a bar chart as it uses bars of varying height to represent data distribution. However, in a histogram values are grouped into consecutive intervals called bins. In a Histogram, continuous values are grouped and displayed in these bins whose size can be varied.
		- Example :
			`data``(airquality)`
			`hist``(airquality$Temp, main ="La Guardia Airport's\`
			`Maximum` `Temperature``(Daily)",`
				`xlab =``"Temperature(Fahrenheit)"``,`
				`xlim =` `c``(50, 125), col =``"yellow"``,`
				`freq =` `TRUE``)`
		- Diagram :  ![[Pasted image 20240422203930.png]]
	- **Box Plot**
		- The statistical summary of the given data is presented graphically using a boxplot. A boxplot depicts information like the minimum and maximum data point, the median value, first and third quartile, and interquartile range.
		- Example : 
			`data``(airquality)`
			`boxplot``(airquality$Wind, main = "Average wind speed\`
			`at La Guardia Airport",`
			        `xlab =` `"Miles per hour"``, ylab =` `"Wind"``,`
			        `col =` `"orange"``, border =` `"brown"``,`
			        `horizontal =` `TRUE``, notch =` `TRUE``)`
		- Diagram : ![[Pasted image 20240422203808.png]]
	- **Scatter Plot**
		- A scatter plot is composed of many points on a Cartesian plane. Each point denotes the value taken by two parameters and helps us easily identify the relationship between them.
		- Example :
			`data``(airquality)`
			`plot``(airquality$Ozone, airquality$Month,`
			     `main =``"Scatterplot Example"``,`
			    `xlab =``"Ozone Concentration in parts per billion"``,`
			    `ylab =``" Month of observation "``, pch = 19)`
		- Diagram :![[Pasted image 20240422203845.png]]	 

