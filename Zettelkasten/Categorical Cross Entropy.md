202211281600
Status: #note
Tags: [[Loss Function]], [[Classification]], 

# Categorical Cross Entropy

The Categorical Cross Entropy is a loss function which is used for a classification problem with more than 2 classes. Otherwise one would use [[Binary Cross Entropy]].

The mathematical definition is as follows

The implementaiton is tensorflow and python is as follows.
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

# References