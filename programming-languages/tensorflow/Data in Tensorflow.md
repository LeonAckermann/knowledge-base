***
## Importing Data and datasets

#### ==tdfs.load()==
#tdfs_method

```python
import tensorflow_datasets as tfds
train_ds, test_ds = tfds.load('mnist', 
							  split=['train', 'test'], 
							  as_supervised=True)
```
==split== sets which split of data to read 
==as_supervised=True== returns a tuple ==(features, labels)==
==data_dir== is the location of the data and default is ==/tensorflow_datasets/==

***
## Preparing data

#### ==map()==
```python
mnist = mnist.map(lambda img, target: (tf.reshape(img, (-1)), target))
```
map from ==img== to ==target== and return target

***
## Tensor transformations with map and lambda
#tf_method

```python
tf.reshape(img, dimension)
tf.cast(img, tensortype)
tf.one_hot(img, depth)
```
