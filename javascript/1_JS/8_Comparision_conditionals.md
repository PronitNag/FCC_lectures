# JavaScript Notes

## How Do Comparisons Work with Null and Undefined Data Types?

### Equality Comparison (`==` vs `===`)
- `null` and `undefined` are loosely equal (`==`) but not strictly equal (`===`).
- When compared to other values, both usually convert to `false`, except in strict comparisons.

```js
console.log(null == undefined);  // true
console.log(null === undefined); // false
console.log(null == 0);          // false
console.log(undefined == 0);     // false
```

### Comparison Operators (`>`, `<`, `>=`, `<=`)
- `null` behaves like `0` in numeric comparisons.
- `undefined` is treated as `NaN`, making all comparisons with it return `false`.

```js
console.log(null > 0);  // false
console.log(null >= 0); // true (null is converted to 0)
console.log(undefined > 0);  // false
console.log(undefined < 0);  // false
console.log(undefined == 0); // false
```

## Not Passed
- If a function parameter is **not passed**, it becomes `undefined`.
- You can provide default values using function parameters.

```js
function greet(name) {
    console.log("Hello, " + name);
}
greet(); // Hello, undefined
```

- Using default values:

```js
function greet(name = "Guest") {
    console.log("Hello, " + name);
}
greet(); // Hello, Guest
greet("Alice"); // Hello, Alice
```

## What Are Switch Statements and How Do They Differ from If/Else Chains?

### Switch Statement
- Used when comparing a variable against multiple possible values.
- Uses `case` and `break` to prevent fall-through.

```js
let fruit = "apple";
switch (fruit) {
    case "banana":
        console.log("Banana is yellow");
        break;
    case "apple":
        console.log("Apple is red");
        break;
    default:
        console.log("Unknown fruit");
}
```

### If/Else Chain
- More flexible but can be less readable for multiple conditions.

```js
let fruit = "apple";
if (fruit === "banana") {
    console.log("Banana is yellow");
} else if (fruit === "apple") {
    console.log("Apple is red");
} else {
    console.log("Unknown fruit");
}
```

### Differences
| Feature        | Switch Statement | If/Else Chain |
|--------------|-----------------|--------------|
| Readability  | Cleaner for multiple exact values | Better for complex conditions |
| Performance  | Potentially faster for many cases | Might be slower with many checks |
| Condition Type | Strict equality (`===`) | Can use any condition |

