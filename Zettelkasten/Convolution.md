202212010739
Status: #note
Tags: [[Convolutional Layer]], [[Deep Learning]]

# Convolution

>[!Definition]
>A convolution is a mathematical function. The motivation it is to obtain a less noisy result from the measurement. The convolution is commulative.
>$$s(t)=(x*w)(t)$$
>$$input = x; kernel = w; featuremap = s(t)$$
>(Goodfellow et al, 2016, p.322)

>[!Motivation]-
>The convolution can improve the neural network by enabling **sparse internactions**, **paramtere sharing** and **equivariant representations**.

>[!Sparse interactions]-
>Also referred to as sparse connectivity or sparse weights. This is accomplished by making the kernel is smaller than the input. The result would we less weights than in a traditional weight matrix.

>[!Bias]-
>A convolution assumes that similar features emerge in different positions and the layer should only learn local features. This could possibly underfitting if the prior doesn't translate to nature of the data (Goodfellow et al, 2016, p.336).

# References
dfhjd



