# JavaScript Arrays

## Key Characteristics of JavaScript Arrays
- **Dynamic**: Arrays in JavaScript can grow and shrink dynamically.
- **Heterogeneous**: They can store elements of different data types.
- **Zero-based indexing**: The first element is at index `0`.
- **Mutable**: Elements can be changed after the array is created.
- **Prototype Methods**: Arrays come with built-in methods like `push()`, `pop()`, `map()`, etc.

```javascript
let arr = [1, "hello", true, { key: "value" }];
console.log(arr.length); // 4
```

---

## Accessing and Updating Elements in an Array
- **Accessing**: Use square brackets `[]` and index number.
- **Updating**: Assign a new value to a specific index.

```javascript
let numbers = [10, 20, 30];
console.log(numbers[1]); // 20

numbers[1] = 25; // Updating
console.log(numbers[1]); // 25
```

---

## Adding and Removing Elements
### Beginning of an Array
- **Add**: `unshift(value)`
- **Remove**: `shift()`

```javascript
let arr = [2, 3, 4];
arr.unshift(1); // [1, 2, 3, 4]
arr.shift(); // [2, 3, 4]
```

### End of an Array
- **Add**: `push(value)`
- **Remove**: `pop()`

```javascript
let arr = [1, 2, 3];
arr.push(4); // [1, 2, 3, 4]
arr.pop(); // [1, 2, 3]
```

---

## One-Dimensional vs Two-Dimensional Arrays
- **One-Dimensional**: A single list of elements.
- **Two-Dimensional**: An array containing other arrays (like a matrix).

```javascript
// One-Dimensional Array
let oneD = [1, 2, 3];

// Two-Dimensional Array
let twoD = [
  [1, 2, 3],
  [4, 5, 6]
];
console.log(twoD[1][2]); // 6
```

---

## Array Destructuring
- A concise way to extract values from an array.

```javascript
let colors = ["red", "green", "blue"];
let [first, second, third] = colors;
console.log(first); // "red"
console.log(second); // "green"
```

- **Skipping Values**
```javascript
let [, , last] = colors;
console.log(last); // "blue"
```

- **Swapping Variables**
```javascript
let a = 1, b = 2;
[a, b] = [b, a];
console.log(a, b); // 2, 1

