- network architecture is determined -> inductive bias
- interconnected sets of units
- perceptual or cognitive computations are collective property of network

## History
[AI.stackexchange](https://ai.stackexchange.com/questions/24921/are-convolutional-neural-networks-inspired-by-the-human-brain)
[TowardsDataScien e](https://towardsdatascience.com/neural-network-architectures-156e5bad51ba)
[IBM](https://www.ibm.com/cloud/learn/convolutional-neural-networks)
[[@minarRecentAdvancesDeep2018]]
- Neocognitron (1980)
- LeNet5 (1994)
- Can Ciresan Net (GPU Neural Nets)(2010)
- AlexNet (2012)
- Overfeat (2013)
- VGG ()
- Network-in-network (NiN)
- GoogleLeNet (2014)
- Inception V2/3 (2015)
- ResNet (2015)
- Inceeption V4
- SqueezeNet
- ENet
- Xception
- MobileNets
- [[CapsNet]] (Sabour et al. , 2017)
- [[Memory Networks]] (Weston et al., 2014)
- [[Augemented Neural Networks]]
- [[Long Short-Term Memory (LSTM)]] (Hochreiter and Schmidhuber, 1997)

## Layers
[Source1](https://towardsdatascience.com/neural-network-architectures-156e5bad51ba)
- [[Convolutional Layer]]
- Pooling
- Non-linearity
- Bottleneck
- Fully-connected
- Residual

## Architectures
- Feed Forward Neural netowrk
- Deep Convolutional Neural Netowrk
- 3-dimensional convolutional neural networks
- DenseNet
- ResNet

## Objective function, Losses
- model is updated through learning rule which minimizes the objective function
- this is only true for unsupervised and reinforcement learning but NOT for supervised learning
- Regression
	- MSE
- Classification
	- Binary Cross Entropy
	- Categorical Cross Entropy

## Optimization algorithms
[source 1](https://ruder.io/optimizing-gradient-descent/index.html#adam)
[slides](https://www.slideshare.net/SebastianRuder/optimization-for-deep-learning)
- Momentum
- AdaGrad
- RMSProp
- Adam

## Activation functions
- sigmoid
- tanh
- ReLU
- softmax







**They use different learning algorithms to adjust the weights of the network**
finding the matching learning rule is very hard because of the number of parameters. Learning rules have their own hyperparameters
- [[Backpropagation]]

**The objective function tells the ANN in what direction to change the output**

