# Loops and Iteration in JavaScript

## How Do Loops and Iteration Work in JavaScript?
Loops in JavaScript allow us to execute a block of code multiple times. The main types of loops in JavaScript are:

- `for` loop
- `for...of` loop
- `for...in` loop
- `while` loop
- `do...while` loop

### Example of a `for` loop:
```javascript
for (let i = 0; i < 5; i++) {
    console.log("Iteration number:", i);
}
```

---

## How Does the For...of Loop Work, and When Should You Use It?
The `for...of` loop is used to iterate over iterable objects such as arrays, strings, maps, and sets.

### Example:
```javascript
const numbers = [10, 20, 30, 40];
for (const num of numbers) {
    console.log(num);
}
```

### When to Use:
- When you need to iterate over values of an iterable object.
- When order matters, such as in an array.

---

## What Is the For...in Loop, and When Should You Use It?
The `for...in` loop is used to iterate over the properties of an object.

### Example:
```javascript
const person = { name: "Alice", age: 25, city: "New York" };
for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

### When to Use:
- When you need to iterate over object properties.
- Not recommended for arrays, as it iterates over enumerable properties rather than values.

---

## What Is a While Loop, and How Does It Differ from the Do...while Loop?
A `while` loop executes as long as a condition is `true`. A `do...while` loop ensures the code runs at least once before checking the condition.

### `while` loop example:
```javascript
let i = 0;
while (i < 5) {
    console.log("Count:", i);
    i++;
}
```

### `do...while` loop example:
```javascript
let j = 0;
do {
    console.log("Count:", j);
    j++;
} while (j < 5);
```

### Key Difference:
- The `while` loop checks the condition before execution.
- The `do...while` loop executes first, then checks the condition.

---

## What Are the Break and Continue Statements Used for in Loops?
- `break` exits a loop immediately.
- `continue` skips the current iteration and moves to the next one.

### Example of `break`:
```javascript
for (let i = 0; i < 10; i++) {
    if (i === 5) break;
    console.log(i);
}
```

### Example of `continue`:
```javascript
for (let i = 0; i < 10; i++) {
    if (i % 2 === 0) continue;
    console.log(i);
}

