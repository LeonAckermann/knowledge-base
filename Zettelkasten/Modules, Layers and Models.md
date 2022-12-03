***
## The Module Class
- organizes variables very neatly

```python
class MyModule(tf.Module):

	def __init__(self, input_dim, output_dim, name=None):
		super(MyModule, self).__init__(name=name)
		self.submodule_1 = MyModule(input_dim = input_dim, 
								output_dim = 10,
								name="layer1")

		self.submodule_2 = MyModule(input_dim = input_dim,
									output_dim = output_dim,
									name="layer2")
	
	@tf.function # was bedeuted das?
	def __call__(self, inputs, training=False):
		x = self.submodule_1(inputs, training)
		ouptut = self.submodule_2(x, training)

		return ouptut
```

***
## The Layer Class
- inherits from the Module Class
- adds a lot more functionality
- adding and collection regularization losses  -> look up
- metrics and bookkeeping
- access submodules in structured way 

```python
class Dense(tf.keras.layers.Layer):
	def __init__(self, n_units, activation_function, **kwargs):
		super(Dense, self).__init__(**kwargs)
		# no variables created as they get created with build method
		self.n_units = n_units
		self.activation_function = activation_function

	# create weights and bias after input shape is clear
	def build(self, input_shape):
		self.w = tf.Variable(tf.random.normal([input_shape[-1], self.n_units],
							name="weights"))
		self.b = tf.Variable(tf.zeors([self.n_units]), name="bias")

	def call(self, inputs):
		x = inputs @ self.w + self.b
		return self.activation_function(x)

dense_layer = Dense(n_units=10, activation_function=tf.nn.relu)
```

***
## The Model Class
- fit method to do the training
- compile the model with metrics, loss and optimizer
- save models weights, if there is some interruption during training
- access all layers in the model
- 