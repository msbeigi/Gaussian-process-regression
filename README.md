

## Gaussian-process-regression
Gaussian Process (GP) is a probabilistic model used for regression and classification tasks. It is a nonparametric probabilistic approach for modeling data. Also, a flexible method that allows for the
representation of complex functions without making any assumptions about their shape or form. It uses a prior distribution over functions and updates this distribution based on observed data to
obtain the posterior distribution. GP is defined as a collection of random variables, any finite number of which have a joint Gaussian distribution. GP is defined by a mean function, which gives the
expected value of the output for each input, and a covariance function, which captures the similarity between the outputs for different inputs. The covariance function is usually parameterized by a set
of hyperparameters, which need to be optimized for the given data. The GP can learn the underlying patterns and correlations between inputs and outputs and make predictions for unseen inputs. The
GP can also provide estimates of uncertainty associated with each prediction, which is particularly useful when dealing with noisy data.

## requirements 
  ```
  openpyxl
  ```


## Implementation Guide
### Gaussian Process Model class:
The GaussianProcess class is defined to represent a Gaussian Process regression model.
The kernel method defines the covariance function (or kernel function) for the GP model. It's a combination of two sine terms with different periods and lengthscales.
The fit method trains the GP model on the training data (X_train and y_train) by calculating the covariance matrix and adding a small noise term for numerical stability.
The predict method predicts the mean and covariance of the output variable for a given input using the trained GP model.

### Adding Noise:
The line `y_noise = y_train + np.random.normal(loc=0, scale=0.1, size=X_train.shape[0])` adds Gaussian noise to the training data.
