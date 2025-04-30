# HashMap Algorithm

## Methods

### `constructor()`
- Initializes a new instance of the HashMap with default capacity (16) and load factor (0.75).

### `length()`
- Returns the number of elements in the HashMap.

### `hash(string)`
- Computes the hash code for a given key using a prime number-based hash function.

### `set(key, value)`
- Adds a key-value pair to the HashMap.
- Resizes the HashMap if the load factor exceeds the threshold.

### `get(key)`
- Retrieves the value associated with the provided key.
- Returns `null` if the key doesn't exist.

### `has(key)`
- Checks if the provided key exists in the HashMap.
- Returns `true` if the key is found, `false` otherwise.

### `remove(key)`
- Removes the key-value pair from the HashMap.
- Returns `true` if the key was removed, `false` if the key doesn't exist.

### `clear()`
- Clears the HashMap, resetting its capacity and removing all key-value pairs.

### `keys()`
- Returns an array of all keys in the HashMap.

### `values()`
- Returns an array of all values in the HashMap.

### `entries()`
- Returns an array of all key-value pairs in the HashMap.

### `resize()`
- Doubles the capacity of the HashMap when the load factor exceeds the threshold and rehashes the existing elements.

## Usage

```javascript
const map = new HashMap();

// Add key-value pairs
map.set('name', 'John');
map.set('age', 30);

// Retrieve values
const name = map.get('name'); // 'John'
const age = map.get('age'); // 30

// Check if a key exists
map.has('name'); // true
map.has('address'); // false

// Remove a key-value pair
map.remove('age');

// Get keys, values, and entries
console.log(map.keys());   // ['name']
console.log(map.values()); // ['John']
console.log(map.entries()); // [['name', 'John']]

// Clear the map
map.clear();
