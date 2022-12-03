202211281604
Status: #idea
Tags: [[Loss Function]]

# Binary Cross Entropy


202212030758
Status: #idea
Tags: 

# Binary Cross Entropy

>[!Definition]

>[!Motivation]



# References

Binary Cross Entropy is a loss function which is used for a [[Classification]] problem with 2 classes. 

I still need to add the mathematical definition. Or it can be found in the internet.

Python impelementation is as follows.
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



# References