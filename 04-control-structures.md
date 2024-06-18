# Lesson 2.2: Control Structures

## Overview

In this lesson, we will delve into control structures in JavaScript. Control structures are used to dictate the flow of the program. We will explore conditional statements, loops, and error handling.

## Table of Contents
1. Conditional Statements
    - if
    - else
    - switch
2. Loops
    - for
    - while
    - do-while
3. Error Handling
    - try
    - catch
    - finally

---

## 1. Conditional Statements

Conditional statements are used to perform different actions based on different conditions.

### if
The `if` statement executes a block of code if a specified condition is true.

```javascript
let age = 18;

if (age >= 18) {
    console.log("You are an adult.");
}
```

### else 

The else statement executes a block of code if the same condition is false.

```javascript
let age = 16;

if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are not an adult.");
}
```

### switch

The switch statement evaluates an expression and executes code blocks based on the matching case.

```javascript
let fruit = "apple";

switch (fruit) {
    case "banana":
        console.log("Banana is yellow.");
        break;
    case "apple":
        console.log("Apple is red.");
        break;
    case "orange":
        console.log("Orange is orange.");
        break;
    default:
        console.log("Unknown fruit.");
}
```

## 2. Loops

Loops are used to repeatedly run a block of code until a specified condition is met.

### for

The for loop repeats a block of code a specified number of times.

```javascript
for (let i = 0; i < 5; i++) {
    console.log(`Iteration ${i}`);
}
```

### while

The while loop executes a block of code as long as the specified condition is true.

```javascript
let i = 0;

while (i < 5) {
    console.log(`Iteration ${i}`);
    i++;
}
```

### do-while

The do-while loop is similar to the while loop, but it executes the block of code once before checking the condition.

```javascript
let i = 0;

do {
    console.log(`Iteration ${i}`);
    i++;
} while (i < 5);
```

## 3. Error Handling

Error handling in JavaScript is done using try, catch, and finally blocks to handle exceptions and perform clean-up actions.

### try
The try block allows you to define a block of code to be tested for errors while it is being executed.

### catch
The catch block allows you to define a block of code to be executed, if an error occurs in the try block.

### finally
The finally block lets you execute code, after try and catch, regardless of the result.

```javascript
try {
    let result = riskyOperation();
    console.log(`Result: ${result}`);
} catch (error) {
    console.log(`An error occurred: ${error.message}`);
} finally {
    console.log("This will always be executed.");
}
```

## Summary
In this lesson, we covered the key control structures in JavaScript, including conditional statements, loops, and error handling mechanisms. These constructs are fundamental for controlling the flow of a program and handling errors gracefully.
