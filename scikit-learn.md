scikit-learn Core API

All objects contain share common API consisting of 3 interfaces:

1. Estimator: For building and fitting the models

2. Predictor: For making predictions

3. Transformer: For converting data

Data representation: Data sets are encoded as NumPy multidimensional arrays for dense data and as SciPy sparse matrices for spase data.

Estimator: For building and fitting the models

- Exposese a fit method for learning a model from training data.
- The constructor just attaches the data given to the object.
