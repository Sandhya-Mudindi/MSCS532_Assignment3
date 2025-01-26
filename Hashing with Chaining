class HashTable:
    def __init__(self, size=10):
        """Initialize the hash table with a fixed size."""
        self.size = size  # Set the size of the hash table
        # Create a list of empty lists (chains) for each index in the hash table
        self.table = [[] for _ in range(size)]

    def _hash_function(self, key):
        """Hash function to compute an index for the given key."""
        # Use Python's built-in hash function and modulo operation to find an index
        return hash(key) % self.size

    def insert(self, key, value):
        """Insert a key-value pair into the hash table."""
        index = self._hash_function(key)  # Compute the index for the given key
        # Check if the key already exists in the chain at the computed index
        for pair in self.table[index]:
            if pair[0] == key:  # If key is found, update its value
                pair[1] = value
                return
        # If the key does not exist, append the new key-value pair to the chain
        self.table[index].append([key, value])

    def search(self, key):
        """Search for a value associated with the given key."""
        index = self._hash_function(key)  # Compute the index for the given key
        # Look for the key in the chain at the computed index
        for pair in self.table[index]:
            if pair[0] == key:  # If key is found, return the associated value
                return pair[1]
        return None  # Return None if the key is not found

    def delete(self, key):
        """Remove a key-value pair from the hash table."""
        index = self._hash_function(key)  # Compute the index for the given key
        # Iterate through the chain at the computed index
        for i, pair in enumerate(self.table[index]):
            if pair[0] == key:  # If key is found, remove it from the chain
                del self.table[index][i]
                return True  # Indicate that the deletion was successful
        return False  # Return False if the key is not found

    def __str__(self):
        """Provide a string representation of the hash table for debugging."""
        result = ""  # Initialize an empty string to store the result
        # Iterate through each index and its chain in the hash table
        for i, chain in enumerate(self.table):
            result += f"Index {i}: {chain}\n"  # Append the chain's representation
        return result  # Return the full string representation

# Example usage
if __name__ == "__main__":
    # Create a hash table with a specified size
    ht = HashTable(size=5)

    # Insert key-value pairs into the hash table
    ht.insert("sandhya", 10)
    ht.insert("sravani", 20)
    ht.insert("srinu", 30)
    ht.insert("sujatha", 40)
    ht.insert("samu", 50)

    # Display the current state of the hash table
    print("Hash Table:")
    print(ht)

    # Search for keys in the hash table
    print("Search Results:")
    print("sandhya:", ht.search("sandhya"))  # Output: 10
    print("sujatha:", ht.search("sujatha"))  # Output: 40
    print("shalu:", ht.search("shalu"))     # Output: None

    # Delete a key-value pair from the hash table
    print("\nDeleting 'samu'...")
    ht.delete("samu")

    # Display the hash table after deletion
    print("Hash Table After Deletion:")
    print(ht)
