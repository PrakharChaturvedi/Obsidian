### Fuzzy Sets terminologies :
- <font color="#ffc000">Core :</font> The **core** of a fuzzy set 𝐴 is the set of all elements 𝑥 in the universe of discourse 𝑋 where the membership function 𝜇𝐴(𝑥) is equal to 1. In other words, it consists of all elements that fully belong to the fuzzy set.
- <font color="#ffc000">Support :</font> The **support** of a fuzzy set 𝐴 is the set of all elements 𝑥 in the universe of discourse 𝑋 where the membership function 𝜇𝐴(𝑥) is greater than 0. It includes all elements that have a non-zero degree of membership in the fuzzy set.
- <font color="#ffc000">Singleton Set :</font> A **singleton set** in the context of fuzzy sets is a fuzzy set where only one element has a non-zero membership value, and that value is typically 1.
- <font color="#ffc000">Band Width :</font> The **band width** of a fuzzy set refers to the range of values in the universe of discourse over which the membership function is non-zero. It essentially describes the spread or width of the fuzzy set.
- <font color="#ffc000">Cross-over Points :</font> **Cross-over points** are the values of 𝑥 in the universe of discourse where the membership function 𝜇𝐴(𝑥) is equal to 0.5. These points indicate where the membership grade of the fuzzy set transitions from being less than 0.5 to greater than 0.5, or vice versa.
- <font color="#ffc000">Convexity :</font> A fuzzy set 𝐴 is **convex** if for any two elements 𝑥1x and 𝑥2​ in the universe of discourse 𝑋, and for any 𝜆∈[0,1], the membership function satisfies :
	-> 𝜇𝐴 (𝜆𝑥1 + (1−𝜆) 𝑥2) *≥* min⁡(𝜇𝐴(𝑥1) , 𝜇𝐴(𝑥2)) 
	This means that the membership grade of any point between 𝑥1 and 𝑥2​ should not be less than the minimum membership grade of 𝑥1​ and 𝑥2.
- <font color="#ffc000">α-cut :</font> The α-cut of a fuzzy set is the subset of elements from the universe of discourse for which the membership degree in the fuzzy set is at least as high as the threshold 𝛼α. This operation essentially <font color="#00b050">converts a fuzzy set into a crisp set</font> by retaining only those elements whose membership degrees exceed or equal a certain level of certainty.
- <font color="#ffc000">Normality :</font> A fuzzy set 𝐴 is **normal** if there is at least one element in the universe of discourse 𝑋 whose membership grade is 1. In other words, the maximum membership grade in the fuzzy set is 1.

### Consider the Following membership Functions: 
- A = { (x1, 0.3). (x2, 0.5), (x3,1), (x4,0.8),(x5,0.1) } 
- B = { (x1, 0.5). (x2, 0.2). (x3,0.7), (x4,0.4), (x5,0.6) }
- Perform the following Fuzzy Operations on these fuzzy sets:
	a. Algebraic sum [ uA(x) + uB(x) - uA(x) * uB(x) ]
	b. Algebraic difference [μA−B​(x) = max ( 0,μA​(x)−μB​(x) )]
	c. Bounded sum [uA(x) (+) uB(x) = min { 1, uA(x) + uB(x) }]
	d. Union [uAUB(x) = max { uA(x), uB(x) }]
	e. Algebraic product [ uA . B(x) = uA(x) * uB(x) ]
	f. Bounded difference [ uA(x) (-) uB(x) = max { 1, uA(x) + uB(x) }]
	g. Cartesian product [ uAxB(x,y) = min { uA(x), uB(x) }]
![[WhatsApp Image 2024-02-21 at 13.07.58_f0ced6d4.jpg]]

## Types of activation functions :
- Activation functions play a critical role in soft computing, particularly in artificial neural networks (ANNs). They determine the output of a neuron given an input or set of inputs.
- Types :
	- Sigmoid Activation Function
		- The sigmoid function, also known as the logistic function, is defined as:
		- $σ(x)=1/(1+e^−x )​$
		- Output Range: (0, 1)
		- Shape: S-shaped curve (sigmoidal)
		- Differentiability: Smooth and differentiable, making it suitable for backpropagation.
	- Hyperbolic tangent (tanh) Activation Function
		- The tanh function is defined as:
		- $tanh(x)=e^x+e^−x/e^x−e^−x​$
		- Output Range: (-1, 1)
		- Shape: Similar to sigmoid but scaled and shifted.
	- ReLU (Rectified Linear Unit Activation Function
		- ReLU(x)=max(0,x)
		- Output range : (0,∞)
		- Shape: Linear for positive inputs and zero for negative inputs.
	- Softmax Activation Function 
		- The softmax function is often used in the output layer of neural networks for classification tasks. 
		- Output Range: (0, 1), with all outputs summing to 1.
		- Shape: Converts raw scores into probabilities.
	- ELU (Exponential Linear Unit Activation Function)
		- It's particularly effective in reducing the vanishing gradient problem during training.
		- ELU might be computationally more expensive than ReLU due to the use of exponential function. Despite this, it's been shown to perform well in various types of neural networks, particularly in networks with deeper architectures.
	- Diagram :![[1_RD0lIYqB5L2LrI2VTIZqGw.webp]]

## LeNet Architecture :
- 1 input layer, 3 convolutional layers, 2 pooling layers, 1 fully connected layer and one output layer
- Layers description : 
	- Input (grayscale image)
	- Convolution layer 1
	- Pooling Layer 2
	- Convolution layer 3
	- Pooling Layer 4
	- Convolution layer 5
	- Fully connected layer
	- Output (softmax for classification)

## Define regularization and drop-out regularization in short
- Regularization
	- Regularization is a set of techniques used in machine learning to prevent overfitting by adding additional information or constraints to a model. Overfitting occurs when a model learns the noise and details in the training data to an extent that it negatively impacts its performance on new, unseen data.
- Dropout Regularization
	- Dropout regularization is a technique used to prevent overfitting in neural networks by randomly "dropping out" a fraction of neurons during training. This means that each iteration of training, a different subset of the network's neurons is used, forcing the network to learn more robust features that are not reliant on specific neurons. 
	- During testing, all neurons are used, but their outputs are scaled by the dropout rate to balance the overall activation levels. This helps to improve the generalization ability of the model.

## How to map human brain in ANN 
- Mapping the human neural network using Artificial Neural Networks (ANNs) involves creating computational models that emulate the brain's structure and function. 
- ANNs consist of layers: input, hidden, and output, analogous to sensory, processing, and motor neurons, respectively. 
- Each artificial neuron processes inputs through weights and biases, similar to synapses in biological neurons. Training involves adjusting these weights using algorithms like backpropagation to minimize error. 
- Activation functions enable non-linear transformations, akin to the brain's complex signal processing. Deep Neural Networks (DNNs), with many hidden layers, mirror the brain’s hierarchical processing for tasks like image recognition. 
- This approach leverages neuroplasticity, allowing ANNs to learn and adapt, reflecting the dynamic nature of human neural networks.