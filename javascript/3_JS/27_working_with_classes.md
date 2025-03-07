# JavaScript Classes and Related Concepts

## What Are Classes, and How Do They Work in JavaScript?
Classes in JavaScript are a blueprint for creating objects. They encapsulate data and methods that operate on that data.

### Example:
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

const person1 = new Person("Alice", 25);
person1.greet();
```

---

## How Does the `this` Keyword Work?
The `this` keyword refers to the object that is executing the current function.

### Example:
```javascript
class Car {
  constructor(brand) {
    this.brand = brand;
  }

  showBrand() {
    console.log(this.brand);
  }
}

const myCar = new Car("Toyota");
myCar.showBrand(); // Outputs: Toyota
```

`this` behaves differently in various contexts, such as global, function, and event listeners.

---

## What Is Class Inheritance, and How Does It Work?
Class inheritance allows one class to inherit properties and methods from another class using the `extends` keyword.

### Example:
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  makeSound() {
    console.log("Some generic sound");
  }
}

class Dog extends Animal {
  makeSound() {
    console.log("Bark!");
  }
}

const myDog = new Dog("Buddy");
myDog.makeSound(); // Outputs: Bark!
```

---

## What Are Static Properties and Methods in Classes?
Static properties and methods belong to the class itself rather than instances of the class.

### Example:
```javascript
class MathUtility {
  static pi = 3.14159;

  static square(number) {
    return number * number;
  }
}

console.log(MathUtility.pi); // Outputs: 3.14159
console.log(MathUtility.square(5)); // Outputs: 25
```

Static members are accessed directly on the class, not on instances.

---

These concepts form the foundation of object-oriented programming in JavaScript!
