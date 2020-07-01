# Google ML Crash Note

## Hyperparameter Tuning

here are a few rules of thumb:

* Training loss should steadily decrease, steeply at first, and then more slowly until the slope of the curve reaches or approaches zero.
* If the training loss does not converge, train for more epochs.
* If the training loss decreases too slowly, increase the learning rate. Note that setting the training loss too high may also prevent training loss from converging.
* If the training loss varies wildly (that is, the training loss jumps around), decrease the learning rate.
* Lowering the learning rate while increasing the number of epochs or the batch size is often a good combination.
* Setting the batch size to a very small batch number can also cause instability. First, try large batch size values. Then, decrease the batch size until you see degradation.
* For real-world datasets consisting of a very large number of examples, the entire dataset might not fit into memory. In such cases, you'll need to reduce the batch size to enable a batch to fit into memory.

Remember: the ideal combination of hyperparameters is data dependent, so you must always experiment and verify.


