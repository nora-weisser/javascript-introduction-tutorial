## Lesson 3.1: Functions

Functions are fundamental building blocks in JavaScript that allow you to encapsulate code for reuse and modularity. In this lesson, we will explore function declarations and expressions, arrow functions, and how to work with parameters and return values.

## Table of Contents
1. Function Declarations and Expressions
2. Arrow Functions
3. Parameters and Return Values

---

## 1. Function Declarations and Expressions

### Function Declarations
A function declaration defines a named function that can be called later in the code. Function declarations are hoisted, meaning they can be called before they are defined in the code.

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("Alice")); // Outputs: Hello, Alice!
```

### Function Expressions
A function expression defines a function as part of a larger expression, typically by assigning it to a variable. Function expressions are not hoisted.

```javascript
const greet = function(name) {
    return `Hello, ${name}!`;
};

console.log(greet("Bob")); // Outputs: Hello, Bob!
```

## 2. Arrow Functions

Arrow functions provide a shorter syntax for writing functions and lexically bind the this value. They are particularly useful for writing concise functions.

### Syntax

Arrow functions use the => syntax and are often used for inline functions.

```javascript
const greet = (name) => {
    return `Hello, ${name}!`;
};

console.log(greet("Charlie")); // Outputs: Hello, Charlie!
```

### Simplified Syntax

For functions with a single expression, you can omit the curly braces and the return keyword.

```javascript
const greet = name => `Hello, ${name}!`;

console.log(greet("Dave")); // Outputs: Hello, Dave!
```

### No ¨this¨ Binding

Arrow functions do not have their own this value; they inherit this from the surrounding scope.

```javascript
function Person(name) {
    this.name = name;
    this.greet = () => {
        console.log(`Hello, ${this.name}!`);
    };
}

const person = new Person("Eve");
person.greet(); // Outputs: Hello, Eve!
```

## 3. Parameters and Return Values

### Parameters

Functions can take parameters, which are values passed to the function when it is called.

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(2, 3)); // Outputs: 5
```

### Default Parameters

You can specify default values for parameters in case no arguments are passed.

```javascript
function greet(name = "Guest") {
    return `Hello, ${name}!`;
}

console.log(greet()); // Outputs: Hello, Guest!
console.log(greet("Frank")); // Outputs: Hello, Frank!
```

### Rest Parameters

Rest parameters allow you to represent an indefinite number of arguments as an array.

```javascript
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4)); // Outputs: 10
```

### Return Values

Functions can return values using the return statement. If no return statement is present, the function returns undefined.

```javascript
function multiply(a, b) {
    return a * b;
}

const result = multiply(4, 5);
console.log(result); // Outputs: 20
```

## Summary

In this lesson, we explored the different ways to define functions in JavaScript, including function declarations, function expressions, and arrow functions. We also covered how to work with parameters, including default and rest parameters, as well as return values. Understanding these concepts is crucial for writing modular and reusable code in JavaScript.
