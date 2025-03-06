# JavaScript Basics

## What Is JavaScript, and How Does It Work with HTML and CSS?
JavaScript is a programming language used to create dynamic and interactive content on web pages. It works alongside:
- **HTML** (structure)
- **CSS** (styling)
- **JavaScript** (behavior)

Example:
```html
<!DOCTYPE html>
<html>
<head>
    <title>JS Example</title>
    <script>
        function showMessage() {
            alert('Hello, JavaScript!');
        }
    </script>
</head>
<body>
    <button onclick="showMessage()">Click Me</button>
</body>
</html>
```

---

## What Is a Data Type, and What Are the Different Data Types in JavaScript?
Data types define the kind of values a variable can hold. JavaScript has:
1. **Primitive Types**
   - Number
   - String
   - Boolean
   - Undefined
   - Null
   - Symbol
   - BigInt
2. **Reference Types**
   - Objects
   - Arrays
   - Functions

Example:
```js
let age = 25;         // Number
let name = "John";    // String
let isStudent = true; // Boolean
let value;            // Undefined
let empty = null;     // Null
```

---

## What Are Variables, and What Are Guidelines for Naming JavaScript Variables?
Variables store data in JavaScript. They should:
- Be meaningful and descriptive
- Start with a letter, `_`, or `$`
- Use camelCase

Example:
```js
let userName = "Alice";
let $amount = 100;
let _tempValue = 50;
```

---

## How Do `let` and `const` Work Differently When It Comes to Variable Declaration, Assignment, and Reassignment?
- `let`: Allows reassignment
- `const`: Cannot be reassigned

Example:
```js
let x = 10;
x = 20; // Allowed

const y = 30;
y = 40; // Error: Assignment to constant variable
```

---

## What Is a String in JavaScript, and What Is String Immutability?
A string is a sequence of characters. Strings are **immutable**, meaning they cannot be changed after creation.

Example:
```js
let str = "Hello";
str[0] = "J"; // This won't change the string
console.log(str); // Output: "Hello"
```

---

## What Is String Concatenation, and How Can You Concatenate Strings with Variables?
String concatenation joins two or more strings.

Example:
```js
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;
console.log(fullName); // Output: "John Doe"
```

Using Template Literals:
```js
let fullName = `${firstName} ${lastName}`;
```

---

## What Is `console.log` Used For, and How Does It Work?
`console.log` is used for debugging and printing output to the console.

Example:
```js
console.log("Hello, World!");
```

---

## What Is the Role of Semicolons in JavaScript, and Programming in General?
Semicolons indicate the end of a statement. JavaScript has **Automatic Semicolon Insertion (ASI)**, but it's best practice to use semicolons to avoid errors.

Example:
```js
let a = 5;
let b = 10;
console.log(a + b);
```

---

## What Are Comments in JavaScript, and When Should You Use Them?
Comments help explain code.

- **Single-line comment**
```js
// This is a comment
console.log("Hello");
```
- **Multi-line comment**
```js
/*
This is a 
multi-line comment
*/
console.log("World");
