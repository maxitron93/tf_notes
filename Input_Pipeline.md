Managing input pipelines is important when you're working with a lot of data. i.e. More data than can fit in your amount of memory. In such cases, achieving peak performance requires an efficient input pipeline that delivers data for the next step before the current step has finished.

Note: When iterating over training data that fits in memory, feel free to use regular Python iteration. Otherwise, tf.data.Dataset is the best way to stream training data from disk.

# tf.data
The tf.data API helps to build flexible and efficient input pipelines. More info on how to use the tf.data API: https://www.tensorflow.org/guide/data

Guide for measuring input pipeline performance: https://www.tensorflow.org/guide/data_performance

The guide also includes best practices for designing performant TensorFlow input pipelines. <strong> Take a look when it becomes more relevant to you. </strong>

