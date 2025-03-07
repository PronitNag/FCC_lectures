# JavaScript Objects and JSON

## What Is an Object in JavaScript, and How Can You Access Properties from an Object?
An object in JavaScript is a collection of key-value pairs. Properties can be accessed using dot notation or bracket notation.

```javascript
const person = { name: "John", age: 30 };
console.log(person.name);  // Dot notation
console.log(person["age"]); // Bracket notation
```

---
## How Can You Remove Properties from an Object?
You can remove a property using the `delete` operator.

```javascript
const user = { name: "Alice", email: "alice@example.com" };
delete user.email;
console.log(user); // { name: "Alice" }
```

---
## How to Check If an Object Has a Property?
Use the `in` operator or `hasOwnProperty()` method.

```javascript
const car = { brand: "Toyota", model: "Corolla" };
console.log("brand" in car); // true
console.log(car.hasOwnProperty("model")); // true
```

---
## How Do You Work with Accessing Properties from Nested Objects and Arrays in Objects?
Use dot or bracket notation to access nested properties.

```javascript
const employee = { details: { name: "Bob", age: 25 }, skills: ["JS", "React"] };
console.log(employee.details.name); // "Bob"
console.log(employee.skills[0]); // "JS"
```

---
## What Is the Difference Between Primitive and Non-Primitive Data Types?
- **Primitive**: Immutable, stored by value (e.g., `string`, `number`, `boolean`).
- **Non-Primitive**: Mutable, stored by reference (e.g., `object`, `array`).

```javascript
let a = 10;
let b = a; // Copy by value
b = 20;
console.log(a); // 10

let obj1 = { value: 10 };
let obj2 = obj1; // Copy by reference
obj2.value = 20;
console.log(obj1.value); // 20
```

---
## What Is the Difference Between Functions and Object Methods?
A function is independent, whereas an object method is a function inside an object.

```javascript
function greet() {
  return "Hello!";
}
const person = {
  sayHello: function() {
    return "Hello from an object!";
  }
};
console.log(greet()); // "Hello!"
console.log(person.sayHello()); // "Hello from an object!"
```

---
## What Is the Object() Constructor, and When Should You Use It?
The `Object` constructor creates objects explicitly but is less common than object literals.

```javascript
const user = new Object();
user.name = "Charlie";
console.log(user); // { name: "Charlie" }
```

---
## What Is the Optional Chaining Operator, and How Does It Work?
The `?.` operator prevents errors when accessing deeply nested properties that might not exist.

```javascript
const data = { user: { profile: { name: "Sam" } } };
console.log(data.user?.profile?.name); // "Sam"
console.log(data.user?.address?.city); // undefined (no error)
```

---
## What Is Object Destructuring, and How Does It Work?
Destructuring extracts properties from objects into variables.

```javascript
const person = { name: "David", age: 28 };
const { name, age } = person;
console.log(name); // "David"
console.log(age); // 28
```

---
## What Is JSON, and How Do You Access Values Using Bracket and Dot Notation?
JSON (JavaScript Object Notation) is a lightweight data format similar to JavaScript objects.

```javascript
const jsonData = { "name": "Emma", "age": 32 };
console.log(jsonData.name); // Dot notation
console.log(jsonData["age"]); // Bracket notation
```

---
## How Do JSON.parse() and JSON.stringify() Work?
- `JSON.stringify()`: Converts an object into a JSON string.
- `JSON.parse()`: Converts a JSON string into an object.

```javascript
const obj = { title: "Book", price: 20 };
const jsonString = JSON.stringify(obj);
console.log(jsonString); // '{"title":"Book","price":20}'

const parsedObj = JSON.parse(jsonString);
console.log(parsedObj.title); // "Book"

