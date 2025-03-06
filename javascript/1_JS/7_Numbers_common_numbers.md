# JavaScript Number Methods

## How Does `isNaN()` Work?

The `isNaN()` function checks if a value is **Not-a-Number (NaN)**. It returns `true` if the value is `NaN` and `false` otherwise.

### Example:
```js
console.log(isNaN(123));       // false (123 is a number)
console.log(isNaN("hello"));  // true (Cannot be converted to a number)
console.log(isNaN("123"));    // false (String can be converted to number)
console.log(isNaN(NaN));       // true (NaN is NaN)
```

---

## How Do `parseFloat()` and `parseInt()` Work?

### `parseFloat()`
`parseFloat()` converts a string into a floating-point number.

#### Example:
```js
console.log(parseFloat("3.14"));   // 3.14
console.log(parseFloat("10.5px")); // 10.5 (Stops at first non-numeric character)
console.log(parseFloat("abc"));    // NaN (Not a valid number)
```

### `parseInt()`
`parseInt()` converts a string into an integer, ignoring decimal values.

#### Example:
```js
console.log(parseInt("42"));      // 42
console.log(parseInt("42.99"));  // 42 (Only integer part is taken)
console.log(parseInt("10px"));   // 10 (Stops at first non-numeric character)
console.log(parseInt("abc"));    // NaN (Not a valid number)
```

---

## What Is the `toFixed()` Method, and How Does It Work?

The `toFixed()` method formats a number to a specified number of decimal places and returns it as a string.

### Example:
```js
let num = 3.14159;
console.log(num.toFixed(2)); // "3.14"
console.log(num.toFixed(4)); // "3.1416" (Rounds up the last digit)
console.log((1.9).toFixed(0)); // "2" (Rounds to the nearest integer)
```

**Note:** `toFixed()` always returns a string, so you may need to convert it back to a number if needed:
```js
let fixedNum = parseFloat(num.toFixed(2)); // 3.14 as a number
