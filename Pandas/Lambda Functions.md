### Lambda Functions in Pandas

Lambda functions in Pandas are small anonymous functions defined using the `lambda` keyword. They are particularly useful when you need to apply quick, simple operations to your data without having to define a full function using `def`. These functions are often used in conjunction with methods like `apply`, `map`, and `agg`.

For example, if you want to add 10 to each element in a column of a DataFrame, you can use a lambda function:

```python
import pandas as pd

# Sample DataFrame
data = {
    'numbers': [1, 2, 3, 4, 5]
}
df = pd.DataFrame(data)

# Using apply with a lambda function to add 10 to each element in the 'numbers' column
df['updated_numbers'] = df['numbers'].apply(lambda x: x + 10)
print(df)
```

This will output:

```
   numbers  updated_numbers
0        1               11
1        2               12
2        3               13
3        4               14
4        5               15
```

Another example is using `map` with a lambda function to categorize numbers in a column based on a condition:

```python
# Using map with a lambda function to create a new column 'category'
df['category'] = df['numbers'].map(lambda x: 'even' if x % 2 == 0 else 'odd')
print(df)
```

This will output:

```
   numbers  updated_numbers category
0        1               11      odd
1        2               12     even
2        3               13      odd
3        4               14     even
4        5               15      odd
```

Lambda functions are concise and can be very powerful when used appropriately, but they can also become hard to read if overused or made too complex. #Lambda Functions #Pandas #Python