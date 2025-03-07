# JavaScript Modules

## What Is a Module in JavaScript?
A **module** in JavaScript is a file containing reusable code. Modules help organize code, promote reusability, and maintainability by encapsulating functionality.

### Benefits of Using Modules:
- **Encapsulation**: Prevents global scope pollution.
- **Reusability**: Use the same module across different files.
- **Maintainability**: Easier to manage and debug.
- **Better Dependency Management**: Import only what is needed.

## Exporting and Importing Modules
JavaScript provides two types of exports: 
1. **Named Exports**
2. **Default Exports**

### 1. Named Exports
Used when exporting multiple values from a module.

#### Exporting Named Values:
```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```

#### Importing Named Values:
```javascript
// main.js
import { add, subtract } from "./math.js";

console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2
```

#### Importing with Aliases:
```javascript
import { add as sum } from "./math.js";
console.log(sum(10, 5)); // Output: 15
```

### 2. Default Export
Used when a module exports a single main function/class/value.

#### Exporting a Default Value:
```javascript
// logger.js
export default function logMessage(message) {
  console.log("Log:", message);
}
```

#### Importing a Default Export:
```javascript
// main.js
import logMessage from "./logger.js";
logMessage("Hello, Modules!");
// Output: Log: Hello, Modules!
```

## Dynamic Imports (Importing Modules at Runtime)
Useful for lazy loading.

```javascript
async function loadMathModule() {
  const math = await import("./math.js");
  console.log(math.add(10, 2)); // Output: 12
}

loadMathModule();
```

## Summary
- Use **named exports** when exporting multiple values.
- Use **default export** when exporting a single primary value.
- Use **dynamic imports** for lazy loading.

JavaScript modules make code more modular, reusable, and maintainable!

