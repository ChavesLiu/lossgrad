# LOSSGRAD
This is an implementation of the LOSSGRAD optimization algorithm for PyTorch.
The algorithm has been implemented in the paper:
<TODO ARXIV LINK>


### Usage
Import the `lossgrad` module and simply wrap your SGD optimizer with `LossgradOptimizer` instance, e.g.:
```python
optimizer = LossgradOptimizer(torch.optim.SGD(net.parameters(), lr=1e-4), net, criterion)
```
and pass the required additional arguments to the optimizer's `step` method:
```python
optimizer.step(X, y, loss)
```

### Examples
A simple example for MNIST dataset is shown in
[mnist_example.py](https://github.com/bartwojcik/lossgrad/blob/master/mnist_example.py).

A more complicated example for an autoencoder trained on Fashion-MNIST (with figures and image samples) is shown in
[autoencoder_fmnist_example.py](https://github.com/bartwojcik/lossgrad/blob/master/autoencoder_fmnist_example.py).


### Citing
If you use the algorithm you can cite our paper:
<TODO PASTE BIBTEX ENTRY AFTER PUBLICATION>