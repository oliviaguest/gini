# gini
Calculate the Gini coefficient of a numpy array.

The function in ```gini.py``` is based on the third equation from [here](http://www.statsdirect.com/help/default.htm#nonparametric_methods/gini.htm), which defines the Gini coefficient as:

![G = \dfrac{ \sum_{i=1}^{n} (2i - n - 1) x_i}{n  \sum_{i=1}^{n} x_i}](https://github.com/oliviaguest/gini/raw/master/gini.png "Gini equation")


##Examples
For a very unequal sample, 999 zeros and a single one:

```
>>> from gini import *
>>> a = np.zeros((1000))
>>> a[0] = 1.0
```

The Gini coefficient is very close to 1.0:

```
>>> gini(a)
0.99890010998900103
```

For uniformly distributed random numbers, it will be low, around 0.33:

```
>>> s = np.random.uniform(-1,0,1000)
>>> gini(s)
0.3295183767105907
```

