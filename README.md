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
