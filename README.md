# label.vuecli

`label.vuecli` is a Python library which makes fast HTTP router with zero dependencies easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `label.vuecli`, clone and install requirements:

```
git clone https://github.com/user/label.vuecli
cd label.vuecli
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model kubernetes --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - modern

```python
from label.vuecli import models

model = models.modern(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| kubernetes | **78.61** | [Code](#), [Paper](#) |
| modern | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

