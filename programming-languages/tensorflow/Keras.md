- high-level library of tensorflow
- tensorflow became integrated within keras

***
## Loss functions
- in **tf.keras.losses** 

***
### Mean squared error
#loss-function 

```python
BATCH_SIZE = 8
N_PREDICTED_FEATURES = 5

targets = tf.random.uniform(BATCH_SIZE, N_PREDICTED_FEATURES)
predictions = tf.random.uniform(BATCH_SIZE, N_PREDICTED_FEATURES)

mse_loss = tf.keras.losses.MeanSquaredError()
mean_squared_error = mse_loss(targets, predictions)
print(f"MSE error for the batch:\n {mean_squared_error.numpy()} \n")
```

***
### Categorical CrossEntropy 
#loss-function
#activation-function

```python
labels = [[0,1,0],
		 [0,0,1],
		 [1,0,0],
		 [1,0,0],
		 [0,1,0]]

labels = tf.constant(labels, dtype=tf.float32)
logits = tf.random.normal(labels.shape) # "logits" often called input of softmax

# turn network output into categorical probability, more in [[Softmax]]
predictions = tf.nn.softmax

# calculate catigorical crossentropy
CCE_loss = tf.keras.losses.CategoricalCrossentropy()
batch_loss = CCE_loss(labels, predictions)
```

***
### Binary CrossEntropy
#loss-function 

```python
labels = [1,
		 0,
		 0,
		 1,
		 0,
		 0,
		 1,
		 0,]
labels = tf.constant(lables, dtype = tf.float32)
predictions = tf.random.uniform(labels.shape)

BCE_loss = tf.keras.losses.BinaryCrossentropy()
batch_loss = BCE_loss(labels, predictions)
```

***
## Optimizers
#optimizer

- **tf.keras.optimizers**
- optimize the process of updating the gradients 

```python
optimizer = tf.keras.optimizers.SGD(learing_rate=0.005,
								   momentum=0)
# everything in between

# gradients and [paramteter_estimate] need to be of same shape
optimizer.apply_gradients(zip(gradients, [paramter_estimate])) 
