### Cost Functions in AI

Cost functions are essential in machine learning and artificial intelligence as they provide a way to measure how well a model's predictions match the actual data. They act as a feedback mechanism during the training process, guiding the optimization algorithm on how to adjust the model parameters to minimize the error or cost.

In supervised learning, for example, a cost function is used to quantify the difference between the predicted values and the true values. The goal of training a model is to find the set of parameters that minimizes this cost function.

#### Types of Cost Functions

1. **Mean Squared Error (MSE):** Used primarily in regression problems, MSE calculates the average squared difference between the predicted and actual values. It penalizes larger errors more heavily due to squaring.

   ```python
   def mean_squared_error(y_true, y_pred):
       return ((y_true - y_pred) ** 2).mean()

   # Example usage
   y_true = [3.0, -0.5, 2.0, 7.0]
   y_pred = [2.5, 0.0, 2.0, 8.0]
   mse = mean_squared_error(y_true, y_pred)
   print(f"Mean Squared Error: {mse}")
   ```

2. **Cross-Entropy Loss:** Commonly used in classification problems, particularly with logistic regression and neural networks with softmax outputs. It measures the difference between two probability distributions.

   ```python
   import numpy as np

   def cross_entropy_loss(y_true, y_pred):
       # Convert predictions to probabilities
       epsilon = 1e-15
       y_pred_clipped = np.clip(y_pred, epsilon, 1 - epsilon)
       log_y_pred = np.log(y_pred_clipped)

       loss = -(y_true * log_y_pred).sum()
       return loss

   # Example usage
   y_true = [0, 1, 0]
   y_pred = [0.2, 0.8, 0.05]
   ce_loss = cross_entropy_loss(y_true, y_pred)
   print(f"Cross Entropy Loss: {ce_loss}")
   ```

3. **Mean Absolute Error (MAE):** Another regression metric that calculates the average absolute difference between predictions and actual values. It is less sensitive to outliers compared to MSE.

   ```python
   def mean_absolute_error(y_true, y_pred):
       return np.abs(y_true - y_pred).mean()

   # Example usage
   y_true = [3.0, -0.5, 2.0, 7.0]
   y_pred = [2.5, 0.0, 2.0, 8.0]
   mae = mean_absolute_error(y_true, y_pred)
   print(f"Mean Absolute Error: {mae}")
   ```

Cost functions play a crucial role in the training of AI models by providing a quantitative measure to optimize performance and accuracy.

#Cost Functions #AI