### Insertion Sort Explanation in Python

Insertion Sort is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort. However, it has the advantage of being simple to implement and efficient for small data sets or partially sorted data.

The algorithm works by iterating over each element in the input list, comparing it with the elements before it, and inserting it into its correct position relative to those elements. This process is similar to how you might sort playing cards in your hands; you take one card at a time and place it in the right spot among the previously sorted cards.

Here's a step-by-step breakdown of how Insertion Sort works:
1. Start from the second element (index 1) of the array.
2. Compare the current element with the elements before it.
3. Shift all elements that are greater than the current element one position to the right.
4. Place the current element in its correct position.
5. Repeat steps 2-4 for each remaining element in the array.

### Example Code in Python

```python
def insertion_sort(arr):
    # Traverse from 1 to len(arr)
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        # Move elements of arr[0..i-1], that are greater than key,
        # to one position ahead of their current position
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key

# Example usage:
arr = [12, 11, 13, 5, 6]
insertion_sort(arr)
print("Sorted array is:", arr)
```

In the example above, `insertion_sort` function sorts the list `arr` in ascending order. The sorted list is then printed out.

#Insertion Sort #Python