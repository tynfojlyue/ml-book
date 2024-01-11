```
conv1.weight: 250 trainable
conv1.bias: 10 trainable
conv2.weight: 5000 trainable
conv2.bias: 20 trainable
fc1.weight: 16000 trainable
fc1.bias: 50 trainable
fc2.weight: 500 trainable
fc2.bias: 10 trainable
```

* conv1.weight: 250 trainable：第一层卷积层的权重数量为 250，这些权重是可训练的。权重数量通常由输入通道数、输出通道数（也就是卷积核的数量）以及卷积核的大小决定。例如，如果这是一个具有 5 个输入通道、10 个输出通道（卷积核）和 `5x5` 大小卷积核的层，则权重总数将是 `5 * 10 * 5 * 5 = 250`。

* conv1.bias: 10 trainable：第一层卷积层的偏差数量为 10，这些偏差是可训练的。每个输出通道（卷积核）通常有一个偏差，所以这里有 10 个卷积核。

* conv2.weight: 5000 trainable：第二层卷积层的权重数量为 5000，这些权重是可训练的。这个数量暗示了这一层可能有更多的输入通道、输出通道或者更大的卷积核。

* conv2.bias: 20 trainable：第二层卷积层的偏差数量为 20，这些偏差是可训练的。这意味着这一层有 20 个输出通道。

* fc1.weight: 16000 trainable：第一个全连接层（或称为密集层）的权重数量为 16000，这些权重是可训练的。全连接层的权重数量是输入特征数乘以输出特征数。例如，如果这一层从前一层接收了 400 个特征，并输出 40 个特征，则权重总数为 `400 * 40 = 16000`。

* fc1.bias: 50 trainable：第一个全连接层的偏差数量为 50，这些偏差是可训练的。偏差的数量通常等于该层的输出特征数。

* fc2.weight: 500 trainable：第二个全连接层的权重数量为 500，这些权重是可训练的。与第一个全连接层类似，权重数量取决于前一层的输出特征数和当前层的输出特征数。

* fc2.bias: 10 trainable：第二个全连接层的偏差数量为 10，这些偏差是可训练的。这意味着这一层输出 10 个特征。

```
Input
  |
  v
[Conv1]---(250 weights)---[10 biases]
  |
  v
[Conv2]---(5000 weights)---[20 biases]
  |
  v
[Flatten]
  |
  v
[FC1]---(16000 weights)---[50 biases]
  |
  v
[FC2]---(500 weights)---[10 biases]
  |
  v
Output
```
