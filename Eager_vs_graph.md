# Eager vs Graph execution
Eager execution is an imperative programming environment that evaluates operations immediately, without building graphs. i.e. Operations return concrete values instead of constructing a computational graph to run later.

Eager execution makes TensorFlow much more intuitive and pythonic. However, eager execution can be slower than executing the equivalent graph as it can’t benefit from whole-program optimizations on the graph, and also incurs overheads of interpreting Python code.

<strong>Protip</strong>: Use Eager execution for research, and for production you should still use Graph execution. Note: <strong>AutoGraph</strong> lets you write graph code using natural Python syntax. More info: https://www.tensorflow.org/versions/r2.0/api_docs/python/tf/autograph

# tf.function
In TensorFlow 2.0, eager execution is turned on by default. The user interface is intuitive and flexible (running one-off operations is much easier and faster), but this can come at the expense of performance and deployability.

To get peak performance and to make your model deployable anywhere, use tf.function to make graphs out of your programs. Thanks to AutoGraph, a surprising amount of Python code just works with tf.function, but there are still pitfalls to be wary of.

More info: https://www.tensorflow.org/guide/function


