# 📘 JS-Mastering  

A collection of JavaScript concepts, interview notes, and hands-on examples for mastering core and advanced topics.  

---

## ✅ To-Do  
- Object oriented programming concepts.  
- [JavaScript Interview Questions (Sudheerj)](https://github.com/sudheerj/javascript-interview-questions?tab=readme-ov-file#why-is-it-important-to-remove-event-listeners-after-use)  

---

## 🔹 Core Concepts  

### 🔸 What is `this`?  
`this` is a special keyword in JavaScript that refers to the execution context (the object that is currently calling the function).  
Its value is determined **at runtime**, not at declaration.  

---

### 🔸 What is an Object in JavaScript?  
An object is a collection of key–value pairs (properties and methods).  

- Keys are **strings or symbols**.  
- Values can be **any data type** (including other objects or functions).  

---

### 🔸 What is a Prototype?  
Every object in JavaScript has a hidden property called `[[Prototype]]` (sometimes shown as `__proto__`).  
A prototype is itself an object, used as a **blueprint** for other objects.  

- **Object** = collection of properties & methods (real data).  
- **Prototype** = “blueprint” object used for inheritance (shared methods/behaviors).  
- **Prototype chain** = JS looks up properties through a chain of objects until it finds it (or reaches `null`).  

**Key points:**  
- The prototype chain enables inheritance in JavaScript.  
- If a property isn’t found on an object, JavaScript looks up its prototype chain.  
- The prototype of an object instance → `Object.getPrototypeOf(obj)` or `__proto__`.  
- The prototype of a constructor function → `Constructor.prototype`.  
- The chain ends when the prototype is `null`.  

---

### 🔸 `Object.assign()`  
Used to copy all the properties from one or more source objects into a target object.  
Mainly used for **cloning** and **merging**.  

---

### 🔸 Singleton  
A singleton is an object that can only be instantiated **once**.  
Repeated calls to its constructor return the same instance.  

---

### 🔸 `call`, `apply`, and `bind`  
Ways to explicitly control the value of `this`.  

---

### 🔸 JSON  
`JSON (JavaScript Object Notation)` is a lightweight, text-based data format using JS object syntax.  
- Popularized by Douglas Crockford.  
- Widely used for transmitting data between a server and a client.  

---

### 🔸 Array Methods: `slice()` vs `splice()`  
- `slice()` → does **not mutate** the original array, returns a **new array**.  
- `splice()` → **modifies** the original array, returns removed elements.  

```js
array.splice(start, deleteCount, item1, item2, ...)

// Can remove and insert elements in a single operation.
```

---

## 🔸 Maps in JavaScript  

- A `Map` is a built-in object introduced in **ES6** that is designed specifically for **key–value storage**.  
- Keys can be of **any type** (objects, functions, primitives).  
- Maintains **insertion order** of keys.  
- Provides **useful built-in methods** like `.set()`, `.get()`, `.has()`, `.delete()`, and `.size`.  

---

## 🔸 Equality in JavaScript  

```js
0 == false            // true   (loose equality, type coercion)
0 === false           // false  (strict equality, different types)

1 == "1"              // true   (string converted to number)
1 === "1"             // false  (different types)

null == undefined     // true   (special case)
null === undefined    // false  (different types)

'0' == false          // true   ('0' is converted to 0)
'0' === false         // false  (different types)

NaN == NaN            // false  (NaN is never equal to itself)
NaN === NaN           // false

[] == []              // false  (different array objects)
[] === []             // false

{} == {}              // false  (different object references)
{} === {}             // false
```

### Lambda Expressions / Arrow Functions  
Shorter and more readable, especially for simple operations or callbacks.  

---

### First-Class Functions / Citizens  

You can assign a function to a variable:  
```js
const greet = function(name) {
  return "Hello, " + name;
};
console.log(greet("Aleena")); // Hello, Aleena
```
##### You can pass a function as an argument to another function.
```
function sayHello() {
  return "Hello!";
}

function greet(fn) {
  console.log(fn()); 
}

greet(sayHello);  // "Hello!"
```
##### You can return a function from another function.
```
function multiplier(factor) {
  return function(number) {
    return number * factor;
  };
}

const double = multiplier(2);
console.log(double(5)); // 10
```
Here, multiplier returns a function → closure is formed.
##### Why is This Important?
 Because of first-class functions, JavaScript supports:
- Callbacks (functions passed as arguments).
- Higher-order functions (functions that take/return other functions).
- Functional programming patterns (map, filter, reduce).
- Async programming (promises, async/await use callbacks under the hood).
### Function Types  

- **First-order function** → does not take another function as an argument and does not return another function.  
- **Higher-order function** → either accepts another function as an argument, returns a function as its result, or both.  
- **Unary function (monadic)** → a function that accepts exactly one argument.  
- **Currying** → process of transforming a function with multiple arguments into a sequence of nested functions, each accepting only one argument at a time.  
```
const curryUnaryFunction = (a) => (b) => (c) => a + b + c;

console.log(curryUnaryFunction(1));       // Returns: function (b) => ...
console.log(curryUnaryFunction(1)(2));    // Returns: function (c) => ...
console.log(curryUnaryFunction(1)(2)(3)); // Output: 6
```
---

### Pure vs Impure Functions  

👉 **Pure Function**  
- Always returns the same output for the same input.  
- Has no side effects (doesn’t modify external state, global variables, DOM, API calls, etc.).  

👉 **Impure Function**  
- May return different outputs for the same inputs.  
- Has side effects (modifies external state, logs to console, changes global variables, DOM, database, etc.).  

###  let - block-scoped local variable.
### var - function-scoped (or globally-scoped if declared outside a function)
| Feature           | `var`                                | `let`                                                |
| ----------------- | ------------------------------------ | ---------------------------------------------------- |
| **Scope**         | Function-scoped                      | Block-scoped (`{}`)                                  |
| **Hoisting**      | Hoisted & initialized as `undefined` | Hoisted but **not initialized** (Temporal Dead Zone) |
| **Redeclaration** | Can be redeclared in the same scope  | Cannot be redeclared in the same scope               |
| **Reassignment**  | Allowed                              | Allowed                                              |
| **Best Use**      | Legacy code (avoid if possible)      | Modern JS (preferred)                                |
