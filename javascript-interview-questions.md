## JavaScript Interview Questions
### Easy Questions:
1. What is JavaScript?

 - JavaScript is a high-level, interpreted programming language that conforms to the ECMAScript specification. It is used primarily to create interactive effects within web browsers.

2. What are the data types in JavaScript?

JavaScript data types include:
 - Primitive: Number, String, Boolean, Undefined, Null, Symbol, BigInt
 - Non-primitive: Object (including Array, Function, Date, etc.)

3. What is the difference between var, let, and const?

 - var: Function-scoped or globally-scoped, can be redeclared and updated.
 - let: Block-scoped, cannot be redeclared within the same scope, but can be updated.
 - const: Block-scoped, cannot be redeclared or updated.

4. What is NaN in JavaScript?

 - NaN stands for "Not-a-Number" and is a value representing an undefined or unrepresentable number. It is a property of the global object.

5. What is undefined and null in JavaScript?

 - undefined: A variable that has been declared but not assigned a value.
 - null: An assignment value representing no value or no object.

6. What are JavaScript functions and how are they declared?

 - Functions are blocks of code designed to perform a particular task. They are declared using the function keyword.
 > function myFunction() {
// code to be executed
}

7. What are arrow functions?

 - Arrow functions are a shorthand syntax for writing function expressions. They do not have their own this context.
 > const myFunction = () => {
// code to be executed
}

8. What is an array in JavaScript?

 - An array is a single variable that is used to store different elements. It is a special type of object that has indexed elements.
 > let fruits = ["Apple", "Banana", "Cherry"];

9. What is the difference between == and ===?

 - ==: Checks for equality after type coercion.
 - ===: Checks for equality without type coercion (strict equality).

10. What is a closure in JavaScript?

 - A closure is a function that retains access to its lexical scope, even when the function is executed outside that scope.
 > function outer() {
let count = 0;
return function inner() {
count++;
return count;
}
}
const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2

11. What are template literals?

 - Template literals are string literals that allow embedded expressions. They are enclosed by backticks (`).
 > let name = "John";
let message = `Hello, ${name}!`;

12. What is the this keyword in JavaScript?

 - The this keyword refers to the object it belongs to. Its value is determined by how a function is called.

13. What is the purpose of the async and await keywords?

 - async and await are used to handle asynchronous operations in JavaScript. async declares a function as asynchronous, and await pauses the execution until the promise is resolved.
 > async function fetchData() {
let response = await fetch('url');
let data = await response.json();
return data;
}

14. What is an event in JavaScript?

 - An event is an action or occurrence detected by JavaScript, such as a user clicking a button or loading a webpage.

15. What is the DOM?

 - The DOM (Document Object Model) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content.

16. How do you add an event listener in JavaScript?

 - You use the addEventListener method to add an event listener to an element.
 > document.getElementById("myBtn").addEventListener("click", function() {
alert("Button was clicked!");
});

17. What is JSON?

 - JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write, and easy for machines to parse and generate.

18. What is the difference between map() and forEach()?

 - map(): Returns a new array with the results of calling a function for every array element.
 - forEach(): Executes a provided function once for each array element, but does not return a new array.

19. What is a promise in JavaScript?

 - A promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value.

20. What is the use strict directive?

 - The use strict directive is a way to enforce stricter parsing and error handling in your JavaScript code. It helps in catching common coding mistakes and unsafe actions.

### Moderate Questions:
1. What is hoisting in JavaScript?

 - Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope. Both variable and function declarations are hoisted, but assignments are not.
 > console.log(x); // undefined
var x = 5;

2. What is the event loop in JavaScript?

 - The event loop is a mechanism that handles the execution of multiple chunks of your program, enabling non-blocking operations. It continuously checks the call stack and the callback queue, pushing callback functions onto the call stack when it is empty.

3. What is the difference between call(), apply(), and bind()?

 - call(): Invokes a function with a given this value and arguments provided individually.
 - apply(): Invokes a function with a given this value and arguments provided as an array.
 - bind(): Creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments.

4. What are higher-order functions?

 - Higher-order functions are functions that can take other functions as arguments and/or return functions as their results.
 > function greet(name) {
return function(message) {
console.log(`${message}, ${name}`);
}
}
const greetJohn = greet('John');
greetJohn('Hello'); // Hello, John

5. What is the prototype in JavaScript?

 - Every JavaScript object has a prototype. The prototype is also an object. All JavaScript objects inherit their properties and methods from their prototype.

6. What is the difference between == and ===?

 - == compares values for equality, with type conversion if necessary. === compares values and types for equality without type conversion.

7. What is a module in JavaScript?

 - A module is a file containing JavaScript code that has its own scope. Variables, functions, and classes defined in one module are not visible to other modules unless explicitly exported and imported.

8. What are JavaScript Promises and how do they work?

 - Promises are used to handle asynchronous operations in JavaScript. They represent a value that may be available now, or in the future, or never.
 > let promise = new Promise(function(resolve, reject) {
// do something
if (success) {
resolve(result);
} else {
reject(error);
}
});
promise.then(
result => console.log(result),
error => console.log(error)
);

9. What is event delegation in JavaScript?

 - Event delegation is a technique of using a single event listener to manage all similar events within a container element. It takes advantage of event bubbling to handle events efficiently.

10. What is the difference between null and undefined?

 - null: An assignment value that represents no value or no object.
 - undefined: A variable that has been declared but not assigned a value.

11. What is a generator function in JavaScript?

 - A generator function is a function that can pause its execution and return multiple values through the yield keyword. They are defined using function* syntax.
 > function* generator() {
yield 1;
yield 2;
yield 3;
}
const gen = generator();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3

12. What is the difference between function declaration and function expression?

 - Function declaration: Named function defined using the function keyword. They are hoisted to the top of their scope.
 > function myFunction() {
// code
}
Function expression: Can be named or anonymous and is not hoisted.
javascript
Skopiuj kod
const myFunction = function() {
// code
}

13. What are JavaScript frameworks and libraries?

 - JavaScript frameworks (e.g., Angular, React, Vue) provide a structured way to build applications, offering a complete solution with built-in tools. Libraries (e.g., jQuery, Lodash) are collections of pre-written code that you can use to perform common tasks.

14. What is the purpose of the async and await keywords?

 - async is used to declare an asynchronous function, and await is used to pause the execution of the function until the awaited promise is resolved.
 > async function fetchData() {
let response = await fetch('url');
let data = await response.json();
return data;
}

15. What are JavaScript callbacks?

 - A callback is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
 > function greet(name, callback) {
console.log('Hello ' + name);
callback();
}
function callMe() {
console.log('I am a callback function');
}
greet('John', callMe);

16. What are let, const, and var in JavaScript?

 - var: Function-scoped or globally-scoped, can be redeclared and updated.
 - let: Block-scoped, cannot be redeclared within the same scope, but can be updated.
 - const: Block-scoped, cannot be redeclared or updated.

17. What is Object.assign()?

 - Object.assign() is used to copy the values of all enumerable own properties from one or more source objects to a target object. It returns the target object.
 > const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const returnedTarget = Object.assign(target, source);
console.log(returnedTarget); // { a: 1, b: 4, c: 5 }

18. What is the difference between synchronous and asynchronous code?

 - Synchronous code: Executes sequentially, blocking further execution until the current task completes.
 - Asynchronous code: Executes without blocking further execution, allowing multiple tasks to run concurrently.

19. What is a Promise.all() method?

 - Promise.all() is a method that takes an iterable of promises and returns a single promise that resolves when all of the promises have resolved or when any of them rejects.
 > Promise.all([promise1, promise2, promise3])
.then(([result1, result2, result3]) => {
// handle results
})
.catch(error => {
// handle error
});

20. What is the difference between Object.freeze() and Object.seal()?

 - Object.freeze(): Freezes an object, preventing new properties from being added, existing properties from being removed, and existing properties from being modified.
 - Object.seal(): Seals an object, preventing new properties from being added, and existing properties from being removed, but allows existing properties to be modified.

### Difficult Questions:
1. What is the Event Loop in JavaScript?

 - The Event Loop is a mechanism that handles the execution of multiple chunks of code, including events and asynchronous operations. It allows JavaScript to perform non-blocking operations by managing the execution stack and callback queue.

2. What is the this keyword in JavaScript, and how is it determined?

The this keyword refers to the object that is executing the current function. Its value depends on how the function is called:
 - In a method, this refers to the object.
 - Alone, this refers to the global object.
 - In a function, this refers to the global object.
 - In an event, this refers to the element that received the event.
 - In strict mode, this remains undefined in a function.

3. What is the difference between function declarations and function expressions?

 - Function declarations: Defined with the function keyword, hoisted to the top of their scope.
 - Function expressions: Defined with the function keyword, assigned to a variable, and not hoisted.

4. How do you create a private variable in JavaScript?

 - Private variables can be created using closures or the Symbol type to hide variables from being accessed directly.
 > function createCounter() {
let count = 0;
return {
increment: function() { count++; },
getCount: function() { return count; }
};
}
const counter = createCounter();

5. What are generators in JavaScript, and how do you use them?

 - Generators are functions that can be paused and resumed, defined using the function* syntax. They return an iterator object with the next method.
 > function* generator() {
yield 1;
yield 2;
yield 3;
}
const gen = generator();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3

6. What is memoization in JavaScript?

 - Memoization is an optimization technique to speed up function calls by caching the results of expensive function calls and returning the cached result when the same inputs occur again.
 > function memoize(fn) {
const cache = {};
return function(...args) {
const key = JSON.stringify(args);
if (cache[key]) {
return cache[key];
} else {
const result = fn(...args);
cache[key] = result;
return result;
}
};
}

7. What are Proxies in JavaScript?

 - Proxies are used to define custom behavior for fundamental operations (e.g., property lookup, assignment, enumeration, function invocation). They are created using the Proxy constructor.
 > const handler = {
get: function(target, name) {
return name in target ? target[name] : 42;
}
};
const p = new Proxy({}, handler);
p.answerToEverything; // 42

8. What is the difference between classical inheritance and prototypal inheritance?

 - Classical inheritance: Objects inherit from classes (blueprints).
 - Prototypal inheritance: Objects inherit directly from other objects.

9. What is a WeakMap in JavaScript?

 - A WeakMap is a collection of key-value pairs where keys are weakly referenced, meaning they can be garbage-collected if there are no other references to the object. It is primarily used for associating data with objects without preventing garbage collection.
 > const wm = new WeakMap();
let obj = {};
wm.set(obj, 'value');
// 'obj' can be garbage collected when no other references exist

10. What are JavaScript Symbols?

 - Symbols are a primitive data type introduced in ES6. They are unique and immutable identifiers, often used to add unique property keys to objects that won’t collide with keys from other code.
 > const sym1 = Symbol('description');
const sym2 = Symbol('description');
console.log(sym1 === sym2); // false

11. What is a Service Worker in JavaScript?

 - A Service Worker is a script that runs in the background, separate from the web page, enabling features like push notifications and background sync. It acts as a proxy between the web app, the browser, and the network.
 > // Registering a service worker
if ('serviceWorker' in navigator) {
navigator.serviceWorker.register('/service-worker.js')
.then(registration => {
console.log('Service Worker registered with scope:', registration.scope);
})
.catch(error => {
console.log('Service Worker registration failed:', error);
});
}

12. How does async/await work in JavaScript?

 - async/await is syntactic sugar built on top of Promises. An async function returns a Promise, and await pauses the execution of the async function until the Promise is resolved.
 > async function fetchData() {
try {
const response = await fetch('https://api.example.com/data');
const data = await response.json();
return data;
} catch (error) {
console.error('Error fetching data:', error);
}
}

13. What is the difference between for...of and for...in?

 - for...of: Iterates over iterable objects (arrays, strings, maps, sets, etc.) and returns the values of the iterable.
 - for...in: Iterates over the enumerable properties of an object and returns the property names (keys).

14. What is the difference between Object.create() and new?

 - Object.create(): Creates a new object with the specified prototype object and properties.
 - new: Creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function.

15. What are tagged templates in JavaScript?

 - Tagged templates are a feature in ES6 that allows you to parse template literals with a function. The tag function can process the template before outputting the result.
 > function tag(strings, ...values) {
let str = '';
strings.forEach((string, i) => {
str += string + (values[i] || '');
});
return str;
}
const name = 'John';
const age = 30;
console.log(tag`Name: ${name}, Age: ${age}`);

16. What is the purpose of the Symbol.iterator?

 - The Symbol.iterator is a well-known symbol that specifies the default iterator for an object. It allows an object to be used with for...of loops and other iteration-based structures.
 > const myIterable = {
*[Symbol.iterator]() {
yield 1;
yield 2;
yield 3;
}
};
for (let value of myIterable) {
console.log(value); // 1, 2, 3
}

17. What is debouncing and throttling in JavaScript?

 - Debouncing: Ensures a function is only called once after a specified delay, no matter how many times the event is triggered.
 - Throttling: Ensures a function is called at most once every specified interval, regardless of how many times the event is triggered.
 > function debounce(func, wait) {
let timeout;
return function(...args) {
clearTimeout(timeout);
timeout = setTimeout(() => func.apply(this, args), wait);
};
}
function throttle(func, limit) {
let lastFunc;
let lastRan;
return function(...args) {
if (!lastRan) {
func.apply(this, args);
lastRan = Date.now();
} else {
clearTimeout(lastFunc);
lastFunc = setTimeout(function() {
if ((Date.now() - lastRan) >= limit) {
func.apply(this, args);
lastRan = Date.now();
}
}, limit - (Date.now() - lastRan));
}
};
}

18. How does prototypal inheritance work in JavaScript?

 - Prototypal inheritance in JavaScript is a style of object-oriented programming where objects inherit directly from other objects. This is achieved through the prototype chain, where an object can access properties and methods from its prototype.
 > function Person(name) {
this.name = name;
}
Person.prototype.greet = function() {
console.log('Hello, ' + this.name);
};
const john = new Person('John');
john.greet(); // Hello, John

19. What is the Temporal Dead Zone in JavaScript?

 - The Temporal Dead Zone (TDZ) is the period of time during which a variable is declared using let or const but cannot be accessed because it has not been initialized. Accessing the variable in the TDZ results in a ReferenceError.
 > console.log(x); // ReferenceError
let x = 5;

20. What are mixins in JavaScript?

 - Mixins are a way to add properties and methods from one class to another without using inheritance. This is achieved by copying properties and methods from one object to another.
 > const canEat = {
eat: function() {
console.log('Eating');
}
};
const canWalk = {
walk: function() {
console.log('Walking');
}
};
function Person(name) {
this.name = name;
}
Object.assign(Person.prototype, canEat, canWalk);
const john = new Person('John');
john.eat(); // Eating
john.walk(); // Walking
