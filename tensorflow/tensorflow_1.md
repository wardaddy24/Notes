### Why graphs?
* Automatic Differentiation
* Deployment to a python-free server, phone
* Graph-based optimizations(CSE,layout,etc)
* Compilation,kernel fusion, layout selection
* Automatic distribution to 100s of machines

### Why eager execution ?
* TensorFlow's eager execution is an imperative programming environment that evaluates operations immediately, without building graphs: operations
return concrete values instead of constructing a computational graph to run later. 
 * Functionality of the host language is available while your model is executing.
 * tf.compat.v1.disable_eager_execution()
