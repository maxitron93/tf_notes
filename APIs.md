There are different APIs that let you build models at different levels

More info: https://www.tensorflow.org/guide

# tf.estimator
A high-level API that enables you to work at a much higher conceptual level than the base TensorFlow APIs.

Comes with many pre-made models and enables you to experiment with different model architectures by making only minimal code changes.

tf.estimator is also good for fast prototyping and to quickly establish baseline performance.

You can also create custom estimators.

More info: https://www.tensorflow.org/guide/estimator

# tf.keras
tf.keras is TensorFlow's implementation of the Keras API specification. This is a high-level API to build and train models that includes first-class support for TensorFlow-specific functionality, such as eager execution, tf.data pipelines, and Estimators.

In Keras, you assemble layers to build models. A model is (usually) a graph of layers.

More info: https://www.tensorflow.org/guide/keras/overview

# Low-level APIs
With the low level APIs you will be working with Tensors, Constant, Placeholders, Graphs, and session etc. directly.

<strong>FAQ</strong>: “When do I need to write low level TensorFlow code?” You only need to work at this low level if you are a student studying deep learning or researcher that needs greater control for your experiments; otherwise stick with the high level APIs.

# Eager vs Graph execution
Eager execution is an imperative programming environment that evaluates operations immediately, without building graphs. i.e. Operations return concrete values instead of constructing a computational graph to run later.

Eager execution makes TensorFlow much more intuitive and pythonic. However, eager execution can be slower than executing the equivalent graph as it can’t benefit from whole-program optimizations on the graph, and also incurs overheads of interpreting Python code.

<strong>Protip</strong>: Use Eager execution for research, and for production you should still use Graph execution. Note: <strong>AutoGraph</strong> lets you write graph code using natural Python syntax. More info: https://www.tensorflow.org/guide/function
