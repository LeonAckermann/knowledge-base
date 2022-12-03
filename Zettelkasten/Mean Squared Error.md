202211281558
Status: #idea
Tags: [[Loss Function]]

# Mean Squared Error

Mean Squared Error is a loss function after which the neural network is optimizing its weights.

This is the implementation in python with tensorflow.
```python
BATCH_SIZE = 8
N_PREDICTED_FEATURES = 5

targets = tf.random.uniform(BATCH_SIZE, N_PREDICTED_FEATURES)
predictions = tf.random.uniform(BATCH_SIZE, N_PREDICTED_FEATURES)

mse_loss = tf.keras.losses.MeanSquaredError()
mean_squared_error = mse_loss(targets, predictions)
print(f"MSE error for the batch:\n {mean_squared_error.numpy()} \n")
```



# References