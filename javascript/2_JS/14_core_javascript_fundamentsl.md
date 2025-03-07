# JavaScript Notes

## What Is a String Object, and How Does It Differ from String Primitive?

In JavaScript, strings can be represented in two ways:

1. **String Primitive** - A simple sequence of characters, created using string literals.
2. **String Object** - Created using the `String` constructor, which wraps the primitive in an object.

### Example:

```js
let primitiveStr = "Hello"; // String primitive
let objectStr = new String("Hello"); // String object

console.log(typeof primitiveStr); // "string"
console.log(typeof objectStr); // "object"
```

## What Is the toString() Method, and How Does It Work?

The `toString()` method converts an object to its string representation.

### Example:

```js
let num = 42;
console.log(num.toString()); // "42"

let arr = [1, 2, 3];
console.log(arr.toString()); // "1,2,3"
```

## What Is the Number Constructor, and How Does It Work for Type Coercion?

The `Number` constructor is used to convert other types into numbers.

### Example:

```js
console.log(Number("42")); // 42
console.log(Number(true)); // 1
console.log(Number("abc")); // NaN
```

## What Are Some Common Practices for Naming Variables and Functions?

1. Use **camelCase** for variables and functions: `myVariable`, `calculateSum()`
2. Use **PascalCase** for constructor functions and classes: `Person`, `Car`
3. Use **descriptive names**: `getUserData()` instead of `gud()`
4. Prefix booleans with `is` or `has`: `isValid`, `hasAccess`
5. Avoid reserved keywords and special characters.

## How Do You Get the Length for an Array, and How Can You Create an Empty Array of Fixed Length?

### Get Array Length:

```js
let arr = [1, 2, 3, 4, 5];
console.log(arr.length); // 5
```

### Create an Empty Array with Fixed Length:

```js
let fixedArray = new Array(5); // Creates an empty array of length 5
console.log(fixedArray.length); // 5
```

## What Are Linters and Formatters, and How Can They Help You with Code Consistency?

- **Linters**: Analyze code for errors and enforce best practices (e.g., ESLint).
- **Formatters**: Automatically format code for readability (e.g., Prettier).

### Example of Using ESLint:

```sh
npm install eslint --save-dev
npx eslint --init
```

## What Is Memory Management, and How Does It Work in JavaScript?

JavaScript uses **automatic garbage collection** to manage memory. The process includes:

1. **Allocation**: Memory is allocated when variables and objects are created.
2. **Usage**: JavaScript tracks references to objects.
3. **Garbage Collection**: When an object is no longer referenced, it is removed from memory.

### Example:

```js
let obj = { name: "Alice" };
obj = null; // The object is now eligible for garbage collection
```

## What Are Closures, and How Do They Work?

A **closure** is a function that remembers variables from its lexical scope even when executed outside that scope.

### Example:

```js
function outerFunction(outerVariable) {
    return function innerFunction(innerVariable) {
        console.log(`Outer: ${outerVariable}, Inner: ${innerVariable}`);
    };
}

const newFunc = outerFunction("Hello");
newFunc("World"); // Outer: Hello, Inner: World

