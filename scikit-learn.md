scikit-learn Core API

All objects contain share common API consisting of 3 interfaces:

1. Estimator: For building and fitting the models

2. Predictor: For making predictions

3. Transformer: For converting data

Data representation: Data sets are encoded as NumPy multidimensional arrays for dense data and as SciPy sparse matrices for spase data.

Estimator Interface: For building and fitting the models

- Classical learning algorithms are objects to be implemented as estimators
- Exposese a fit method for learning a model from training data.
- The constructor just attaches the data given to the object.
- Learned parameters are exposed as public attributes with names suffixed with a trailing underscore (e.g., coef_)
- Always returns the estimator object it was called onm which now serves as model and can be used to perform predictions.

Predictor Interface: For making predictions

- Predictor method takes an array(X_test) and produces predictions(Y_test) based on learner parameters of estimator.
- Predictors may implement methods that quantify the confidence of predictions like decision_function; predic_proba...
- Predictors provide score function to assess the performance of the predictors. This higher the score the better.

Transformer Interface: For converting data

- For the common neeed to modifyor filter data before feeding it to a learning algorithm. Takes X_test data and yealds tranformed version of X_test
- Preprocessing; feature selection; feature exraction and dimensionality reduction algorithms are all provided as transformers with in the library.
