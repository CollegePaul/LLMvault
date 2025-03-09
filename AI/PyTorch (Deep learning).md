### Introduction to PyTorch in AI

PyTorch is an open-source machine learning library based on the Torch library, used for applications such as computer vision and natural language processing, primarily developed by Facebook's AI Research lab. It provides two high-level features: tensor computation (like NumPy) with strong GPU acceleration and deep neural networks built on a tape-based autograd system.

#### Key Features of PyTorch
1. **Dynamic Computation Graphs**: PyTorch builds the graph at runtime, which makes debugging easier and allows for more flexible and dynamic models.
2. **Tensor Operations**: Similar to NumPy arrays but can run on GPUs, making it much faster for large-scale data processing.
3. **Autograd System**: Automatically computes gradients, which is essential for backpropagation in training neural networks.
4. **Ease of Use**: PyTorch has a Pythonic interface, making it user-friendly and easy to learn, especially for researchers.

#### Example: Simple Neural Network with PyTorch

Let's create a simple feedforward neural network using PyTorch that classifies data into two classes. We'll use a dummy dataset generated with NumPy for demonstration purposes.

```python
import torch
import torch.nn as nn
import torch.optim as optim
import numpy as np

# Generate dummy data: 100 samples, each with 2 features
np.random.seed(42)
X = np.random.randn(100, 2).astype(np.float32)
y = (X[:, 0] + X[:, 1] > 0).astype(np.int32)

# Convert numpy arrays to PyTorch tensors
X_tensor = torch.from_numpy(X)
y_tensor = torch.from_numpy(y)

# Define a simple neural network
class SimpleNN(nn.Module):
    def __init__(self):
        super(SimpleNN, self).__init__()
        self.fc1 = nn.Linear(2, 4)  # Input layer to hidden layer with 4 neurons
        self.relu = nn.ReLU()
        self.fc2 = nn.Linear(4, 1)  # Hidden layer to output layer

    def forward(self, x):
        out = self.fc1(x)
        out = self.relu(out)
        out = self.fc2(out)
        return torch.sigmoid(out)

# Instantiate the model
model = SimpleNN()

# Define loss function and optimizer
criterion = nn.BCELoss()
optimizer = optim.SGD(model.parameters(), lr=0.1)

# Training loop
num_epochs = 50
for epoch in range(num_epochs):
    # Forward pass: compute predicted y by passing X to the model
    outputs = model(X_tensor)
    loss = criterion(outputs.squeeze(), y_tensor.float())

    # Zero gradients, perform a backward pass, and update the weights.
    optimizer.zero_grad()
    loss.backward()
    optimizer.step()

    if (epoch+1) % 10 == 0:
        print(f'Epoch [{epoch+1}/{num_epochs}], Loss: {loss.item():.4f}')

# Test the model
with torch.no_grad():
    predicted = model(X_tensor)
    predicted = (predicted > 0.5).float()
    accuracy = (predicted.squeeze() == y_tensor.float()).sum().item() / len(y_tensor)
    print(f'Accuracy: {accuracy * 100:.2f}%')

# Output the final loss and accuracy
print('Final Loss:', loss.item())
```

In this example, we created a simple neural network with one hidden layer to classify data points into two classes based on whether their sum is greater than zero. The model uses binary cross-entropy loss and stochastic gradient descent (SGD) for optimization.

#PyTorch (Deep learning)
#AI