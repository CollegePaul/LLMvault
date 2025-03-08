### Datetime Formatting in Python

Datetime formatting allows you to convert datetime objects into readable strings according to specified patterns. This can be useful for displaying dates and times in a user-friendly format or preparing them for storage or transmission.

In Python, the `datetime` module provides a class called `strftime()` that enables you to create custom date and time formats. The method takes one parameter: a string with directives that specify how the datetime object should be formatted.

Here are some common directives used in strftime:
- `%Y`: Year with century as a decimal number.
- `%m`: Month as a zero-padded decimal number.
- `%d`: Day of the month as a zero-padded decimal number.
- `%H`: Hour (24-hour clock) as a zero-padded decimal number.
- `%M`: Minute as a zero-padded decimal number.
- `%S`: Second as a zero-padded decimal number.

Let's look at some examples:

```python
from datetime import datetime

# Create a datetime object for demonstration
now = datetime.now()

# Example 1: Format date in YYYY-MM-DD format
formatted_date = now.strftime("%Y-%m-%d")
print("Formatted Date:", formatted_date)

# Example 2: Format time in HH:MM:SS format
formatted_time = now.strftime("%H:%M:%S")
print("Formatted Time:", formatted_time)

# Example 3: Combine date and time with custom separators
custom_format = now.strftime("%Y/%m/%d %I:%M %p")
print("Custom Format:", custom_format)
```

In the examples above:
- The first example formats the current date as `YYYY-MM-DD`.
- The second example formats the current time as `HH:MM:SS`.
- The third example combines both date and time, using a 12-hour clock format with AM/PM.

These formatting options are highly customizable to meet your specific requirements. #DatetimeFormatting #Datetime #Python