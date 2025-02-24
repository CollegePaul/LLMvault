### Timedelta Objects in Datetime

In Python's `datetime` module, a `timedelta` object represents a duration, the difference between two dates or times. This duration can be expressed in days, seconds, and microseconds. The main purpose of `timedelta` is to perform arithmetic on dates and times.

Here are some key points about `timedelta`:

- **Creation**: You can create a `timedelta` object by specifying the number of days, seconds, and microseconds.
- **Operations**: You can add or subtract `timedelta` objects from `datetime` objects to get new dates. You can also add or subtract two `timedelta` objects to get a new `timedelta`.
- **Attributes**: A `timedelta` object has several attributes like `days`, `seconds`, and `microseconds`.

#### Examples

```python
from datetime import datetime, timedelta

# Creating a timedelta object representing 5 days
five_days = timedelta(days=5)
print(five_days)  # Output: 5 days, 0:00:00

# Creating a timedelta object for 2 hours and 30 minutes
two_hours_thirty_minutes = timedelta(hours=2, minutes=30)
print(two_hours_thirty_minutes)  # Output: 2:30:00

# Current date and time
now = datetime.now()
print("Current Time:", now)

# Adding a timedelta to the current datetime
future_time = now + five_days
print("Future Time (5 days later):", future_time)

# Subtracting a timedelta from the current datetime
past_time = now - two_hours_thirty_minutes
print("Past Time (2 hours and 30 minutes ago):", past_time)
```

In this example:
- We create a `timedelta` object representing 5 days and another for 2 hours and 30 minutes.
- We then use these `timedelta` objects to find future and past dates relative to the current date and time.

#Timedelta Objects #Datetime #Python