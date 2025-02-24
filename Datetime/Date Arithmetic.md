### Date Arithmetic in Datetime

Date arithmetic involves performing operations on dates such as adding or subtracting days, months, years, etc., to calculate new dates. In Python, the `datetime` module provides tools to perform these operations using classes like `date`, `time`, and `timedelta`.

The `timedelta` class represents a duration expressing the difference between two dates, times, or datetimes. It can be used to add or subtract days from a date.

Here are some examples of date arithmetic in Python:

```python
from datetime import date, timedelta

# Current date
current_date = date.today()
print("Current Date:", current_date)

# Adding 5 days to the current date
future_date = current_date + timedelta(days=5)
print("Future Date after adding 5 days:", future_date)

# Subtracting 10 days from the current date
past_date = current_date - timedelta(days=10)
print("Past Date after subtracting 10 days:", past_date)

# Adding months and years requires additional handling as datetime does not support month or year directly in timedelta
from dateutil.relativedelta import relativedelta

# Adding 2 months to the current date
future_month = current_date + relativedelta(months=+2)
print("Future Date after adding 2 months:", future_month)

# Subtracting 1 year from the current date
past_year = current_date + relativedelta(years=-1)
print("Past Date after subtracting 1 year:", past_year)
```

This code snippet demonstrates basic date arithmetic using `timedelta` for days and `relativedelta` from the `dateutil` module for months and years.

#Date Arithmetic #Datetime #Python