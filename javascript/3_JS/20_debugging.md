# JavaScript Error Handling & Debugging

## Common JavaScript Errors

JavaScript errors can be categorized into different types:

1. **Syntax Errors** – Occur when there is a mistake in the code syntax.
   ```js
   console.log('Hello World' // Missing closing parenthesis
   ```

2. **Reference Errors** – Occur when trying to access an undefined variable.
   ```js
   console.log(notDefinedVar); // ReferenceError: notDefinedVar is not defined
   ```

3. **Type Errors** – Occur when performing an invalid operation on a data type.
   ```js
   let num = 10;
   num.toUpperCase(); // TypeError: num.toUpperCase is not a function
   ```

4. **Range Errors** – Occur when using a number outside of the allowed range.
   ```js
   let arr = new Array(-5); // RangeError: Invalid array length
   ```

---

## The `throw` Statement

The `throw` statement allows you to manually generate exceptions.

```js
function divide(a, b) {
    if (b === 0) {
        throw new Error("Cannot divide by zero");
    }
    return a / b;
}

console.log(divide(10, 2)); // 5
console.log(divide(10, 0)); // Error: Cannot divide by zero
```

---

## The `try...catch...finally` Statement

Used for handling exceptions gracefully.

```js
try {
    let result = JSON.parse('{invalidJson}');
} catch (error) {
    console.log("Error occurred:", error.message);
} finally {
    console.log("This will always execute.");
}
```

---

## The `debugger` Statement

The `debugger` statement pauses script execution if developer tools are open.

```js
function testDebug() {
    let x = 5;
    debugger; // Execution will pause here in dev tools
    x += 10;
    console.log(x);
}

testDebug();
```

---

## Advanced JavaScript Debugging Techniques

1. **Using `console.table()` to log objects**
   ```js
   let users = [
       { id: 1, name: "Alice" },
       { id: 2, name: "Bob" }
   ];
   console.table(users);
   ```

2. **Using Breakpoints in DevTools**
   - Open Developer Console (F12 or Right Click > Inspect).
   - Navigate to the "Sources" tab.
   - Click on the line number to set a breakpoint.

3. **Using `performance.now()` for profiling**
   ```js
   let start = performance.now();
   for (let i = 0; i < 1000000; i++) {} // Simulating workload
   let end = performance.now();
   console.log(`Execution time: ${end - start}ms`);
   ```

4. **Monitoring Events with `monitorEvents()`**
   - Open the browser console and run:
   ```js
   monitorEvents(document, 'click');
   ```

These techniques help in efficiently debugging JavaScript code and improving performance.


# JavaScript Debugging Notes

## Use the JavaScript Console to Check the Value of a Variable

The `console.log()` method is used to print values to the console for debugging.

```javascript
let x = 10;
console.log(x); // Output: 10
```

## Understanding the Differences between the freeCodeCamp and Browser Console

- The freeCodeCamp console may not always behave the same as the browser console.
- The browser console (F12 in most browsers) provides more detailed errors and logs.

## Use typeof to Check the Type of a Variable

The `typeof` operator returns the data type of a variable.

```javascript
let name = "John";
console.log(typeof name); // Output: string
```

## Catch Misspelled Variable and Function Names

Misspelled variables or function names cause reference errors.

```javascript
let myVar = 42;
console.log(myVar); // Correct
console.log(myvar); // ReferenceError: myvar is not defined
```

## Catch Unclosed Parentheses, Brackets, Braces, and Quotes

Ensure all brackets and quotes are properly closed.

```javascript
function add(a, b) {
  return a + b; // Correct
}

// Incorrect: Missing closing parenthesis
// function add(a, b {
```

## Catch Mixed Usage of Single and Double Quotes

Use consistent quotes to avoid syntax errors.

```javascript
let str = "Hello, world!"; // Correct
// let str = "Hello, world!'; // Incorrect
```

## Catch Use of Assignment Operator Instead of Equality Operator

Use `===` for comparison instead of `=`.

```javascript
let a = 5;
if (a === 5) { // Correct
  console.log("Equal");
}
```

## Catch Missing Open and Closing Parenthesis After a Function Call

Functions must be called with parentheses.

```javascript
function greet() {
  return "Hello!";
}

console.log(greet()); // Correct
// console.log(greet; // Incorrect
```

## Catch Arguments Passed in the Wrong Order When Calling a Function

Ensure the correct order of arguments.

```javascript
function divide(a, b) {
  return a / b;
}

console.log(divide(10, 2)); // Correct: 5
console.log(divide(2, 10)); // Incorrect: 0.2
```

## Catch Off By One Errors When Using Indexing

Indexes start at 0, not 1.

```javascript
let arr = ["a", "b", "c"];
console.log(arr[0]); // Correct: "a"
// console.log(arr[3]); // Incorrect: undefined
```

## Use Caution When Reinitializing Variables Inside a Loop

Avoid unnecessary re-declarations inside loops.

```javascript
for (let i = 0; i < 5; i++) {
  let x = i * 2; // Correct
  console.log(x);
}
```

## Prevent Infinite Loops with a Valid Terminal Condition

Ensure loops have a valid exit condition.

```javascript
let i = 0;
while (i < 5) { // Correct
  console.log(i);
  i++;
}

// Incorrect: Infinite loop
// while (true) {
//   console.log("Looping");
// }

