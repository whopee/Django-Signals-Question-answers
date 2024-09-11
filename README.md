# Django Signals and Python Classes

This repository contains code examples and answers to questions about Django signals and Python custom classes.

## Django Signals

### Question 1: Are Django signals synchronous or asynchronous?
Since Django signals are executed synchronously by default, the message "Model saved!" will only be printed after the signal handler finishes. This proves that signals are synchronous by default.


### Question 2: Do Django signals run in the same thread as the caller?
Yes, Django signals run in the same thread as the caller.


### Question 3: Do Django signals run in the same database transaction as the caller?
Yes, Django signals run in the same database transaction as the caller if the signal is connected to a database-related action.


## Python Custom Class

### Rectangle Class

```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def __iter__(self):
        yield {'length': self.length}
        yield {'width': self.width}

# Example:
rect = Rectangle(10, 20)
for dimension in rect:
    print(dimension)
```
