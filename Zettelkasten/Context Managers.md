***
## GradientTape

- calculate loss between targets and predictions with GradienTape context manager

```python
def model(x, paramter):
	return x*paramter
```

```python
X = tf.random.uniform((20,1), minval=0, maxaval=10)
Y = X + np.pi
```

```python
paramter_estimate = tf.Variable(7.5, trainable=True, dtype=tf.float32)
learning_rate = tf.constant(0.005, dtype=tf.float32)
```

```python
for epoch in range(2):

	# interate over training examples
	for x,y in zip(X,Y):

		with tf.GradientTape() as tape:
			prediction = model(x, paramter_esmtimate) 
			loss = (prediction - y)**2 # loss needs to be a scalar

	gradients = tape.gradient(loss, [paramteter_estimate])
	new_parameter_val = paramter_estimate - learning_rate * gradients
	paramter_estime.assign(new_paramter_val[0])
```

***
## NameScope

```python
with tf.name_scope(name) as scope:
	self.weights = tf.Variable(tf.random.normal(shape=(input_dim, output_dim)),
								trainable=True,
								name="weights")
								
	self.bias = tf.Variable(tf.random.normal(shape=(input_dim, output_dim)),
								trainable=True,
								name="bias")
```

