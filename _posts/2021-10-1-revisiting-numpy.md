---
layout: post
title: My two cents on numpy broadcasting
date: 2021-10-2
description: 
---

Numpy is the go-to library that one generally uses in order to speedup heavy computations in python.
However, one needs to be knowledgable of different numpy tips and tricks to make full use of it. One of these tricks is broadcasting.

## Shape of numpy arrays
Broadcasting is generally used to perform operations between variables of different shapes. But, before diving into it, let's familiarize first with how shapes of variables are represented

#### Example 1
```python
import numpy as np

# 1) A scalar
s = np.array(1)
print(s.shape) # ()

# 2) A 1D array
a = np.array([1, 2, 3])
print(a.shape) # (3,)

# 3) A row vector
v = np.array([[1, 2, 3]])
print(v.shape) # (1, 3)
```

Things start to get tedious once we start seeing something like:
```python
import numpy as np

arr = np.array(
    [[[[1], [2]], [[3], [4]], [[5], [6]]], [[[7], [8]], [[9], [10]], [[11], [12]]]]
)
```

It's easy to confuse yourself looking at such multi-dimensional array. Knowing the shape of the underlying numpy array is cruicial for knowing how other operations like broadcasting, and indexing will work.
The way I found is to start from the deepest level lists (i.e.: [1] or [2] or ...). The length of such lists is 1, and thus the shape of the numpy array is (????, 1).
The next step is to look at the next level list (i.e.: [ [1], [2] ] or [ [3], [4] ] or ...). Ignore the values in the inner lists and just count the number of lists inside the outer list. For this example, we have two inner lists which makes the shape of the numpy array (????, 2, 1).

