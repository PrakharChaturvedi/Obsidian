Unit 1 :  Elements, Variables, and Data categorization, Levels of Measurement, Data management and indexing, Introduction to statistical learning and R-Programming
Unit 2 : Measures of central tendency, Measures of location of dispersions, Practice and analysis with R
## Data Science 
- Data science is a interdisciplinary field that uses scientific methods and computational techniques to extract valuable insights from data. It involves <font color="#ffc000">collecting, cleaning, and analyzing data, as well as building and evaluating models</font> for predictive or descriptive purposes. 
- Data scientists apply statistical methods, machine learning, and domain-specific knowledge to make data-driven decisions in various industries. The process includes data collection, preprocessing, exploratory data analysis, model building, evaluation, deployment, and iterative refinement.   
## Data Analytics 
- Data analytics is the process of examining and interpreting data to find useful insights and make informed decisions. It involves cleaning and analyzing data using statistical methods and computational tools to identify patterns and trends. The goal is to extract valuable knowledge from data for practical applications across various industries.
- Types :
	1. **Descriptive Analysis:**
	    - **Characteristics:** Descriptive analytics focuses on summarizing and aggregating historical data to provide a comprehensive view of past events.
	    - **Methods:** Common techniques include data summarization, aggregation, and visualization through tools like charts and graphs.
	    - **Application:** Businesses use descriptive analytics to monitor key metrics, assess performance, and gain a broad understanding of trends over time.
	2. **Predictive Analysis:**
	    - **Characteristics:** Predictive analytics aims to forecast future outcomes by analyzing patterns and relationships in historical data.
	    - **Methods:** This involves the use of statistical algorithms, machine learning models, and data mining techniques to make predictions.
	    - **Application:** Industries leverage predictive analysis for forecasting sales, demand planning, risk management, and identifying potential opportunities or threats.
	3. **Diagnostic Analysis:**
	    - **Characteristics:** Diagnostic analytics focuses on understanding the reasons behind past events or trends by analyzing historical data in more detail.
	    - **Methods:** Root cause analysis, correlation analysis, and in-depth examination of contributing factors are common diagnostic techniques.
	    - **Application:** Businesses use diagnostic analysis to investigate anomalies, identify the factors influencing performance issues, and improve decision-making processes.
	4. **Prescriptive Analysis:**
	    - **Characteristics:** Prescriptive analytics provides recommendations on actions to optimize future outcomes based on predictive models.
	    - **Methods:** Utilizes advanced analytics, optimization algorithms, and simulation techniques to suggest the best course of action.
	    - **Application:** This type of analysis is applied in scenarios where organizations want actionable insights, such as optimizing marketing strategies, supply chain management, and resource allocation.
- Process :
	1. Data Requirements Specification 
	2. Data Collection 
	3. Data Processing 
	4. Data Cleaning 
	5. Data Analysis 
	6. Communication
 
## Variables 
- Definition : In R, a variable is a symbolic name assigned to a storage location that holds a data value.
- Example : You might create a variable called `age` to store a vector of ages, or `gender` to store a factor representing male or female.
- <font color="#9d69f4">Independent Variables :</font> 
	- In statistical analysis, the independent variable is the variable that is manipulated or controlled in an experiment. It is the variable that is<font color="#ffc000"> presumed to cause the changes in the dependent variable.</font>
	- The independent variable is <font color="#ffc000">typically plotted on the x-axis in a graph</font>, and its values are used to categorize or group the data.
	- <font color="#ffc000">Example</font> : someone's age, space, time, mass, fluid, etc.
	- <font color="#e41c2a">Types of Independent variables :</font> 
		- **Experimental Variables** :
			- Experimental independent variables are those that researchers intentionally change or manipulate in an experiment to observe their effect on the dependent variable. Researchers have control over these variables, and they are actively modified to test their impact on the outcome.
		- **Subject Variables** :
			- Subject variables, also known as non-experimental or quasi-independent variables, are characteristics or traits of the participants that cannot be manipulated by the researcher. These variables exist naturally and are not subject to intentional modification.
- <font color="#9d69f4">Dependent Variables :</font> 
	- The dependent variable in a research study is the variable that is being observed, measured, or tested to determine the effects of the independent variable.
	- It is the outcome or response variable that researchers are interested in understanding or predicting. The changes in the dependent variable are assumed to be influenced by the manipulation or variation of the independent variable(s).
	- <font color="#ffc000">Example</font> : In a study examining the effect of a new drug on patients' blood pressure, the dependent variable would be the blood pressure of the patients. If the drug has an impact, the changes in blood pressure are attributed to the manipulation of the independent variable


## Data element definition :
- A data element is a conceptual, logical definition of data with specific characteristics, including identification, size, type, and potentially a specific set of values. It is distinct from the physical storage unit, known as a field, where the data element is stored within records in a data processing system.

## Level of Measurement 
- Level of measurement refers to how variables are categorized and measured. There are four levels: Nominal (categories with no order), Ordinal (categories with order), Interval (consistent intervals without a true zero), and Ratio (consistent intervals with a true zero).
- <font color="#ffc000">Example :</font> If you wanted to analyze the spending habits of people living in Indore, you might send out a survey to 500 people asking questions about their income, their exact location, their age, and how much they spend on various products and services. These are your variables: data that can be measured and recorded, and whose values will differ from one individual to the next
- <font color="#ffc000">Importance :</font> Understanding the level of measurement is crucial for selecting appropriate statistical analyses, interpreting data meaningfully, choosing descriptive and inferential statistics, and guiding data treatment. It ensures accurate and relevant statistical analysis aligned with the nature of the data.
- 4 levels of measurements :
	1. **Nominal Level:**
	    - Definition: Categorical data without any inherent order or ranking.
	    - Characteristics: Categories are mutually exclusive, and there is no meaningful order among them.
	    - Example: Colors, gender, or types of fruits.
	2. **Ordinal Level:**
	    - Definition: Categorical data with a meaningful order or ranking.
	    - Characteristics: Intervals between categories are not consistent or meaningful.
	    - Example: Education levels (e.g., high school, college, graduate), socio-economic status.
	3. **Interval Level:**
	    - Definition: Numeric data with consistent intervals between values but no true zero point.
	    - Characteristics: Has a meaningful order, and the differences between values are consistent.
	    - Example: Temperature measured in Celsius or Fahrenheit, IQ scores.
	4. **Ratio Level:**
	    - Definition: Numeric data with a true zero point, where zero indicates the absence of the attribute being measured.
	    - Characteristics: Has a meaningful order, consistent intervals, and a true zero point.
	    - Example: Height, weight, income, number of items.


## Vectors :
- A vector is a fundamental data structure that represents an ordered collection of elements of the same data type. Vectors can be of different types, such as numeric, character, logical, etc.
- 2 types of vectors :
	- <font color="#ffc000">Single element vector</font>
		- Only a single element in a vector is called a a single element vector.
		- It is a special case of a vector where the length of the vector is one. Despite having just one element, it is still considered a vector in R.
		- Exmple : single_vector <- (1.5)
	- <font color="#ffc000">Multiple element vector</font>
		- A Multiple-elements vector in R is a vector that contains more than one element. It is the most common type of vector used in R to store and manipulate collections of data.
		- A Multiple-elements vector in R is a vector that contains more than one element. It is the most common type of vector used in R to store and manipulate collections of data.
			- numeric_vector <- c(1.5, 2.3, 4.0, 5.1)
			- character_vector <- c("apple", "banana", "orange")
			- logical_vector <- c(TRUE, FALSE, TRUE, TRUE)
- <font color="#9d69f4">The c() function is used to create a vector with multiple elements. The elements are separated by commas within the parentheses.</font> 
- Some more codes :
	- <font color="#ffc000">Sequence operator :</font>
		- Create vector with elements from 5 to 9 incrementing by 0.4. 
			 -> print(seq(5, 9, by = 0.4))
			 --> Solution : [1] 5.0 5.4 5.8 6.2 6.6 7.0 7.4 7.8 8.2 8.6 9.0
	- <font color="#ffc000">Accessing vectors :</font>
		- <font color="#9d69f4">Using position : </font>
			- t <- c("Sun","Mon","Tue","Wed","Thurs","Fri","Sat")
				u <- t[c(2,3,6)]
				print(u)
		- <font color="#9d69f4">Logical indexing :</font>
			- v <- t[c(TRUE,FALSE,FALSE,FALSE,FALSE,TRUE,FALSE)]
		- <font color="#9d69f4">Negative indexing : </font>
			- x <- t[c(-2,-5)]
		- <font color="#9d69f4">0/1 indexing </font>
			- y <- t[c(0,0,0,0,0,0,1)]
	- <font color="#ffc000">Operations on vectors :</font>
		-  <font color="#9d69f4">Addition : </font>
			v1 <- c(3,8,4,5,0,11) 
			v2 <- c(4,11,0,8,1,2)
			result <- v1+v2 
			print(result)
		- <font color="#9d69f4">Sorting :</font>
			v <- c(3,8,4,5,0,11, -9, 304)
			result <- sort(v)
			print(result)
		- <font color="#9d69f4">Empty Recycling :</font>
			v1 <- c(3,8,4,5,0,11) 
			v2 <- c(4,11)
			result <- v1+v2 
			print(result)
			result_sub <- v1-v2
			print(result_sub)

## List 
- Lists are the R objects which contain elements of different types like − numbers, strings, vectors and another list inside it. A list is a collection of data which is ordered and changeable. A list can also contain a matrix or a function as its elements. List is created using list() function.
- <font color="#ffc000">Example :</font>
	- list_data <- list("Red", "Green", c(21,32,11), TRUE, 51.23, 119.1) 
		print(list_data)
- <font color="#ffc000">Naming list elements :</font>
	- list_data <- list(c("Jan", "Feb", "Mar"), matrix(c(3,9,5,1,-2,8), nrow = 2),list("green",12.3))
		names(list_data) <- c("1st Quarter", "A_Matrix", "A Inner list")
		print(list_data)
	- <font color="#9d69f4">Output :</font>
		$ `1st Quarter`
		[1] "Jan" "Feb" "Mar"
		$ A_Matrix
		[,1]  [,2]  [,3]
		[1,]   3    5   -2
		[2,]   9    1    8
		$`A Inner list`
		$`A Inner list` [[1]]
		[1] "green"
		$`A Inner list`[[2]]
		[1] 12.3 
- <font color="#ffc000">Accessing :</font>
	- Elements of the list can be accessed by the index of the element in the list. In case of named lists it can also be accessed using the names.
	- print(list_data[1])
	- print(list_data$A_Matrix)

## Matrices 
- A matrix is a two-dimensional data structure that contains elements arranged in rows and columns. Each element in a matrix must be of the same data type. You can create a matrix using the `matrix()` function.
- Code :
	- <font color="#ffc000">Creating a matrix</font>
		my_matrix <- matrix(1:6, nrow = 2, byrow = TRUE)
		print(my_matrix)
	- <font color="#ffc000">Accessing elements in a matrix</font>
		print(my_matrix[1, 2])  
	- <font color="#ffc000">Transposing a matrix</font>
		transposed_matrix <- t(my_matrix)
		print(transposed_matrix)
	- <font color="#ffc000">Matrix multiplication</font>
		matrix_product <- my_matrix % * % transposed_matrix
		print(matrix_product)

## Array 
- An array is a multi-dimensional data structure that extends the concept of matrices to more than two dimensions. You can create arrays using the `array()` function.
- <font color="#ffc000">Creating an array :</font>
	- my_array <- array(1:24, dim = c(2, 3, 4))
		print(my_array)
- <font color="#ffc000">Naming Column and rows </font>
	- dimnames(my_array) <- list(c("Row1", "Row2"), c("Col1", "Col2", "Col3"), c("Depth1", "Depth2", "Depth3", "Depth4"))
		print(my_array)
- <font color="#ffc000">Accessing Array Elements:</font>
	- element <- my_array["Row1", "Col2", "Depth3"] 
		print(element)
- <font color="#ffc000">Manipulating Array Elements:</font>
	- my_array["Row1", "Col2", "Depth3"] <- 999
		print(my_array)

## Data frames 
- A data frame is a two-dimensional data structure that can store different types of data, including numeric, character, and factor variables. You can create a data frame using the `data.frame()` function.
- <font color="#ffc000">Creation : </font>
	- my_data <- data.frame(
		Name = c("Alice", "Bob", "Charlie"), 
		Age = c(25, 30, 22),
		Gender = c("Female", "Male", "Male"),
		stringsAsFactors = FALSE 
		)
		print(my_data)

## Factors :
- Factors are a special type of data structure in R used to represent categorical variables. They are created using the `factor()` function.
- <font color="#ffc000">Declaration : </font>
	- gender_factor <- factor(c("Male", "Female", "Male", "Female"))
		print(gender_factor)
- <font color="#ffc000">Adding a factor variable to the data frame </font>: 
	- my_data$MaritalStatus <- factor(c("Single", "Married", "Single"), levels = c("Single", "Married"))
		print(my_data) 