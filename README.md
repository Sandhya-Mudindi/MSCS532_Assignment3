# MSCS532 Assignment 3

This repository contains implementations of algorithms and data structures as part of Assignment 3. Each file demonstrates a specific concept with example usage and performance analysis.

---

## Files and How to Run Them

### 1. **`Randomized Quicksort.py`**
- **Description:** Implements Randomized Quicksort to sort arrays with empirical performance comparison.
- **How to Run:**
  ```bash
  python Randomized Quicksort.py

### 2. **`Randomizied and Deterministic Quick Sort.py`**
- **Description:** Implements Randomized and Deterministic Quicksort using the first element as the pivot and performance times for randomizied and deterministic partitioning across test cases..
- **How to Run:**
  ```bash
  python Randomizied and Deterministic Quick Sort.py


### 3. **`Hashing with Chaining`**
- **Description:** Demonstrates a Hash Table implementation using chaining for collision handling..
- **How to Run:**
  ```bash
  python Hashing with Chaining.py

###  **`Summary of Findings`**


- Randomized Quicksort: Random pivot selection reduces the likelihood of encountering the worst-case performance, showing consistent runtime across various input types.
- Deterministic Quicksort: Uses a fixed pivot strategy and performs efficiently for unsorted and reverse-sorted arrays but is prone to worst-case performance on sorted data.
- Hash Table: Hash tables efficiently handle collisions using chaining, ensuring consistent performance for operations like insertion, search, and deletion.
Demonstrates the impact of hash function and table size on performance, making it scalable for different workloads.


