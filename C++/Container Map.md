### Container Map in C++

In C++, the `std::map` is an associative container that stores elements formed by a combination of a key value and a mapped value, following a specific order. The keys are unique and used to sort the data internally using a comparison object (by default, it uses `std::less<Key>` which sorts in ascending order). This structure allows for fast retrieval, insertion, and deletion based on keys.

Here's how you can use `std::map`:

```cpp
#include <iostream>
#include <map>

int main() {
    // Creating a map where the key is an integer and the value is a string.
    std::map<int, std::string> myMap;

    // Inserting elements in random order
    myMap[1] = "one";
    myMap[3] = "three";
    myMap[2] = "two";

    // Printing contents of map
    for (const auto& pair : myMap) {
        std::cout << pair.first << ": " << pair.second << '\n';
    }

    return 0;
}
```

In this example, the elements are automatically sorted by their keys.

### Equivalent Example in Python

Python does not have a direct equivalent of `std::map` since it uses dictionaries for similar functionality. However, starting from Python 3.7, dictionaries maintain insertion order, and they behave somewhat similarly to `std::map` in terms of key-value storage with unique keys.

Here's how you can use a dictionary in Python:

```python
# Creating a dictionary where the key is an integer and the value is a string.
my_dict = {}

# Inserting elements in random order
my_dict[1] = "one"
my_dict[3] = "three"
my_dict[2] = "two"

# Printing contents of dictionary
for key, value in my_dict.items():
    print(f"{key}: {value}")
```

In this Python example, the elements are stored and iterated over in insertion order. However, if you need to maintain a specific sorted order (like `std::map`), you can use `collections.OrderedDict` or simply rely on the fact that from Python 3.7 onwards, dictionaries maintain insertion order.

#Container Map #cpp