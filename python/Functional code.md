### Functional Programming in Python

Functional programming is a paradigm that treats computation as the evaluation of mathematical functions and avoids changing state or mutable data. In Python, while not purely functional, you can adopt functional programming principles through the use of functions like `map()`, `filter()`, and `reduce()`, as well as higher-order functions and lambda expressions.

**Key Concepts:**

1. **Immutability:** Data is treated as immutable, meaning once a data structure is created, it cannot be changed. Instead, new structures are created based on the original ones.
   
2. **First-Class Functions:** Functions are first-class citizens in Python, which means they can be passed around as arguments to other functions, returned from other functions, and assigned to variables just like any other object.

3. **Higher-Order Functions:** These are functions that take one or more functions as an argument or return a function as a result. Examples include `map()`, `filter()`, and `reduce()`.

4. **Lambda Expressions:** Anonymous functions defined with the `lambda` keyword, which can be used wherever function objects are required.

**Examples:**

1. **Using `map()` with a Lambda Function:**
   ```python
   # Applying a lambda function to square each element in a list
   numbers = [1, 2, 3, 4, 5]
   squared_numbers = map(lambda x: x**2, numbers)
   print(list(squared_numbers))  # Output: [1, 4, 9, 16, 25]
   ```

2. **Using `filter()` with a Lambda Function:**
   ```python
   # Filtering out even numbers from a list using a lambda function
   numbers = [1, 2, 3, 4, 5]
   even_numbers = filter(lambda x: x % 2 == 0, numbers)
   print(list(even_numbers))  # Output: [2, 4]
   ```

3. **Using `reduce()` with a Lambda Function:**
   ```python
   from functools import reduce

   # Summing all elements in a list using a lambda function
   numbers = [1, 2, 3, 4, 5]
   total_sum = reduce(lambda x, y: x + y, numbers)
   print(total_sum)  # Output: 15
   ```

Functional programming encourages writing clear and concise code by breaking down problems into smaller functions that are easier to understand and test. It can lead to more efficient and scalable applications.

#Functional code #Python