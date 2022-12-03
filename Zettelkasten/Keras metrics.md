
202211291213
Status: #idea
Tags: [[Tensorflow]], [[Deep Learning]]

# Keras metrics
- keep track of the metrics like loss and acuracy
- Keras metrics allow us to do this very elegantly
- update_state() for updating
- reset_states() in each epoch

## Loss metric

```python
loss_metrics = tf.keras.metrics.Mean(name="loss")
loss_metric.update_state(values=loss)
```

## Accuracy metrics for binary classification

```python
binary_accuracy_metric = tf.keras.metrics.BinaryAccuracy(..)
categorical_accuracy_metric = tf.keras.metrics.CategoricalAccuracy()
binary_accuracy_metric.update_state(target, model_output)
binary_accuracy_metric.reset_states()
```






# References


