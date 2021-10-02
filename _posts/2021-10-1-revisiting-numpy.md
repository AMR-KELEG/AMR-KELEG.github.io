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


TO BE CONTINUED!