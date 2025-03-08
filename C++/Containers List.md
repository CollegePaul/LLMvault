### Containers List in C++

In C++, containers are part of the Standard Template Library (STL) that store collections of objects. The `std::list` container, specifically, is a doubly linked list which allows for efficient insertion and deletion of elements at any position. This makes it particularly useful when you need to frequently modify the contents of the collection.

#### Key Features:
- **Doubly Linked List**: Each element (node) contains pointers to both its previous and next node.
- **Dynamic Size**: The size can grow or shrink dynamically as needed.
- **Efficient Insertions/Deletions**: Inserting or deleting elements is efficient, especially when you have an iterator pointing to the position of insertion/deletion.

#### Common Operations:
- `push_front(value)`: Inserts a new element at the beginning.
- `push_back(value)`: Inserts a new element at the end.
- `pop_front()`: Removes the first element.
- `pop_back()`: Removes the last element.
- `insert(iterator, value)`: Inserts a new element before the specified iterator position.
- `erase(iterator)`: Removes the element at the specified iterator position.

### Example in C++:
```cpp
#include <iostream>
#include <list>

int main() {
    std::list<int> numbers;

    // Insert elements
    numbers.push_back(10);
    numbers.push_front(5);
    numbers.insert(std::next(numbers.begin()), 7);

    // Output list
    for (int num : numbers) {
        std::cout << num << " "; // Outputs: 5 7 10
    }

    // Remove elements
    numbers.pop_front();
    numbers.erase(std::next(numbers.begin()));

    // Output updated list
    for (int num : numbers) {
        std::cout << num << " "; // Outputs: 10
    }
}
```

### Example in Python:
Python does not have a direct equivalent to C++'s `std::list`, but it has a similar data structure called `collections.deque` which can be used for efficient insertion and deletion from both ends. For more general linked list operations, you would need to implement your own class or use libraries like `linkedlist`.

Here’s how you might mimic some of the functionality using Python's `deque`:

```python
from collections import deque

# Create a deque (double-ended queue)
numbers = deque()

# Insert elements
numbers.append(10)        # Equivalent to push_back
numbers.appendleft(5)     # Equivalent to push_front
numbers.insert(1, 7)      # Insert at index 1

# Output list
print(numbers)            # Outputs: deque([5, 7, 10])

# Remove elements
numbers.popleft()         # Equivalent to pop_front
del numbers[1]            # Delete element at index 1

# Output updated list
print(numbers)            # Outputs: deque([5])
```

In this Python example, `deque` is used to demonstrate similar operations as the C++ `std::list`. While `deque` is not a linked list in the strict sense (it’s more like an array with dynamic resizing and fast fixed-end insertions/deletions), it serves many of the same purposes for certain applications.

#Containers List #cpp