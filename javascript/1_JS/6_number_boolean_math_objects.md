# JavaScript Basics

## Number Type in JavaScript
JavaScript has a single `number` type that includes both integers and floating-point numbers.

### Types of Numbers:
- **Integers**: `let x = 10;`
- **Floating-point numbers**: `let y = 3.14;`
- **Infinity**: `let inf = Infinity;`
- **NaN (Not a Number)**: `let invalid = 0 / 0;`

## Arithmetic Operators
JavaScript supports basic arithmetic operations:
```js
let a = 10, b = 5;
console.log(a + b); // Addition
console.log(a - b); // Subtraction
console.log(a * b); // Multiplication
console.log(a / b); // Division
console.log(a % b); // Modulus (remainder)
console.log(a ** b); // Exponentiation
```

## Numbers and Strings in Calculations
```js
console.log("5" + 3);  // "53" (String Concatenation)
console.log("5" - 3);  // 2 (String converted to Number)
console.log("5" * "2"); // 10 (Both strings converted to numbers)
```

## Operator Precedence
Order of execution follows **BODMAS**:
```js
console.log(5 + 3 * 2); // 11 (* has higher precedence than +)
console.log((5 + 3) * 2); // 16 (Parentheses have highest precedence)
```

## Increment and Decrement Operators
```js
let x = 5;
console.log(++x); // Pre-increment: 6
console.log(x++); // Post-increment: 6 (then x becomes 7)
console.log(--x); // Pre-decrement: 6
console.log(x--); // Post-decrement: 6 (then x becomes 5)
```

## Compound Assignment Operators
```js
let x = 10;
x += 5; // x = x + 5
x -= 3; // x = x - 3
x *= 2; // x = x * 2
x /= 2; // x = x / 2
x %= 3; // x = x % 3
x **= 2; // x = x ** 2
```

## Booleans and Equality Operators
```js
console.log(5 == "5");  // true (loose equality, type conversion)
console.log(5 === "5"); // false (strict equality, no type conversion)
console.log(5 != "5");  // false
console.log(5 !== "5"); // true
```

## Comparison Operators
```js
console.log(5 > 3);   // true
console.log(5 < 3);   // false
console.log(5 >= 5);  // true
console.log(5 <= 4);  // false
```

## Unary Operators
```js
let x = 5;
console.log(-x); // -5 (Negation)
console.log(+"10"); // 10 (Unary plus converts to number)
```

## Bitwise Operators
```js
console.log(5 & 1); // AND (0101 & 0001) -> 0001 -> 1
console.log(5 | 1); // OR (0101 | 0001) -> 0101 -> 5
console.log(5 ^ 1); // XOR (0101 ^ 0001) -> 0100 -> 4
console.log(~5);    // NOT (~0101) -> 1010 (in 2's complement)
console.log(5 << 1); // Left Shift (0101 << 1) -> 1010 -> 10
console.log(5 >> 1); // Right Shift (0101 >> 1) -> 0010 -> 2
```

## Conditional Statements (if/else if/else)
```js
let num = 10;
if (num > 10) {
    console.log("Greater than 10");
} else if (num === 10) {
    console.log("Equal to 10");
} else {
    console.log("Less than 10");
}
```

## Binary Logical Operators
```js
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true); // false (NOT)
```

## Math Object
```js
console.log(Math.PI); // 3.141592653589793
console.log(Math.sqrt(16)); // 4
console.log(Math.pow(2, 3)); // 8
console.log(Math.round(4.7)); // 5
console.log(Math.floor(4.7)); // 4
console.log(Math.ceil(4.3)); // 5
console.log(Math.random()); // Random number between 0 and 1
