### Quick Sort Explanation

Quick Sort is an efficient sorting algorithm that follows the divide-and-conquer paradigm. The algorithm works by selecting a 'pivot' element from the array and partitioning the other elements into two sub-arrays, according to whether they are less than or greater than the pivot. The sub-arrays are then sorted recursively.

Here's a step-by-step breakdown of how Quick Sort operates:

1. **Choose a Pivot**: Select an element from the array as the pivot. There are various strategies for choosing a pivot, such as picking the first element, the last element, the middle element, or even a random element.

2. **Partitioning**: Rearrange the array so that all elements less than the pivot come before it, while all elements greater than the pivot come after it. The pivot is now in its final position.

3. **Recursively Apply**: Recursively apply the above steps to the sub-array of elements with smaller values and the sub-array of elements with greater values.

### Quick Sort Example in Python

Below is an example implementation of Quick Sort in Python:

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[len(arr) // 2]  # Choosing the middle element as the pivot
        left = [x for x in arr if x < pivot]
        middle = [x for x in arr if x == pivot]
        right = [x for x in arr if x > pivot]
        return quick_sort(left) + middle + quick_sort(right)

# Example usage:
array = [3, 6, 8, 10, 1, 2, 1]
sorted_array = quick_sort(array)
print(sorted_array)
```

In this example, the `quick_sort` function takes an array as input and returns a new sorted array. The pivot is chosen as the middle element of the array, and the list comprehension is used to partition the array into three sub-arrays: elements less than the pivot (`left`), elements equal to the pivot (`middle`), and elements greater than the pivot (`right`). The function then recursively sorts the `left` and `right` sub-arrays and combines them with the `middle` array.

#Quick Sort #Python