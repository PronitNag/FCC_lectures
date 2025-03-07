# JavaScript Sets and WeakSets

## What Are Sets in JavaScript?
A `Set` in JavaScript is a collection of unique values, meaning it does not allow duplicate elements.

### Creating a Set
```javascript
const mySet = new Set([1, 2, 3, 3, 4]);
console.log(mySet); // Output: Set { 1, 2, 3, 4 }
```

### Set Methods
```javascript
mySet.add(5);    // Adds an element
mySet.delete(2); // Removes an element
console.log(mySet.has(3)); // Checks if an element exists
console.log(mySet.size);   // Returns the number of elements
```

## How Does a Set Differ from a WeakSet?
- `Set` stores values strongly and allows iteration.
- `WeakSet` only stores objects and does not allow iteration.

### Creating a WeakSet
```javascript
const weakSet = new WeakSet();
let obj = { a: 1 };
weakSet.add(obj);
console.log(weakSet.has(obj)); // true
```

### WeakSet Characteristics
- Only stores objects.
- Garbage collection removes objects if no references exist.
- No size property or iteration methods.

---

# JavaScript Map and WeakMap

## What Is the Map Object?
A `Map` in JavaScript is a collection of key-value pairs where keys can be of any data type.

### Creating a Map
```javascript
const myMap = new Map();
myMap.set('name', 'Alice');
myMap.set(1, 'one');
console.log(myMap.get('name')); // Output: Alice
```

### Map Methods
```javascript
myMap.delete(1);  // Removes a key-value pair
console.log(myMap.has('name')); // Checks if key exists
console.log(myMap.size);  // Returns number of elements
```

## How Does a Map Differ from a WeakMap?
- `Map` stores key-value pairs strongly and supports iteration.
- `WeakMap` only allows objects as keys and does not allow iteration.

### Creating a WeakMap
```javascript
const weakMap = new WeakMap();
let obj = {};
weakMap.set(obj, 'value');
console.log(weakMap.get(obj)); // Output: value
```

### WeakMap Characteristics
- Keys must be objects.
- Garbage collection removes unused objects.
- No size property or iteration methods.

