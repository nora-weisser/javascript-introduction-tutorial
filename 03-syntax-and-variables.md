# Lesson 2.1: Syntax and Variables

## Overview

In this lesson, we will cover the basics of JavaScript syntax and variables. Understanding these fundamental concepts is crucial for writing effective and efficient code. We'll explore different types of variables, data types, and how to use operators and expressions.

## Table of Contents
1. Variables
    - var
    - let
    - const
2. Data Types
    - Strings
    - Numbers
    - Booleans
    - Arrays
    - Objects
3. Operators and Expressions

---

## 1. Variables

Variables are used to store data that can be referenced and manipulated in a program. JavaScript provides three ways to declare variables: `var`, `let`, and `const`.

### var
- **Scope:** Function-scoped.
- **Hoisting:** Variables declared with `var` are hoisted to the top of their scope.
- **Usage:** Generally avoided in modern JavaScript due to scope and hoisting issues.

```javascript
var exampleVar = "I'm a var variable";
```

### let
- **Scope:** Block-scoped.
- **Hoisting:** Variables declared with let are not accessible before declaration.
- **Usage:** Preferred for variables that will change value.


```javascript
let exampleLet = "I'm a let variable";
exampleLet = "I can be changed";
```

### const
- **Scope:** Block-scoped.
- **Hoisting:** Variables declared with const are not accessible before declaration.
- **Usage:** Preferred for variables that should not change value.

```javascript
const exampleConst = "I'm a const variable";
// exampleConst = "This will cause an error"; // Uncommenting this line will throw an error
```

## 2. Data Types

JavaScript supports several data types which can be divided into two categories: primitive types and objects.

### Strings
- Description: Used for textual data.
- Syntax: Can be defined using single quotes ('), double quotes ("), or backticks (`) for template literals.

```javascript
let name = "John Doe";
let greeting = `Hello, ${name}`;
```

### Numbers
- Description: Represents both integer and floating-point numbers.
- Syntax: No distinction between integer and floating-point.

```javascript
let age = 30;
let price = 19.99;
```

### Booleans
- Description: Represents logical values.
- Syntax: true or false.

```javascript
let isStudent = true;
let hasGraduated = false;
```

### Arrays
- Description: Used to store multiple values in a single variable.
- Syntax: Defined using square brackets ([]).

```javascript
let fruits = ["apple", "banana", "cherry"];
```

### Objects
- Description: Used to store collections of data and more complex entities.
- Syntax: Defined using curly braces ({})

```javascript
let person = {
    name: "John Doe",
    age: 30,
    isStudent: true
};
```

## Operators and Expressions

Operators are symbols used to perform operations on operands. Expressions are combinations of values, variables, and operators that compute to a value.

### Arithmetic Operators

#### Addition (+)

```javascript
let sum = 5 + 3; // 8
```

#### Subtraction (-)

```javascript
let difference = 5 - 3; // 2
```

#### Multiplication (*)

```javascript
let product = 5 * 3; // 15
```

#### Division (/)

```javascript
let quotient = 6 / 3; // 2
```

### Assignment Operators

#### Assignment (=)

```javascript
let x = 10;
```

#### Addition assignment (+=)

```javascript
x += 5; // x is now 15
```

### Comparison Operators

#### Equal (==)

```javascript
let isEqual = (5 == "5"); // true
```

#### Strict equal (===)

```javascript
let isStrictEqual = (5 === "5"); // false
```

#### Not equal (!=)

```javascript
let isNotEqual = (5 != "5"); // false
```

#### Strict not equal (!==)

```javascript
let isStrictNotEqual = (5 !== "5"); // true
```

### Logical Operators

#### AND (&&)

```javascript
let isTrue = (true && false); // false
```

#### OR (||)

```javascript
let isEitherTrue = (true || false); // true
```

#### NOT (!)

```javascript
let isNotTrue = !true; // false
```

### Expressions

- Description: Any valid unit of code that resolves to a value.
- Examples:

```javascript
let total = 5 + 10; // 15
let isAdult = age >= 18; // true or false based on age value
```

## Summary
In this lesson, we covered the basics of variables, data types, and operators in JavaScript. Understanding these concepts is essential for writing and understanding JavaScript code effectively. Practice using these elements to become more comfortable with their syntax and behavior.
