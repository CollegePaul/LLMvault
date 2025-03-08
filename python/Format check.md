### Format Check in Python

In Python, format checking generally refers to verifying whether data is structured or formatted as expected. This can involve checking types of variables, ensuring strings match a specific pattern, validating dates and times, or confirming that data adheres to certain constraints.

Python provides several ways to perform these checks:

1. **Type Checking**: Using built-in functions like `isinstance()`.
2. **Regular Expressions**: Using the `re` module for complex string pattern matching.
3. **Custom Validation Functions**: Writing custom functions to check specific conditions.
4. **Third-party Libraries**: Tools like `pydantic` or `voluptuous` can enforce data validation rules.

#### Examples

**1. Type Checking with `isinstance()`**

```python
def validate_integer(value):
    if not isinstance(value, int):
        raise ValueError("Value must be an integer")
    return True

try:
    validate_integer(5)
    print("Validation passed for integer 5.")
except ValueError as e:
    print(e)

try:
    validate_integer("5")
    print("Validation passed for string '5'.") # This line will not execute
except ValueError as e:
    print(e)  # Output: Value must be an integer
```

**2. Regular Expressions with `re` module**

```python
import re

def is_valid_email(email):
    pattern = r'^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$'
    if not re.match(pattern, email):
        raise ValueError("Invalid email format")
    return True

try:
    is_valid_email("example@test.com")
    print("Email validation passed for example@test.com.")
except ValueError as e:
    print(e)

try:
    is_valid_email("example.test@com")  # Missing domain part
    print("Email validation passed for example.test@com.") # This line will not execute
except ValueError as e:
    print(e)  # Output: Invalid email format
```

**3. Custom Validation Functions**

```python
def validate_password(password):
    if len(password) < 8:
        raise ValueError("Password must be at least 8 characters long")
    elif not any(char.isdigit() for char in password):
        raise ValueError("Password must contain at least one digit")
    else:
        return True

try:
    validate_password("Passw0rd")
    print("Password validation passed.")
except ValueError as e:
    print(e)

try:
    validate_password("pass")  # Shorter than 8 characters
    print("Password validation passed.") # This line will not execute
except ValueError as e:
    print(e)  # Output: Password must be at least 8 characters long
```

**4. Using `pydantic` for Data Validation**

```python
from pydantic import BaseModel, EmailStr, validator

class User(BaseModel):
    name: str
    age: int
    email: EmailStr

    @validator('age')
    def check_age(cls, v):
        if v < 18:
            raise ValueError('Age must be at least 18 years old')
        return v

try:
    user = User(name="John Doe", age=20, email="john.doe@example.com")
    print("User validation passed.")
except ValueError as e:
    print(e)

try:
    user = User(name="Jane Doe", age=15, email="jane.doe@example")  # Invalid email and underage
    print("User validation passed.") # This line will not execute
except ValueError as e:
    print(e)  # Output: Age must be at least 18 years old or value is not a valid email address: 'jane.doe@example'
```

#Format check #Python