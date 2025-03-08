### Merge Sort Explanation in Python

Merge Sort is a classic divide-and-conquer algorithm used to sort elements. It operates by dividing the array into two halves, recursively sorting each half, and then merging the sorted halves back together to produce the final sorted array.

#### Steps Involved:
1. **Divide**: The array is split into two halves until each subarray contains a single element.
2. **Conquer**: Each pair of subarrays is merged in a manner that results in a new sorted array.
3. **Combine**: The merging process continues up the recursion tree, combining smaller sorted arrays to form larger ones until the entire original array is sorted.

#### Why Merge Sort?
- **Stability**: It maintains the relative order of equal elements.
- **Performance**: It has a time complexity of O(n log n) in all cases (worst, average, and best).

#### How Merging Works:
- Two pointers are used to traverse each subarray. The smaller element from the two is selected and placed into the new array.
- This process continues until one of the subarrays is exhausted, at which point any remaining elements from the other subarray are copied directly into the new array.

### Example Code in Python

```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2  # Finding the mid of the array
        L = arr[:mid]  # Dividing the array elements into 2 halves
        R = arr[mid:]

        merge_sort(L)  # Sorting the first half
        merge_sort(R)  # Sorting the second half

        i = j = k = 0

        # Copy data to temp arrays L[] and R[]
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        # Checking if any element was left
        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1

        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1

# Example usage:
arr = [38, 27, 43, 3, 9, 82, 10]
merge_sort(arr)
print("Sorted array is:", arr)  # Output: Sorted array is: [3, 9, 10, 27, 38, 43, 82]

#Merge Sort #Python