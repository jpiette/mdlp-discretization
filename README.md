# Minimum Description Length Binning

This is an implementation of Usama Fayyad's entropy based
expert binning method.

Please read the original paper
<a href="http://sci2s.ugr.es/keel/pdf/algorithm/congreso/fayyad1993.pdf">here</a>.
for more information

# Tests

Feel free to run the tests using `nose`.
```
cd tests
nosetests test_mdlp
```

# Installation and Usage

This code was built using Cython, so you have to run the makefile
in the directory.
```
$ make
```

Afterwards, assuming that `discretization.py` and `_mdlp.so` are in the
same directory, you can import the MDLP class.

```
>>> from discretization import MDLP
>>> from sklearn.datasets import load_iris
>>> iris = load_iris()
>>> X = iris.data
>>> y = iris.target
>>> mdlp = MDLP()
>>> conv_X = mdlp.fit_transform(X, y)
```
