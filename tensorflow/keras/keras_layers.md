Dense layer is also known as Fully connected layer. All the neurons of the FC layer are connected to every neuron in the preceding layer.

### A Sequential model is not appropriate when:
* Your model has multiple inputs or multiple outputs
* Any of your layers has multiple inputs or multiple outputs
* You need to do layer sharing
* You want non-linear topology (e.g. a residual connection, a multi-branch model)

Once a Sequential model has been built, it behaves like a Functional API model. This means that every layer has an input and output attribute.
