# Gradient Descent Scalability Experiments

In this assignment, you will study how the Gradient Descent algorithm for linear regression scales with:

1. The number of data points (dataset size)  
2. The number of features (data dimensionality)

You will complete the missing parts of the code and run experiments that visualize how convergence behavior and runtime change as the problem size increases.


## Objective

The goals of this assignment are to:

- Implement Full Batch Gradient Descent for linear regression.
- Measure how many iterations are required for convergence as data size increases.
- Measure how runtime changes as the number of features increases.

1. Data Generation

The function `generate_data(n, d)` creates a synthetic regression dataset using the model:

\[
y = X w_{true} + \text{noise}
\]

where:
- \(n\) = number of data points  
- \(d\) = number of features  

2. Loss Function

The function `f(w, X, y)` computes the Mean Squared Error:

\[
f(w) = \frac{1}{n}\sum_{i=1}^n (y_i - X_i w)^2
\]

3. Gradient of the Loss

The function `df(w, X, y)` computes the gradient:

\[
\nabla f(w) = -\frac{2}{n} X^T (y - Xw)
\]

This is the direction of steepest increase of the loss. Gradient Descent moves in the opposite direction.

4. Gradient Descent (To Be Implemented)
    - You must complete the function `gradient_descent(X, y, lr, tol, max_epochs)`
    - For each step, compute the loss and its gradient and update the weights using:
```
w = w − lr * ∂f(w)/∂w
```
    - Stop when the change in loss is smaller than tol.

5. Plotting
The function plot_graphs(...) is provided to visualize results.

## Experiments

### Experiment 1: Convergence vs Data Size
    - Measures the number of gradient descent iterations are required to converge, as the number of data points varies.


### Experiment 2: Runtime vs Number of Features
    - Should measure the total time taken for gradient descent to converge when the number of features vary.
    - This needs to be implemented.

Note: You are encouraged to design and include additional experiment beyond those provided to further explore the behavior and scalability of gradient descent.