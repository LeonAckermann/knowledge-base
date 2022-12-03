- in keras, a high-level library of tensorflow
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
