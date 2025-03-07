# JavaScript Functions and Methods

## What Is a Callback Function, and How Does It Work with the forEach Method?
A **callback function** is a function that is passed as an argument to another function and is executed later.

The `forEach` method is used to iterate over an array and execute a callback function for each element.

### Example:
```js
const numbers = [1, 2, 3, 4];
numbers.forEach(function(num) {
    console.log(num * 2);
});
```

## What Are Higher-Order Functions?
A **higher-order function** is a function that either:
1. Takes another function as an argument, or
2. Returns a function.

### Example:
```js
function greet(name) {
    return function(message) {
        console.log(`${message}, ${name}!`);
    };
}

const sayHello = greet("Alice");
sayHello("Hello"); // Output: Hello, Alice!
```

## What Is the Map Method, and How Does It Work?
The `map` method creates a new array by applying a function to each element of an existing array.

### Example:
```js
const numbers = [1, 2, 3, 4];
const squared = numbers.map(num => num * num);
console.log(squared); // Output: [1, 4, 9, 16]
```

## What Is the Filter Method, and How Does It Work?
The `filter` method creates a new array with elements that satisfy a given condition.

### Example:
```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

## What Is the Reduce Method, and How Does It Work?
The `reduce` method accumulates array values into a single result.

### Example:
```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // Output: 10
```

## What Is Method Chaining, and How Does It Work?
**Method chaining** allows multiple methods to be called on the same array in a single statement.

### Example:
```js
const numbers = [1, 2, 3, 4, 5];
const result = numbers.filter(num => num % 2 !== 0)
                      .map(num => num * 2)
                      .reduce((acc, num) => acc + num, 0);
console.log(result); // Output: 12
```

## How Does the Sort Method Work?
The `sort` method sorts elements in an array **alphabetically** by default. For numbers, a comparator function is required.

### Example:
```js
const numbers = [5, 2, 9, 1, 3];
numbers.sort((a, b) => a - b);
console.log(numbers); // Output: [1, 2, 3, 5, 9]
```

## How Do the every() and some() Methods Work?
- `every()`: Checks if **all** elements in an array satisfy a condition.
- `some()`: Checks if **at least one** element satisfies a condition.

### Example:
```js
const numbers = [2, 4, 6, 8];
console.log(numbers.every(num => num % 2 === 0)); // Output: true
console.log(numbers.some(num => num > 5)); // Output: true
