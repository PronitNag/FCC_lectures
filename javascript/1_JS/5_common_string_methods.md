# JavaScript String Manipulation Notes

## What Is ASCII, and How Does It Work with `charCodeAt()` and `fromCharCode()`?
ASCII (American Standard Code for Information Interchange) is a character encoding standard for text. In JavaScript, you can work with ASCII values using:

- `charCodeAt(index)`: Returns the ASCII code of a character at a specified index in a string.
- `fromCharCode(code)`: Converts ASCII codes into characters.

### Example:
```javascript
let char = 'A';
console.log(char.charCodeAt(0)); // 65

let asciiCode = 65;
console.log(String.fromCharCode(asciiCode)); // 'A'
```

## How Can You Test if a String Contains a Substring?
Use the `includes()` method to check if a string contains a specific substring.

### Example:
```javascript
let text = "Hello, world!";
console.log(text.includes("world")); // true
```

## How Can You Extract a Substring from a String?
Use the `slice()`, `substring()`, or `substr()` methods:

### Example:
```javascript
let str = "JavaScript";
console.log(str.slice(0, 4)); // 'Java'
console.log(str.substring(0, 4)); // 'Java'
```

## How Can You Change the Casing for a String?
Use `toUpperCase()` and `toLowerCase()`:

### Example:
```javascript
let str = "Hello";
console.log(str.toUpperCase()); // 'HELLO'
console.log(str.toLowerCase()); // 'hello'
```

## How Can You Replace Parts of a String with Another?
Use the `replace()` method:

### Example:
```javascript
let text = "Hello, world!";
console.log(text.replace("world", "JavaScript")); // 'Hello, JavaScript!'
```

## How Can You Repeat a String x Number of Times?
Use the `repeat()` method:

### Example:
```javascript
let str = "Hi ";
console.log(str.repeat(3)); // 'Hi Hi Hi '
```

## How Can You Trim Whitespace from a String?
Use `trim()`, `trimStart()`, and `trimEnd()`:

### Example:
```javascript
let text = "  Hello  ";
console.log(text.trim()); // 'Hello'
console.log(text.trimStart()); // 'Hello  '
console.log(text.trimEnd()); // '  Hello'
