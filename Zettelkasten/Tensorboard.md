- comes with tensorboard
```python
# load in jupyter notebook with
%load_ext tensorboard
```

```python
file_path = ""
summary_writer = tf.summary.ceate_file_writer(file_path)
```

- write the data
- use summary write as [[Context Managers]]
```python
with summary_writer.as_default():
	# write scalar in summary, could be other types like images, text, etc
	# step is most often an epoch
	tf.summary.scalar(name="loss", data=loss, step=i)
```

- open tensorboard
```python
# open tensorboard and specifying the directory
%tensorboard --logdir test_logs/
```

