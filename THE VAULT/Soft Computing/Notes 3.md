## AlexNet Layers
- **Definition :**
	- Alex Net is a significant convolutional neural network (CNN) architecture developed by Alex Krizhevsky and his colleagues. It consists of 8 layers, with the first 5 being convolutional layers and the last 3 being fully connected layers.
- **The key components of AlexNet's architecture include:**
	- <font color="#ffc000">Convolutional Neural Network :</font>
		- AlexNet is a deep CNN designed for image classification tasks, leveraging convolutional layers to learn hierarchical features from images.
	- <font color="#ffc000">Architecture :</font> 
		- The network comprises five convolutional layers with filter sizes of 11x11, 5x5, and 3x3, followed by max-pooling layers to reduce spatial dimensions. It also includes three fully connected layers for classification.
	- <font color="#ffc000">ReLU activation : </font>
		- AlexNet uses the Rectified Linear Unit (ReLU) activation function, known for its superior performance compared to traditional activation functions like sigmoid and tanh.
	- <font color="#ffc000">Transfer Learning : </font>
		- AlexNet can be used with transfer learning by utilizing pre-trained weights on the ImageNet dataset to achieve exceptional performance.
- AlexNet is a pioneering CNN architecture that revolutionized the field of computer vision, particularly in image classification tasks, by introducing deep learning techniques that significantly improved accuracy and efficiency in large-scale image recognition challenges.

## RNN 
- **Definition:** 
	- Recurrent Neural Network (RNN) are a type of artificial neural network, what is incorporates feedback loops, allowing information to persist. They are unrolled or unfolded through time, enabling them to retain memory of past inputs. 
- **Feedback Loop:**  
	- In RNNs, the feedback loop ensures that the output of one cell becomes an input for the same cell, creating a memory mechanism. This feedback loop distinguishes RNNs from traditional feedforward neural networks, enabling them to retain historical information and learn patterns based on context.
- **Unrolling:**  
	- Unrolling an RNN involves visualizing the network over multiple time steps, where each step represents a past observation. This unrolling process helps in understanding how information flows through the network and how the network can be seen as a sequence of interconnected neural networks.
- **Types of RNN:**
	- <font color="#ffc000">Traditional RNN:</font>  
		- Traditional RNNs utilize feedback loops to retain short-term memory, allowing them to process sequential data. They are simple in design and are the foundation for more advanced RNN architectures. However, they can struggle with long sequences and vanishing gradient issues, which can cause them to forget important information.
	- <font color="#ffc000">LSTM:</font> 
		- Long Short-Term Memory (LSTM) networks address vanishing gradient issues and maintain long-term dependencies by incorporating memory cells and gates. These gates, including the input, forget, and output gates, allow LSTMs to selectively remember or forget information from the input sequence, making them more effective for long-term dependencies.
	- <font color="#ffc000">GRU:</font> 
		- Gated Recurrent Unit (GRU) networks offer a simpler design than LSTM while still addressing vanishing gradient problems. GRUs combine the reset and update gates to selectively update their internal state based on the input sequence, allowing them to maintain long-term dependencies.
- **Applications:**  
	- RNNs find applications in various fields due to their ability to handle sequential data and remember past information. Some common applications include:
		- Speech recognition
		- Music generation
		- DNA sequence analysis
		- Machine translation
		- Time series prediction

## LSTM 
- **Definition :**
	- Long Short-Term Memory (LSTM) is a type of Recurrent Neural Network (RNN) that uses memory cells to retain information over long periods, addressing the vanishing and exploding gradient problems typically found in traditional RNNs. LSTMs are powerful in modeling sequential data due to their ability to control the flow of information across time steps.
- **Memory Cell :** 
	- The LSTM cell also has a memory cell that **stores information from previous time steps and uses it to influence the output of the cell at the current time step**. The output of each LSTM cell is passed to the next cell in the network, allowing the LSTM to process and analyze sequential data over multiple time steps.
- **Gates :** 
	- **Forget Gate (`ft`) :** 
		- Controls the flow of information out of the memory cell. The forget gate determines what information should be discarded from the cell state. The forget gate's activation function is also a sigmoid function, which outputs a value between 0 and 1, indicating the level of information to be forgotten from the cell state.
		- <font color="#ffc000">Equation :</font> 
			- ft ​= σ(Wf​⋅[ht−1​,xt​]+bf​), 
				- Where  `W_i` and `b_i` are the weights and bias for the input gate.
				- `h_{t-1}` is the previous hidden state. 
				- `x_t` is the input at the current time step.
				- `sigma` is the sigmoid activation function.
	- **Input Gate (`i_t`) :**
		- The input gate controls which new information should be added to the memory cell.
		- <font color="#ffc000">Equation :</font> 
			- it ​= σ(Wi​⋅[ht−1​,xt​]+bi​), where  `W_i` and `b_i` are the weights and bias for the input gate.
	- **Output Gate (`o_t`) :** 
		- Controls the flow of information out of the memory cell to the hidden state. The output gate determines what information should be used as the hidden state's output. The output gate's activation function is typically a sigmoid function, which outputs a value between 0 and 1, indicating the level of information to be output from the cell state.
		- <font color="#ffc000">Equation : </font>
			- ot ​= σ(Wo​⋅[ht−1​,xt​]+bo​)
- **Cell Candidate:** Determines the new candidate values to be added to the cell state. The cell candidate's activation function is typically a hyperbolic tangent (tanh) function, which outputs a value between -1 and 1, indicating the level of new information to be added to the cell state.
- **Cell State:** The cell state is the internal memory of the LSTM cell, which stores information over long periods. The cell state is updated using the input gate, forget gate, and cell candidate.
- **Hidden State:** The hidden state is the output of the LSTM cell, which is used as input for the next cell in the sequence. The hidden state is updated using the output gate and the cell state.

## GRU (Gated Recurrent Units) 
- GRU networks offer a simpler design than LSTM while still addressing vanishing gradient problems. GRUs combine the reset and update gates to selectively update their internal state based on the input sequence, allowing them to maintain long-term dependencies.
- **Difference b/w LSTM and GRU :**
	- 1. **Architecture : **
	    - **LSTM**: LSTMs have three gates: input, output, and forget gates, along with a cell state that maintains long-term memory. The gates control the flow of information into and out of the cell state, allowing the network to learn what information to keep and what to discard.
	    - **GRU**: GRUs have two gates: an update gate and a reset gate. GRUs do not have a separate cell state; instead, they combine the cell state and hidden state into one state.
	2. **Complexity :** 
		- **LSTM**: LSTMs are more complex due to their three gates and additional cell state.
		- **GRU**: GRUs are simpler, with only two gates and no separate cell state, which may result in faster training and fewer parameters.
	3. **Performance :**  
		- Both GRUs and LSTMs perform well on various sequence modeling tasks, and their performance can depend on the specific dataset and problem.
		- In some tasks, LSTMs may perform slightly better due to their ability to maintain long-term dependencies, while GRUs may be faster to train and less prone to overfitting.
	4.  **Training Efficiency :**
	    - GRUs are generally faster to train and require fewer parameters than LSTMs because of their simpler architecture. This can be advantageous when working with limited computational resources.
	5. **Applications :**
		- LSTMs are widely used in applications requiring long-term dependencies, such as language modeling and time series prediction.
		- GRUs can be more suitable for tasks where computational efficiency is important, such as real-time applications and edge devices.
- In summary, while both LSTMs and GRUs are powerful architectures for sequence modeling, GRUs offer a simpler and faster alternative to LSTMs, though LSTMs may have a slight edge in tasks requiring long-term memory. The choice between them often depends on the specific problem, dataset, and resource constraints.

## Vanishing Gradient 
- **Definition** 
	- The vanishing gradient problem occurs when the gradients (i.e., partial derivatives of the loss function with respect to the model's parameters) become very small as they are propagated back through the network.
- **Effect** 
	- When gradients vanish, the weights in earlier layers or earlier time steps are updated very slowly, if at all. This can lead to slow or stalled training and difficulty learning long-range dependencies in the data.
- **Solution**
	- Architectures like LSTMs and GRUs are designed to mitigate the vanishing gradient problem by using gating mechanisms that control the flow of information and help maintain gradients over time.

## **Exploding Gradient**:
- **Definition** 
	- The exploding gradient problem occurs when the gradients become very large during backpropagation, causing large updates to the model's parameters.
- **Effect** 
	- When gradients explode, the model's parameters may change drastically with each training step, leading to instability and potentially causing the model to diverge or become unable to converge to a good solution.
- **Solution**
	- Techniques such as gradient clipping, where the gradients are limited to a specific range, can help prevent exploding gradients and maintain stable training.

## Keras 
- Keras is a high-level deep learning library, you can build various neural network architectures for tasks such as image classification, sequence modeling, and more. Here are explanations of the common functions and layers you mentioned :
	- **`Sequential`**
		- The `Sequential` class in Keras is a simple and linear stack of layers. You can create a neural network by adding layers one after another in sequence.
		- Example : 
			- <font color="#3dbf1c">from keras.models import Sequential</font> 
			- <font color="#3dbf1c">model = Sequential()</font>
	- **`Dense` function**
		- The `Dense` layer is a fully connected layer in which each neuron is connected to every neuron in the previous layer. It applies a linear transformation to the input and then a non-linear activation function.
		- Example : 
			- <font color="#3dbf1c">from keras.layers import Dense</font>
			- <font color="#3dbf1c">model.add(Dense(units=64, activation='relu', input_shape=(input_shape,)))</font>
	- **`Conv2D` layer**
		- The `Conv2D` layer is a convolutional layer that applies 2D convolution operations on images or spatial data. It is commonly used in image processing and computer vision tasks.
		- Example : 
			- <font color="#3dbf1c">from keras.layers import Conv2D</font>
			- <font color="#3dbf1c">model.add(Conv2D(filters=32, kernel_size=(3, 3), activation='relu', input_shape=(height, width, channels)))</font>
	- **`model.fit()`**
		- The `fit()` method is used to train the model on the given data. It takes the input data and target labels as arguments and adjusts the model's weights through backpropagation.
		- Example : 
			- <font color="#3dbf1c">model.fit(X_train, y_train, epochs=10, batch_size=32, validation_data=(X_val, y_val))</font>
<font color="#3dbf1c"> </font>
## How deep learning used for text summarising, covid 19
- 