### Linear Search in Python

Linear search is a straightforward algorithm used to find a specific element within a list or array. It works by iterating through each element of the list sequentially until the desired element is found or the end of the list is reached. This method is simple and does not require the list to be sorted, but it can be inefficient for large datasets as its time complexity is O(n), where n is the number of elements in the list.

Here's a basic example of how linear search can be implemented in Python:

```python
def linear_search(arr, target):
    """
    Perform a linear search on a list to find the index of a target value.
    
    Parameters:
        arr (list): The list to search through.
        target: The element to search for.

    Returns:
        int: The index of the target element if found, otherwise -1.
    """
    for index, element in enumerate(arr):
        if element == target:
            return index
    return -1

# Example usage:
my_list = [3, 5, 2, 4, 9]
target_value = 4

result = linear_search(my_list, target_value)

if result != -1:
    print(f"Element {target_value} found at index {result}.")
else:
    print(f"Element {target_value} not found in the list.")

# Output: Element 4 found at index 3.
```

In this example, the `linear_search` function takes a list and a target value as arguments. It iterates over each element in the list using `enumerate`, which returns both the index and the element. If it finds the target element, it returns its index; if not, it returns -1 after completing the loop.

#Linear search #Python