# Dynamic Typing in JavaScript vs. Statically Typed Languages

## What Is Dynamic Typing?

Dynamic typing means that a variable's type is determined at runtime rather than at compile time. In JavaScript, you don't need to declare the type of a variable explicitly; it can hold values of different types at different times.

### Example:

```javascript
let value = 42;      // value is a number
console.log(typeof value); // "number"

value = "Hello";    // Now value is a string
console.log(typeof value); // "string"
```

## Difference from Statically Typed Languages

| Feature | Dynamically Typed (JavaScript) | Statically Typed (C++, Java) |
|---------|------------------------------|----------------------------|
| Type Declaration | Not required | Required |
| Type Checking | At runtime | At compile-time |
| Type Safety | Less strict | More strict |
| Flexibility | High | Low |

In statically typed languages like C++ and Java, variables must be declared with a specific type, and type mismatches are caught at compile time.

### Example in C++:

```cpp
int num = 42;
num = "Hello"; // Compilation error: cannot assign a string to an int
```

---

# The `typeof` Operator and the `typeof null` Bug

## How `typeof` Works

The `typeof` operator is used to determine the type of a value in JavaScript.

### Example:

```javascript
console.log(typeof 42);         // "number"
console.log(typeof "Hello");    // "string"
console.log(typeof true);       // "boolean"
console.log(typeof undefined);  // "undefined"
console.log(typeof {});         // "object"
```

## The `typeof null` Bug

In JavaScript, `typeof null` returns "object" due to a historical bug.

### Example:

```javascript
console.log(typeof null); // "object" (this is a known issue)
```

### Why This Happens?
- In early JavaScript implementations, values were stored as type tags.
- The type tag for objects was `0`, and `null` was mistakenly given the same type tag.
- Changing this behavior would break existing code, so it remains as is.

## Correct Way to Check for `null`

To check for `null`, use strict equality (`===`):

```javascript
let value = null;
if (value === null) {
    console.log("Value is null");
}
