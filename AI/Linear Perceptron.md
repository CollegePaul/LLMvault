### Linear Perceptron

A Linear Perceptron is a type of artificial neural network used primarily for binary classification tasks. It operates by taking a set of input features, multiplying each feature by a corresponding weight, summing these products, and then applying an activation function (typically a step function) to determine the output class. The linear perceptron learns the optimal weights through a process called supervised learning, where it iteratively adjusts the weights based on the error between predicted and actual outputs.

The basic structure of a Linear Perceptron consists of:
- **Input Layer**: Contains neurons representing input features.
- **Weights**: Each input is associated with a weight that determines its importance in the decision-making process.
- **Bias**: An additional constant term that allows the model to fit data that does not pass through the origin.
- **Output Layer**: A single neuron that applies the activation function to the weighted sum of inputs plus bias.

The learning algorithm for a Linear Perceptron is straightforward:
1. Initialize weights and bias randomly or to zero.
2. For each training example, compute the predicted output by applying the linear combination of inputs and weights followed by the step function.
3. Update the weights and bias based on the error (difference between actual and predicted outputs).
4. Repeat steps 2-3 for a fixed number of iterations or until convergence.

Here is a simple example using Python to implement a Linear Perceptron from scratch:

```python
import numpy as np

# Step function for activation
def step_function(x):
    return 1 if x >= 0 else 0

# Linear Perceptron class
class LinearPerceptron:
    def __init__(self, learning_rate=0.1, epochs=100):
        self.learning_rate = learning_rate
        self.epochs = epochs
        self.weights = None
        self.bias = None
    
    def fit(self, X, y):
        n_samples, n_features = X.shape
        self.weights = np.zeros(n_features)
        self.bias = 0
        
        for _ in range(self.epochs):
            for idx, x_i in enumerate(X):
                linear_output = np.dot(x_i, self.weights) + self.bias
                y_predicted = step_function(linear_output)
                
                # Update rule
                update = self.learning_rate * (y[idx] - y_predicted)
                self.weights += update * x_i
                self.bias += update
    
    def predict(self, X):
        linear_output = np.dot(X, self.weights) + self.bias
        y_predicted = step_function(linear_output)
        return y_predicted

# Example usage
if __name__ == "__main__":
    # AND gate example
    X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]])
    y = np.array([0, 0, 0, 1])
    
    perceptron = LinearPerceptron(learning_rate=0.1, epochs=10)
    perceptron.fit(X, y)
    
    predictions = perceptron.predict(X)
    print("Predictions:", predictions)  # Output should be [0, 0, 0, 1]
```

This example demonstrates a Linear Perceptron learning the AND gate logic function. The model is trained on a small dataset and uses a step function as its activation function. After training, it accurately predicts the outputs for the given inputs.

#Linear Perceptron #AI