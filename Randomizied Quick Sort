import random

def randomized_partition(arr, low, high):
    """Performs the partition step using a random pivot."""
    pivot_index = random.randint(low, high)
    arr[pivot_index], arr[high] = arr[high], arr[pivot_index]  # Swap pivot with the last element
    pivot = arr[high]
    i = low - 1  # Index of the smaller element

    for j in range(low, high):
        if arr[j] <= pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]  # Swap if element is smaller than or equal to pivot

    arr[i + 1], arr[high] = arr[high], arr[i + 1]  # Swap pivot to the correct position
    return i + 1

def randomized_quicksort(arr, low, high):
    """Implements the Randomized Quicksort algorithm."""
    if low < high:
        pi = randomized_partition(arr, low, high)  # Partition index
        randomized_quicksort(arr, low, pi - 1)  # Recursively sort the left subarray
        randomized_quicksort(arr, pi + 1, high)  # Recursively sort the right subarray

def quicksort(arr):
    """Public function to sort an array using Randomized Quicksort."""
    if arr and len(arr) > 1:
        randomized_quicksort(arr, 0, len(arr) - 1)

# Example usage
if __name__ == "__main__":
    test_cases = [
        [],
        [1],
        [5, 2, 9, 1, 5, 6],
        [4, 2, 2, 8, 4, 3, 3],
        [1, 2, 3, 4, 5, 6],
        [6, 5, 4, 3, 2, 1],
    ]

    for i, test in enumerate(test_cases, 1):
        print(f"Test case {i}: Original: {test}")
        quicksort(test)  # Sorts the array in place
        print(f"Sorted: {test}\n")
