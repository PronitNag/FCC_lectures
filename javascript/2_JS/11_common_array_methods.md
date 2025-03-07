# JavaScript Array Methods - Short Notes

## 1. Get Index of an Element in an Array Using `indexOf`
The `indexOf` method returns the first index of a given element in an array. If the element is not found, it returns `-1`.

```javascript
const numbers = [10, 20, 30, 40, 50];
console.log(numbers.indexOf(30)); // Output: 2
console.log(numbers.indexOf(100)); // Output: -1 (not found)
```

## 2. Add and Remove Elements from the Middle of an Array
The `splice` method is used to add or remove elements at any position in an array.

### Adding Elements
```javascript
const fruits = ["Apple", "Banana", "Mango"];
fruits.splice(1, 0, "Orange"); // Insert "Orange" at index 1
console.log(fruits); // Output: ["Apple", "Orange", "Banana", "Mango"]
```

### Removing Elements
```javascript
fruits.splice(2, 1); // Remove 1 element at index 2
console.log(fruits); // Output: ["Apple", "Orange", "Mango"]
```

## 3. Check if an Array Contains a Certain Value
### Using `includes`
```javascript
const colors = ["Red", "Green", "Blue"];
console.log(colors.includes("Green")); // Output: true
console.log(colors.includes("Yellow")); // Output: false
```

### Using `indexOf`
```javascript
console.log(colors.indexOf("Blue") !== -1); // Output: true
```

## 4. Shallow Copy of an Array
A shallow copy means copying an array without modifying the original. Some ways to create a shallow copy:

### Using `slice()`
```javascript
const original = [1, 2, 3];
const copy = original.slice();
console.log(copy); // Output: [1, 2, 3]
```

### Using Spread Operator `...`
```javascript
const copy2 = [...original];
console.log(copy2); // Output: [1, 2, 3]
```

### Using `Array.from()`
```javascript
const copy3 = Array.from(original);
console.log(copy3); // Output: [1, 2, 3]
```

## 5. Reverse a String Using String and Array Methods
We can use `split()`, `reverse()`, and `join()` to reverse a string.

```javascript
const str = "hello";
const reversed = str.split('').reverse().join('');
console.log(reversed); // Output: "olleh"

