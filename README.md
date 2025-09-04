# JS-Mastering
To-Do 
* Object oriented programming concepts.
* links -> https://github.com/sudheerj/javascript-interview-questions?tab=readme-ov-file#why-is-it-important-to-remove-event-listeners-after-use 
* -> What is `this`?
this is a special keyword in JavaScript that refers to the execution context (the object that is currently calling the function).
Its value is determined at runtime, not at declaration.
* -> What is an `Object` in JavaScript?

An object is a collection of key–value pairs (properties and methods).

Keys are strings or symbols, and values can be any data type (including other objects or functions).
* ->  What is a `Prototyp`e?

Every object in JavaScript has a hidden property called [[Prototype]] (sometimes shown as __proto__).

A prototype is itself an object, used as a blueprint for other objects.
`Object = collection of properties & methods (real data).`

`Prototype = “blueprint” object used for inheritance (shared methods/behaviors).`

`Prototype chain = JS looks up properties through a chain of objects until it finds it (or reaches null).`

If you try to access a property that doesn’t exist on the object, JavaScript will look for it in the prototype chain.

`*The prototype chain enables inheritance in JavaScript.
*If a property isn’t found on an object, JavaScript looks up its prototype chain.
*The prototype of an object instance can be accessed with Object.getPrototypeOf(obj) or __proto__.
*The prototype of a constructor function is available via Constructor.prototype.
*The chain ends when the prototype is null.`


* -> The Object.assign method is used to copy all the properties from one or more source objects and stores them into a target object. This is mainly used for cloning and merging.
* -> A Singleton is an object which can only be instantiated one time. Repeated calls to its constructor return the same instance. This way one can ensure that they don't accidentally create multiple instances.
* -> `call, apply, and bind`

*-> `JSON (JavaScript Object Notation)` is a lightweight, text-based data format that uses JavaScript object syntax for structuring data. It was popularized by Douglas Crockford and is widely used for transmitting data between a server and a client in web applications.
* -> The` slice()` method does not mutate (change) the original array; instead, it returns a new array containing the extracted elements.
*->  `splice()` modifies the original array in place and returns an array containing the removed elements.

`array.splice(start, deleteCount, item1, item2, ...)` - > You can use it both to remove and insert elements in a single operation.

`Maps in JavaScript`

A Map is a built-in object introduced in ES6 that is designed specifically for key–value storage.

Keys can be of any type (objects, functions, primitives).

Keeps insertion order of keys.

Has useful built-in methods.

0 == false            // true      (loose equality, type coercion)
0 === false           // false     (strict equality, different types)
1 == "1"              // true      (string converted to number)
1 === "1"             // false     (different types)
null == undefined     // true      (special case)
null === undefined    // false     (different types)
'0' == false          // true      ('0' is converted to 0)
'0' === false         // false     (different types)
NaN == NaN            // false     (NaN is never equal to itself)
NaN === NaN           // false
[] == []              // false     (different array objects)
[] === []             // false
{} == {}              // false     (different object references)
{} === {}             // false

#  lambda expressions or arrow functions - >  shorter and more readable, especially for simple operations or callbacks.

# first-class function/ citizens, You can assign a function to a variable.
# You can pass a function as an argument to another function.
# You can return a function from another function.
