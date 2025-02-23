### Loading Files in Python

In Python, loading files involves reading data from external sources into your program. This can be done using built-in functions such as `open()`, which allows you to open a file and read its contents. The most common methods for loading files are reading text files and binary files.

#### Reading Text Files
To read a text file in Python, you can use the `open()` function with the mode set to `'r'` (read). Here is an example:

```python
# Open a file in read mode
with open('example.txt', 'r') as file:
    # Read the entire content of the file
    content = file.read()
    print(content)
```

In this example, `open()` opens the file named `'example.txt'` and returns a file object. The `with` statement ensures that the file is properly closed after its suite finishes, even if an exception is raised on the way.

#### Reading Binary Files
To read binary files, such as images or PDFs, you use the mode `'rb'`. Here's how you can do it:

```python
# Open a binary file in read mode
with open('image.png', 'rb') as file:
    # Read the content of the file into a byte object
    binary_content = file.read()
    print(binary_content)
```

#### Reading Files Line by Line
For large files, it might be more efficient to read one line at a time. You can achieve this with a loop:

```python
# Open a text file and read line by line
with open('example.txt', 'r') as file:
    for line in file:
        print(line.strip())  # strip() removes the newline character from the end of each line
```

#### Reading CSV Files
For CSV files, Python's `csv` module can be very useful:

```python
import csv

# Open a CSV file and read its contents
with open('data.csv', 'r') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)  # Each row is returned as a list of strings
```

#### Reading JSON Files
To read JSON files, you can use the `json` module:

```python
import json

# Open and read a JSON file
with open('data.json', 'r') as jsonfile:
    data = json.load(jsonfile)
    print(data)  # The content is loaded into a Python dictionary or list, depending on the structure of the JSON
```

These are some common ways to load files in Python. Depending on your specific needs, you might need to use other modules or methods, but these examples cover the basics.

#Loading Files #Python