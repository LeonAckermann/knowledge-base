[TowardsDataScience](https://towardsdatascience.com/convolutional-neural-networks-the-biologically-inspired-model-f2d23a301f71)
***
## History
- first convolutional network was proposed by Kunihiko Fukushima in 1980 with Neocognitron and described in his paper [Neocognitron...](https://www.cs.princeton.edu/courses/archive/spr08/cos598B/Readings/Fukushima1980.pdf) [Source](https://ai.stackexchange.com/questions/24921/are-convolutional-neural-networks-inspired-by-the-human-brain)
	- he was inspired by the work of Hubel and Wiesel about Receptive fields of single neurons  in his [Paper](https://www.cs.princeton.edu/courses/archive/spr08/cos598B/Readings/Fukushima1980.pdf)

**Biological inspiration**
- by seminal findings in visual neuroscience

**Inductive bias**
- the same object can occur anywhere, hence look for the same features everywhere

**Description**
- conv layers are divided into feature maps

## Characteristics

### Number of filters

### Kernel size
- (n,m) matrix
- smaller kernel sizes have less weights
- each kernel has $x*y*input-channels +1$ weights
- rather use more but smaller kernels

### Strides
- horizontal
- vertical

### Padding
- valid
- same

## Block
- multiple Conv2D layers of same size
- defined by image size and filter size
- 224 * 224 * 64

## Pooling
```python
tf.keras.layers.MaxPool2D
tf.keras.layers.AveragePooling2D
```
- reduce dimension from convolution to convolution layer
- pool_size
- strides
- padding
- max pooling reduces noise and computation and generally preferred

## Pooling to fully connected
```python
tf.keras.layers.Flatten
tf.keras.layers.GlobalAveragePooling2D
tf.keras.layers.GlobalMaxPool2D
```