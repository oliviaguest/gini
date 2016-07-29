# gini
Calculate the Gini coefficient of a numpy array.

##Examples


For a very unequal sample, 999 zeros and a single one:

```
>>> from gini import *
>>> a = np.zeros((1000))
>>>  a[0] = 1.0
```

The Gini coefficient is very close to 1.0:

```
>>> gini(a)
0.99890010998900103
```

For uniformly distributed random numbers:
