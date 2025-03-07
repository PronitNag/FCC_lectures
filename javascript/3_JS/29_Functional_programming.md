# Functional Programming and Currying

## What Is Functional Programming?
Functional programming (FP) is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. 

### Key Principles of Functional Programming:
- **First-class functions**: Functions can be assigned to variables, passed as arguments, and returned from other functions.
- **Pure functions**: A function always produces the same output for the same input and has no side effects.
- **Immutability**: Data should not be changed after it is created.
- **Function composition**: Small functions are combined to create more complex functions.
- **Higher-order functions**: Functions that can take other functions as arguments or return them.

### Example in JavaScript:
```javascript
// Pure function example
function add(a, b) {
    return a + b;
}
console.log(add(3, 4)); // Output: 7
```

### Example in C++:
```cpp
#include <iostream>
#include <functional>

// A pure function in C++
int add(int a, int b) {
    return a + b;
}

int main() {
    std::cout << add(3, 4) << std::endl; // Output: 7
    return 0;
}
```

---

## What Is Currying, and How Does It Work?
Currying is a technique in functional programming where a function is transformed into a sequence of functions, each taking a single argument.

### Benefits of Currying:
- **Reusability**: Functions can be reused with partially applied arguments.
- **Function Composition**: Helps in creating small reusable functions.
- **Readability**: Improves code readability and modularity.

### Example in JavaScript:
```javascript
// Normal function
function add(a, b) {
    return a + b;
}

console.log(add(3, 4)); // Output: 7

// Curried version
function curriedAdd(a) {
    return function(b) {
        return a + b;
    };
}

const addThree = curriedAdd(3);
console.log(addThree(4)); // Output: 7
```

### Example in C++:
```cpp
#include <iostream>
#include <functional>

// Curried function using std::function
std::function<std::function<int(int)>(int)> curriedAdd = [](int a) {
    return [a](int b) {
        return a + b;
    };
};

int main() {
    auto addThree = curriedAdd(3);
    std::cout << addThree(4) << std::endl; // Output: 7
    return 0;
}
```

---
By using functional programming and currying, you can write cleaner and more maintainable code. These concepts are widely used in modern programming languages, especially in functional and hybrid languages like JavaScript, C++, Python, and Haskell.

