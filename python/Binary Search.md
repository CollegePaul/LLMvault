### Binary Search in Python

Binary search is an efficient algorithm for finding an item from a sorted list of items. It works by repeatedly dividing in half the portion of the list that could contain the item, until you've narrowed down the possible locations to just one.

The basic idea behind binary search is to start with two pointers: one at the beginning and one at the end of the list. You then calculate the middle index of the current range and compare the target value with the element at this middle index. If the target value matches the element, the search is successful. If the target value is less than the middle element, you adjust the end pointer to be just before the middle index, effectively discarding the upper half of the list. Conversely, if the target value is greater than the middle element, you adjust the start pointer to be just after the middle index, discarding the lower half of the list.

This process repeats until either the target value is found or the range becomes empty (i.e., the start pointer exceeds the end pointer), in which case the search concludes that the target value is not present in the list.

Here's a simple implementation of binary search in Python:

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        # Check if target is present at mid
        if arr[mid] == target:
            return mid
        
        # If target is greater, ignore left half
        elif arr[mid] < target:
            left = mid + 1
        
        # If target is smaller, ignore right half
        else:
            right = mid - 1
    
    # Target was not found in the array
    return -1

# Example usage:
sorted_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
target_value = 7
result = binary_search(sorted_list, target_value)

if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found in the list")
```

In this example, `binary_search` is a function that takes a sorted array and a target value as arguments. It returns the index of the target value if it is present in the array, or -1 if it is not.

#Binary Search #Python