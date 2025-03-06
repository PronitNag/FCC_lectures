# JavaScript String Basics

## What Is Bracket Notation, and How Do You Access Characters from a String?
Bracket notation allows you to access individual characters in a string using their index.

```javascript
let str = "Hello";
console.log(str[0]); // 'H'
console.log(str[4]); // 'o'
```

Indexes start at `0`, so the first character is at index `0`, the second at `1`, and so on.

---

## How Do You Create a Newline in Strings and Escape Strings?
Newlines and special characters can be added using escape sequences.

```javascript
let str = "Hello\nWorld"; // Newline
console.log(str);

let escapeStr = "She said, \"JavaScript is fun!\""; // Escape double quotes
console.log(escapeStr);
```

Common escape sequences:
- `\n` → Newline
- `\t` → Tab
- `\\` → Backslash
- `\"` → Double quote
- `\'` → Single quote

---

## What Are Template Literals, and What Is String Interpolation?
Template literals allow multi-line strings and embedded expressions using backticks (`` ` ``) instead of quotes.

```javascript
let name = "Alice";
let greeting = `Hello, ${name}!`;
console.log(greeting); // "Hello, Alice!"
```

Advantages:
- Supports multi-line strings without `\n`
- Allows variable interpolation with `${}`

```javascript
let multiLine = `This is
a multi-line string.`;
console.log(multiLine);
```

---

## How Can You Find the Position of a Substring in a String?
You can use `indexOf()` or `search()` to find the position of a substring.

```javascript
let text = "Hello, world!";
console.log(text.indexOf("world")); // 7
console.log(text.indexOf("JavaScript")); // -1 (not found)
```

`indexOf()` returns `-1` if the substring is not found.

---

## What Is the prompt() Method, and How Does It Work?
`prompt()` is used to take input from the user in a browser environment.

```javascript
let name = prompt("Enter your name:");
console.log("Hello, " + name);
```

- Displays a dialog box with a text input field.
- Returns the entered value as a string.
- If the user cancels, it returns `null`.

```javascript
let age = prompt("Enter your age:");
if (age !== null) {
    console.log(`You are ${age} years old.`);
} else {
    console.log("No input provided.");
}

