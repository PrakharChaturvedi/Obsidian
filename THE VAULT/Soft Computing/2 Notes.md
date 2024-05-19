## Artificial Neural Network 
- <font color="#ffc000">Biological neural network</font> :
	- The biological nervous system is crucial for many living organisms, particularly humans.
	- The brain is a central component of the human nervous system.
	- Neurons are the building blocks of the nervous system, functioning as interconnected processing units.
	- Neurons are approximately 10µm in length and can operate in parallel.
	- The human brain typically comprises around 10^11 (100 billion) neurons.
	- Communication among neurons occurs through electrical impulses.
- <font color="#ffc000">Neurons and it's working</font> :
	- <font color="#00b050">Neuron Components</font>: Dendrite (thin fiber bush), Axon (long cylindrical fiber), Soma (cell body), Synapse (junction between axon and neighboring dendrites).
	- <font color="#00b050">Neurotransmitter</font>: Chemical in neurons facilitating signal transmission.
	- <font color="#00b050">Signal Transmission</font>: Signals (senses) transmitted via neurotransmitters across neurons through dendrites.
	- <font color="#00b050">Signal Accumulation</font>: Signals accumulate at neuron synapse before transmission.
	- <font color="#00b050">Electrical Impulse</font>: Action can generate a millisecond-long electrical impulse, triggered by incoming signals.
	- <font color="#00b050">Threshold</font>: Action potential occurs in the axon only if signals surpass a threshold.
	- <font color="#00b050">Signal Summation</font>: Incoming signals summed at soma before transmitting through axon.
- <font color="#ffc000">Artificial Neural Network</font> :
	- <font color="#00b050">Human brain</font>: A highly intricate network of interconnected neurons responsible for complex functions like computation, storage, and learning.
	- <font color="#00b050">Artificial Neural Networks (ANNs)</font>: Simplified computational models inspired by the structure and functioning of the brain, used for various tasks in machine learning and artificial intelligence.
	- <font color="#00b050">Biological neuron analogy</font>: ANNs mimic the structure and behavior of biological neurons, with each component of an artificial neuron mirroring its biological counterpart.
	- <font color="#00b050">Neuron function</font>: Biological neurons receive inputs through dendrites, integrate them at the soma, and produce output if the integrated signal surpasses a certain threshold. 
	- <font color="#00b050">Synaptic weights</font>: In ANNs, weights represent the strength of connections (synapses) between neurons, with stronger connections having higher weights.
	- <font color="#00b050">Input calculation</font>: The total input to an artificial neuron's soma is computed as the sum of the products of input values and their corresponding weights.
	- **Function :** 
		- **Transformation functions** :
			- <font color="#ffc000">Hard-limit transfer function</font> : 
				- The transformation we have just discussed is called hard-limit transfer function. It is generally used in perception neuron.
				- φ(I) = { 1 , if I > θ 
						{ 0 , if I ≤ θ
			- <font color="#ffc000">Linear transfer function</font> :
				- The output of the transfer function is made equal to its input (normalized) and its lies in the range of −1.0 to +1.0. It is also known as Signum or Quantizer function 
				- φ(I) = { +1 , if I > θ 
						{ −1 , if I ≤ θ 
		- **Other transformation function** :
			- <font color="#ffc000">Sigmoid transfer function</font> :
				- This function is a continuous function that varies gradually between the asymptotic values 0 and 1 (called log-sigmoid) or -1 and +1 (called Tan-sigmoid) threshold function and is given by
				- φ(I) = (1/1+e−αI) [log-Sigmoid]
				- φ(I) = tanh(I) = (e^(αI) - e^(αI))/(e^(αI) + e^(αI)) [tan-Sigmoid]
				- a -> coefficient of transfer function  ![[Pasted image 20240318234728.png]]
	- **Advantages of ANN** :
		-  <font color="#ffc000">Mapping capabilities</font>: ANNs can map input patterns to corresponding output patterns, making them useful for various tasks.
		- <font color="#ffc000">Learning by examples</font>: ANNs are trained with known examples of a problem before being tested on unknown instances, allowing them to identify new objects.
		- <font color="#ffc000">Generalization</font>: ANNs can generalize, applying learned patterns to new situations where exact mathematical models are unavailable.
		- <font color="#ffc000">Robustness and fault tolerance</font>: ANNs can recall full patterns from incomplete, partial, or noisy data, making them resilient to errors.
		- <font color="#ffc000">Parallel processing</font>: ANNs process information in parallel, rapidly and in a distributed manner, enabling highly interconnected systems with learning capabilities.
- **Architecture of Neural Network** **:**
	- 3 fundamental classes of ANN architecture :
		- Single layer feed forward architecture
		- Multilayer feed forward architecture
		- Recurrent networks architecture
- **Types of learning in neural network** **:**  
	- <font color="#ffc000">Single layer feed forward neural network</font> :
		- A single-layer feedforward neural network (SLFN) is a type of feedforward neural network that consists of only one layer of neurons. In this architecture, the input layer receives the input signal, and the output layer generates the network's output.
		- The key feature of a single-layer feedforward network is that it does not involve hidden layers for computation. Instead, the output is computed directly based on the weighted inputs. This network is simple and effective for tasks where a direct mapping from inputs to outputs is sufficient, such as basic classification or regression problems.
		- Functioning : 
			- The inputs x1, x2, · · · , xm are connected to the layers of neurons through the weight matrix W.
			- W = | w11 w12 w13 ..... w1n   |
				 | w21 w22 w23 ...  w2n  |
				 |   .       .       .          .     |
				 |   .       .       .          .     |
				 | wm1 wm2 wm3 ... wmn |
			- Output of Kth neuron can be determined as follows : 
				- Ok = fk (**Σ**m i=1 (wik xi) + θk)
					- k = 1, 2, 3, .... n 
					- θk denotes the threshold value of the k-th neuron. Such network is feed forward in type or acyclic in nature and hence the name.![[Pasted image 20240319100706.png]]
	- <font color="#ffc000">Multilayer feed forward neural network</font> :
		- It is a type of artificial neural network that consists of multiple layers of interconnected neurons. These networks are designed to process information in a forward direction, from the input layer through hidden layers to the output layer. 
		- The number of layers in a neural network corresponds to the number of layers of perceptrons, with each layer contributing to the network's ability to learn and generalize.
		- In a multilayer feedforward neural network:
			- The input layer receives input signals.
			- Hidden layers perform computations and pass results to subsequent layers.
			- The output layer generates the final output based on the processed information.
			- Weights associated with neurons are adjusted during training to minimize loss through backpropagation.
			- Activation functions like sigmoid, tanh, or ReLU are used in different layers for non-linear transformations.
			- The network can be used for tasks like binary classification, multiclass classification, regression, and forecasting
		- Key points about MLFNNs include:
			- They can approximate any differentiable function with sufficient hidden neurons in two layers.
			- Adding more hidden layers can sometimes improve accuracy and reduce computational time compared to increasing the number of neurons in a single hidden layer.
			- MLFNNs are widely used in various fields like medicine, speech regeneration, data processing, and image processing.![[Pasted image 20240319102459.png]]
		- Functioning : 
			1. **Network Architecture:**
				- Input Layer: Contains ***l*** neurons.
				- Hidden Layer: Contains ***m*** neurons.
				- Output Layer: Contains ***n*** neurons. 
			2. **Input and Weight Matrices:**
				- Inputs x1,x2,…,xp​ are fed to the input layer.
				- Weight matrices:
					- W1​ between the input layer and the first layer.
					- W2​ between the first layer and the hidden layer.
					- W3​ between the hidden layer and the output layer.
			3. **Transfer Functions and Threshold Values:**
				- Transfer functions:
					- f1​ for neurons in the first layer.
					- f2​ for neurons in the hidden layer.
					- f3​ for neurons in the output layer.
				- Threshold values:
					- θ1i​ for the i-th neuron in the first layer.
					- θ2j​ for the j-th neuron in the hidden layer.
					- θ3k​ for the k-th neuron in the output layer.
			4. **Output Calculation:**
				- The output Oli​ of the i-th neuron in the l-th layer is computed using: Oli​ = fl​(∑X***i***+​​W***l***​+θ***li***​) where ***X***l​ is the input vector to the **l-th** layer, W***l***​ represents the weight matrix for connections to the **l-th** layer, and θ***li***​ is the threshold value for the **i-th** neuron in the **l-th** layer.
	- <font color="#ffc000">Recurrent neural network architecture</font>
		- The networks differ from feedback network architectures in the sense that there is at least one ”feedback loop”. Thus, in these networks, there could exist one layer with feedback connection. There could also be neurons with self-feedback links, that is, the output of a neuron is fed back into itself as input. ![[Pasted image 20240319104319.png]]
	- <font color="#ffc000">Dynamic Neural Network</font> 
		- In some cases, the output needs to be compared with its target values to determine an error, if any.
		- Based on this category of applications, a neural network can be static neural network or dynamic neural network. 
		- In a static neural network, error in prediction is neither calculated nor feedback for updating the neural network. On the other hand, in a dynamic neural network, the error is determined and then feed back to the network to modify its weights (or architecture or both). ![[Pasted image 20240319110546.png]]

#### NOTE :
- For linearly separable problems, we solve using single layer feed forward neural network.
- For non-linearly separable problem, we solve using multilayer feed forward neural networks. 
- For problems, with error calculation, we solve using recurrent neural networks as well as dynamic neural networks.

## Types of learning :
- **Learning**
	- <font color="#ffc000">Supervised</font> 
		- Stochastic
		- Error Correction gradient descent
			- Least mean square
			- Back propagation
	- <font color="#ffc000">Unsupervised</font>
		- Hebbian
		- Competitive
	- <font color="#ffc000">Reinformed</font>
- <font color="#ffc000">Supervised Learning Algorithms :</font>
	-  Definition:
		 - It is based on supervision 
		 - Training of machine using **"labelled"** dataset, and based on the training, the machine predicts the output.
		- <font color="#9bbb59">Labelled data</font> specifies that some of the inputs are already mapped to the output. 
		- <font color="#92d050">More preciously, we can say; first, we train the machine with the input and corresponding output, and then we ask the machine to predict the output using the test dataset.</font>
		- <font color="#8db3e2"><font color="#4bacc6">The main goal of the supervised learning technique is to map the input variable(x) with the output variable(y). Some real-world applications of supervised learning are Risk Assessment, Fraud Detection, Spam filtering, etc.</font></font>
- <font color="#ffc000">Unsupervised Learning Algorithms</font>
	- Definition :
		- Different from supervised learning technique.
		- It does not require supervision.
		- The machine is trained using the **unlabeled data**, and machine predicts the output without any supervision.
		- The models are trained with the data that is neither classified nor labelled, and the model acts on that data without any supervision.	
		- <font color="#4bacc6">The main aim of the unsupervised learning algorithm is to group or categories the unsorted dataset according to the similarities, patterns, and differences.</font>
- <font color="#ffc000">Reinforcement Learning Algorithms</font>
	- Reinforcement learning works on a feedback-based process, in which an AI agent (A software component) automatically explore its surrounding by hitting & trail, taking action, learning from experiences, and improving its performance.
	- Agent gets rewarded for each of good action and get punishment for each bad action.
	- Hence the goal of reinforcement learning agent is to maximize the rewards.
- <font color="#ffc000">Gradient Descent learning</font> 
	- **Objective**: Gradient Descent minimizes error (E) in a neural network by adjusting weights based on the error gradient (∂E/∂Wij).
	- **Requirement**: Activation function must be differentiable for gradient calculation. As the weight update is dependent on the gradient of the error E.
	- **Weight Update (ΔWij)**: Determined by the learning rate (η) multiplied by the error gradient (∂E/∂Wij).
		- Formula :
			- ∆Wij = η (∂E)/(∂Wij) 
	- **Variations**:
		1. **Least Mean Square (LMS)**: Minimizes mean square error between predicted and target values.
		2. **Backpropagation**: Computes error at output and propagates it backward to adjust weights layer by layer.
- <font color="#ffc000">Stochastic learning</font> 
	- Simulated Annealing, introduced by Boltzmann and Cauchy, adjusts weights in a neural network probabilistically. Inspired by the annealing process in metallurgy, it starts with high temperatures allowing random exploration of weight configurations, gradually cooling to focus on minimizing errors. Unlike deterministic methods, it accepts uphill moves with a certain probability, allowing exploration of the solution space. This probabilistic approach helps avoid local minima, potentially leading to better overall solutions.
- <font color="#ffc000">Hebbian learning</font> 
	- This learning technique, inspired by biology, relies on correlative weight adjustment, where input-output pattern pairs (xi, yi) are associated with a weight matrix W, also known as the correlation matrix. 
	- In this method, the matrix W is computed by summing the outer products of each input-output pair. Specifically, W is calculated as the sum from i=1 to n of the outer product of the input vector Xi and the transpose of the associated output vector yi. 
	- This correlation matrix serves as a basis for adjusting weights in accordance with the input-output relationships observed in the training data.
- <font color="#ffc000">Competitive learning</font>
	- In this learning method, those neurons which responds strongly to input stimuli have their weights updated. When an input pattern is presented, all neurons in the layer complete and the winning neuron undergoes weight adjustment. This is why it is called a Winner-takes-all strategy.

## CNN (Convolutional Neural Network)
- <font color="#ffc000">Explanation</font> : 
	- CNN stands for Convolutional Neural Network. It's a type of artificial neural network designed to analyze visual data by automatically and adaptively learning spatial hierarchies of features from the input images. <font color="#92d050">CNNs consist of multiple layers, including convolutional layers that apply convolutional operations to extract features, pooling layers that reduce spatial dimensions, and fully connected layers for classification or regression tasks.</font> They are widely used in computer vision tasks such as image classification, object detection, and image segmentation due to their ability to capture local patterns efficiently.
	- Convolutional neural networks are distinguished from other neural networks by their superior performance with image, speech, or audio signal inputs. <font color="#ffc000">They have three main types of layers, which are:</font>
		- Convolutional layer
		- Pooling layer
		- Fully-connected (FC) layer
	- The **convolutional layer** is the first layer of a convolutional network. While convolutional layers can be followed by additional convolutional layers or pooling layers, the fully-connected layer is the final layer. 
	- With each layer, the CNN increases in its complexity, identifying greater portions of the image. Earlier layers focus on simple features, such as colors and edges. 
	- As the image data progresses through the layers of the CNN, it starts to recognize larger elements or shapes of the object until it finally identifies the intended object.
- <font color="#ffc000">Components</font> :
	 1. **Convolutional Layer**: This layer applies filters (kernels) to the input image, detecting features through parameter sharing. Hyperparameters like the number of filters, stride, and padding affect the size of the output feature maps. The ReLU activation function introduces nonlinearity to the model.
	2. **Additional Convolutional Layers**: Following the initial convolutional layer, subsequent layers create a hierarchical structure, allowing the network to recognize higher-level patterns by combining lower-level features.
	3. **Pooling Layer**: Pooling layers perform downsampling, reducing the spatial dimensions of the input while retaining important features. Max pooling and average pooling are common pooling methods, each selecting or averaging values within a receptive field.
	4. **Fully-Connected Layer**: In this layer, every node is connected to every node in the previous layer, enabling classification based on extracted features. Typically, softmax activation is used for multi-class classification tasks, producing probability distributions over the classes.
	These components work together to process input images, extract features at different levels of abstraction, and make predictions.
-  <font color="#ffc000">ReLU function</font> :
	- The Rectified Linear Unit (ReLU) function is a simple mathematical operation used in neural networks to introduce nonlinearity. It replaces negative values in the input with zeros and leaves positive values unchanged. Mathematically, ReLU can be represented as:
		\[ f(x) = \max(0, x) \]
	- ReLU is popular in deep learning because it helps alleviate the vanishing gradient problem and accelerates convergence during training. Additionally, it's computationally efficient compared to other activation functions like sigmoid or tanh.
- <font color="#ffc000">Convolutional Kernel</font> : 
	- A convolutional kernel, also called a filter, is a small matrix of learnable weights used in a Convolutional Neural Network (CNN). It slides over input data, computing dot products at each position to detect features. These weights are adjusted during training to recognize different patterns in the data.
	- The result is summed up to produce a single value in the output feature map. By using different filters with varying parameters (such as size, shape, and weights), CNNs can learn to detect different types of features at multiple spatial locations in the input image
- <font color="#ffc000">Feature Map</font> :
	- **Feature map** refers to the output of applying convolutional filters (also known as kernel filters) to an input image. Each feature map represents the activation of neurons in a particular layer of the network, corresponding to specific learned features detected in the input image. These features could include edges, textures, shapes, or higher-level patterns. 
- <font color="#ffc000">Applications</font> : 
	-  **Image Classification**: CNNs classify images into predefined categories, like identifying animals or objects in photos.
	-  **Object Detection**: CNNs locate and identify objects within images, crucial for tasks like autonomous driving and security surveillance.
	-  **Facial Recognition**: CNNs recognize faces, enabling applications like unlocking smartphones or identifying individuals in crowds.
	-  **Medical Image Analysis**: CNNs analyze medical images to detect diseases, assisting radiologists in diagnosis and treatment planning.
	-  **Video Analysis**: CNNs process video data for tasks such as action recognition and surveillance, enhancing security and enabling personalized content recommendations.
- <font color="#ffc000">Visual Representation</font> : ![[Pasted image 20240319115043.png]]


## Deep vs Shallow learning 
 -  **Shallow Learning:**
	- Shallow learning, also known as shallow machine learning, refers to the use of relatively simple models with a small number of layers or processing stages. These models typically have a limited capacity to learn complex patterns from data. 
	- Examples of shallow learning algorithms include linear regression, logistic regression, decision trees, k-nearest neighbors, and support vector machines. 
	- These algorithms are often used for tasks where the data has relatively simple patterns and the relationships between features and outcomes are straightforward.
 -  **Deep Learning:** 
	 -  Deep learning, on the other hand, involves using neural networks with many layers to automatically learn intricate patterns and representations from data.
	 - Deep learning has shown impressive performance in various fields, such as image and speech recognition, natural language processing, and game playing.
	 -  Deep learning models, such as convolutional neural networks (CNNs) and recurrent neural networks (RNNs), are capable of capturing complex relationships in data by progressively extracting hierarchical features.

## Backpropagation with gradient decent method
- **Backpropagation** is a fundamental algorithm used to train neural networks. It's a supervised learning technique that allows networks to adjust their weights and biases in order to minimize the difference between predicted and actual outputs.
- In backpropagation, the network first makes a forward pass, where input data is fed through the network, resulting in an output prediction. 
- Then, the algorithm calculates the error between the predicted output and the actual target output using a <font color="#ffc000">predefined loss function</font>. Next, it performs a backward pass through the network to propagate this error backward, layer by layer, while updating the weights and biases of each neuron based on the gradient of the error with respect to those parameters. This process is repeated iteratively for a number of epochs or until the error converges to an acceptable level.
- **Gradient Descent Method for Backpropagation:**
	1. **Initialization**: Start by initializing the weights and biases of the neural network with random values.
	2. **Forward Pass**: Feed the input data through the network, layer by layer, to obtain the predicted output.
	3. **Calculate Loss**: Compute the error between the predicted output and the actual target output using a loss function, such as mean squared error or cross-entropy loss.
	4. **Backward Pass (Gradient Calculation)**: Propagate the error backward through the network to calculate the gradient of the loss function with respect to each weight and bias parameter. This is done using the chain rule of calculus, computing the partial derivatives of the loss function with respect to each parameter.
	5. **Update Parameters**: Adjust the weights and biases of the network in the opposite direction of the gradient, scaled by a factor called the learning rate. This step aims to minimize the loss function. The updated weights and biases are calculated using the gradient descent update rule:
		- <font color="#92d050">New Weight = Old Weight − Learning Rate × Gradient of Loss with respect to Weight</font>
			- New Weight = old weight - λ △J(θ) 
			- Here, λ = learning rate, △ = gradient, θ = loss function. 
		- <font color="#92d050">New Bias = Old Bias − Learning Rate × Gradient of Loss with respect to Bias.</font>
	6. **Repeat**: Repeat steps 2-5 for a fixed number of iterations (epochs) or until the loss converges to a satisfactory level.

## How to add layers in ANN using Keras library:
- Importing Necessary Modules
- Initializing the model
- Adding layers sequentially 
- Compiling the model 
- Output model at the end !!