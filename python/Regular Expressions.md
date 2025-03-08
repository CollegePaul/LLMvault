### Regular Expressions in Python

Regular expressions, often abbreviated as regex or regexp, are sequences of characters that define search patterns. They are used for string matching and manipulation in text processing tasks. In Python, the `re` module provides support for working with regular expressions.

Key components of a regular expression include:

- **Literals**: Characters that match themselves (e.g., `a`, `b`, `123`).
- **Metacharacters**: Special characters with specific meanings in regex, such as:
  - `.`: Matches any character except a newline.
  - `^`: Matches the start of a string.
  - `$`: Matches the end of a string.
  - `*`: Matches zero or more occurrences of the preceding element.
  - `+`: Matches one or more occurrences of the preceding element.
  - `?`: Matches zero or one occurrence of the preceding element.
- **Character classes**: Defined by square brackets `[]`, match any character within them (e.g., `[abc]` matches 'a', 'b', or 'c').
- **Quantifiers**: Specify how many times an element should be matched (e.g., `{n}`, `{n,}`, `{n,m}`).
- **Groups and Ranges**: Parentheses `()` are used for grouping parts of the regex pattern, while ranges like `\d`, `\w` match digits and word characters respectively.

Common functions in Python's `re` module include:

- `re.match(pattern, string)`: Matches pattern at the start of the string.
- `re.search(pattern, string)`: Searches the entire string for a match to the pattern.
- `re.findall(pattern, string)`: Returns all non-overlapping matches of the pattern in the string as a list.
- `re.sub(pattern, repl, string)`: Replaces occurrences of the pattern with `repl` in the string.

#### Example Code

Here's an example demonstrating some basic uses of regular expressions in Python:

```python
import re

# Sample text
text = "The rain in Spain falls mainly in the plain."

# Find all words starting with 'S' or 's'
matches = re.findall(r'\b[Ss]\w+', text)
print(matches)  # Output: ['Spain', 'starts']

# Replace 'mainly' with 'mostly'
new_text = re.sub(r'mainly', 'mostly', text)
print(new_text)  # Output: The rain in Spain falls mostly in the plain.

# Check if a string contains digits
has_digits = re.search(r'\d+', "Hello123")
if has_digits:
    print("Contains digits!")  # This will be printed

# Split a string by non-alphanumeric characters
split_result = re.split(r'\W+', text)
print(split_result)  # Output: ['The', 'rain', 'in', 'Spain', 'falls', 'mainly', 'in', 'the', 'plain']
```

#Regular Expressions #Python