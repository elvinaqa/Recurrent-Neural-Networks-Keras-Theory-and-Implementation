# Recurrent-Neural-Networks-Keras-Theory-and-Implementation
Recurrent Neural Networks with Keras

RNN - are used in SEQUENCES - such as, Time Series (Sales), Sentence (completion), Audio,  Car Trajectories, Music
Order is essential

For time series data,to know what history holds, (in order to predict future),output of neuron is also fed back to itself

Recurrent Neuron

RNNs have different kind of input and output formats and fully flexible in terms of that
Sequence to Sequence - Many to Many -> Give 5 words, predict next 5 words
Sequence to Vector - Many to One -> Give 5 words, predict next 1 word - Text Generation
Vector to Sequence - One to Many -> Give 1 words, predict next 5 words

Basic RNN's disadvantage is - it only remembers ONE step back, cant keep track of longer history

'''Backpropogation - when you go back to the input layer from the output layer in the end through hidden layers, changes in
weights and biases become so small that it doesnt modified at all - Gradient Vanishing'''

# The opposite happen in the feed-forward models, in the way to the output layer from input, gradient values becomes so
# significantly bigger that it change the values of bias and weights profoundly - Gradient Explotion

When n hidden layers use activation function like sigmoid, n small DERIVATIVES are multiplied together making the 
exponential descrease in the gradient values as the model backpropogates down to initial layers

Thus, it is all about activation functions - to fix this issue, we can edit activation function itself
Rectified Linear Unit is widely used since it doesnt saturate bigger values
Leaky RELU, Exponential RELU, 

# Another solution is to use batch normalization which is normalizing each batch based on batch mean and std deviation

# Gradient clipping is also used to put borders on gradient to prevent them becoming too big or too small
![Screenshot (178)](https://user-images.githubusercontent.com/57037068/83904097-54da7480-a770-11ea-9778-b33ace2bac00.png)


![Screenshot (179)](https://user-images.githubusercontent.com/57037068/83904089-5146ed80-a770-11ea-9ea9-00f152aa6846.png)


![lstm](https://user-images.githubusercontent.com/57037068/83904502-04afe200-a771-11ea-919f-289c8e454501.PNG)
