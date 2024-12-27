---
Title: 'strptime' Description: 'Parses a string representing a date and/or time into a datetime object using the specified format.'
  Subjects:
- 'Python'
- 'Datetime'
  Tags:
- 'Datetime'
- 'Parsing'
- 'Strings'
  CatalogContent:
- 'learn-python-3'
- 'paths/computer-science'

---

The **`.strptime()`** **method** in Python is a part of the `datetime` module. It is used to parse a string representing a date and/or time and convert it into a `datetime` object using a specified format.

## Syntax

```python
from datetime import datetime

datetime.strptime(date_string, format)
```

### Parameters:

- `date_string` (str): The string representing the date and/or time.
- `format` (str): The format that defines the structure of `date_string`. This uses the directives from the `datetime` module (e.g., `%Y` for a four-digit year, `%m` for a two-digit month).

### Returns:

- A `datetime` object corresponding to the parsed date and time.

### Raises:

- `ValueError`: If the `date_string` does not match the `format`.

## Example

### Parsing a Date String

```python
from datetime import datetime

# Define the date string and format
date_string = "2024-12-27"
date_format = "%Y-%m-%d"

# Parse the string into a datetime object
dt_object = datetime.strptime(date_string, date_format)

print(dt_object)  # Output: 2024-12-27 00:00:00
```

### Parsing a Date and Time String

```python
from datetime import datetime

# Define the date-time string and format
datetime_string = "27/12/2024 15:30:00"
datetime_format = "%d/%m/%Y %H:%M:%S"

# Parse the string into a datetime object
dt_object = datetime.strptime(datetime_string, datetime_format)

print(dt_object)  # Output: 2024-12-27 15:30:00
```

## Codebyte Example

```codebyte/python
from datetime import datetime

# Parse a date string with a specific format
date_string = "03-01-2023"
format = "%d-%m-%Y"
dt_object = datetime.strptime(date_string, format)

print("Parsed datetime:", dt_object)
# Output: Parsed datetime: 2023-01-03 00:00:00
```

