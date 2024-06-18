## Lesson 3.2: Scope and Closures

Understanding scope and closures is fundamental in JavaScript programming. In this lesson, we will explore global and local scope, function and block scope, and delve into closures and their practical applications.

## Table of Contents
1. Global vs. Local Scope
2. Function Scope and Block Scope
3. Closures and Their Practical Use

---

## 1. Global vs. Local Scope

### Global Scope
Variables declared outside any function are in the global scope. They can be accessed from anywhere in the code.

```javascript
let globalVar = "I'm a global variable";

function showGlobalVar() {
    console.log(globalVar);
}

showGlobalVar(); // Outputs: I'm a global variable
console.log(globalVar); // Outputs: I'm a global variable
```

### Local Scope
Variables declared within a function are in the local scope and can only be accessed within that function.

```javascript
function localScopeExample() {
    let localVar = "I'm a local variable";
    console.log(localVar);
}

localScopeExample(); // Outputs: I'm a local variable
console.log(localVar); // Error: localVar is not defined
```

## 2. Function Scope and Block Scope

### Function Scope
In JavaScript, each function creates a new scope. Variables declared within a function are not accessible outside of that function.


```javascript
function functionScopeExample() {
    var functionScopedVar = "I'm function scoped";
    console.log(functionScopedVar);
}

functionScopeExample(); // Outputs: I'm function scoped
console.log(functionScopedVar); // Error: functionScopedVar is not defined
```

### Block Scope
Variables declared with let or const inside a block (e.g., inside {}) are block-scoped and cannot be accessed outside the block.

```javascript
{
    let blockScopedVar = "I'm block scoped";
    console.log(blockScopedVar); // Outputs: I'm block scoped
}

console.log(blockScopedVar); // Error: blockScopedVar is not defined
```

## 3. Closures and Their Practical Use

### Closures
A closure is a function that has access to its own scope, the scope of the outer function, and the global scope. Closures are created every time a function is created.

```javascript
function outerFunction(outerVar) {
    return function innerFunction(innerVar) {
        console.log(`Outer variable: ${outerVar}`);
        console.log(`Inner variable: ${innerVar}`);
    };
}

const newFunction = outerFunction("outside");
newFunction("inside");
// Outputs:
// Outer variable: outside
// Inner variable: inside
```

### Practical Use of Closures

#### Data Privacy
Closures can be used to create private variables.

```javascript
function createCounter() {
    let count = 0;
    return {
        increment: function() {
            count++;
            return count;
        },
        decrement: function() {
            count--;
            return count;
        }
    };
}

const counter = createCounter();
console.log(counter.increment()); // Outputs: 1
console.log(counter.increment()); // Outputs: 2
console.log(counter.decrement()); // Outputs: 1
```

#### Function Factories
Closures can be used to create functions with preset parameters.

```javascript
function createGreeting(greeting) {
    return function(name) {
        return `${greeting}, ${name}!`;
    };
}

const sayHello = createGreeting("Hello");
console.log(sayHello("Alice")); // Outputs: Hello, Alice!

const sayHi = createGreeting("Hi");
console.log(sayHi("Bob")); // Outputs: Hi, Bob!
```

## Summary
In this lesson, we covered the different types of scope in JavaScript, including global, local, function, and block scope. We also explored closures and their practical uses, such as creating private variables and function factories. Understanding scope and closures is essential for writing robust and maintainable JavaScript code.
