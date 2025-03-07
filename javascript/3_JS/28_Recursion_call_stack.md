# Recursion in JavaScript

## What Is Recursion?
Recursion is a programming technique where a function calls itself to solve a problem. It breaks down complex problems into smaller subproblems until a base condition is met.

## How Recursion Works in JavaScript
A recursive function consists of:
1. **Base Case**: A condition that stops the recursion.
2. **Recursive Case**: The function calls itself with a smaller problem.

### Example: Factorial Function
```javascript
function factorial(n) {
    if (n === 0) return 1; // Base case
    return n * factorial(n - 1); // Recursive case
}
console.log(factorial(5)); // Output: 120
```

### Example: Fibonacci Sequence
```javascript
function fibonacci(n) {
    if (n <= 1) return n; // Base case
    return fibonacci(n - 1) + fibonacci(n - 2); // Recursive case
}
console.log(fibonacci(6)); // Output: 8
```

## Advantages of Recursion
- Simplifies code for problems like tree traversal and divide-and-conquer algorithms.
- Makes it easier to express problems in a mathematical way.

## Disadvantages of Recursion
- Can lead to high memory usage (stack overflow) if not optimized.
- Sometimes less efficient than iterative solutions.

## Optimizing Recursion with Memoization
```javascript
function fibonacciMemo(n, memo = {}) {
    if (n in memo) return memo[n];
    if (n <= 1) return n;
    memo[n] = fibonacciMemo(n - 1, memo) + fibonacciMemo(n - 2, memo);
    return memo[n];
}
console.log(fibonacciMemo(50)); // Optimized Fibonacci calculation
```

## Tail Recursion (ES6+)
Some JavaScript engines optimize tail-recursive calls, preventing stack overflow.
```javascript
function factorialTail(n, acc = 1) {
    if (n === 0) return acc;
    return factorialTail(n - 1, n * acc);
}
console.log(factorialTail(5)); // Output: 120
```

Recursion is a powerful concept, but it should be used wisely to avoid performance issues.

