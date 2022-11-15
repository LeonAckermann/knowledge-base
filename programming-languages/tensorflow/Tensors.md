***
## Creating Tensors

```python
tensor = tf.constant(to_tensor, dtype=tf.float32)
```
==to_tensor== needs to be rectangular

```python
tensor = tf.ones(shape=(3,2))
tensor = tf.random.normal((3,2))
tensor = tf.random.uniform((4,3,2), minval= 0, maxval=100, dtype=tf.int32)
tensor = tf.range(1,101, dtype=tf.float32)
```

*** 
## Reshaping

```python
reshaped_tensor = tf.reshape(tensor, (20,5))
expanded_tensor = tf.expand_dims(tensor, axis=-1) # (m,n)->(m,n,1)
squeezed_tensor = tf.queeze(expanded_tensor, axis=None) # (1,20,1,20)->(20,20)
transposed_tensor = tf.transpose(reshaped_tensor)
permuted_tensor = tf.transpose(reshaped_tensor, perm=[1,0]) # (10,5,2)->(5,10,2
```

***
## Concatenating tensors

```python
A = tf.ones((128,12,12,15), dtype=tf.float32)
B = tf.zeros((128,12,12,35), dtype=tf.float32)

tf.concat([A,B], axis=-1)
```

***
## Reduce-operations in tensorflow
- we reduce the tensor by summing, multiplying, etc. over the specified dimension

```python
tensor = tf.ones((32,4,2))
feature_sum = tf.reduce_sum(tensor, axis=1) # (32,4,2)->(32,2)
batch_sum = tf.reduce_prod(tensor, axis=0)
total_sum = tf.reduce_mean(tensor, axis=None)
total_std = tf.math.reduce_std(tensor, axis=None)
```

***
## Matrix multiplication

```python
A = tf.ones((32,2,5))
B = tf.ones((32,5,10))

result = tf.matmul(A,B) # (32,2,5)@(32,5,10)->(32,2,10)
```

****
## Constants and variables

