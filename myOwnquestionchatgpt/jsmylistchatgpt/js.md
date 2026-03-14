# JavaScript Interview Questions (4+ Years) - Topic Wise

---

# 1. BASIC / FUNDAMENTALS

### Variables & Data Types

- What are the different data types in JavaScript?
- Difference between `var`, `let`, and `const`?
- What is hoisting in JavaScript?
- What is the difference between `undefined`, `null`, and `NaN`?
- What is type coercion? Examples?
- What is a primitive vs non-primitive data type?

---

# 2. FUNCTIONS & SCOPE

### Functions

- What is a higher-order function?
- Explain pure functions with example.
- What is a callback function?
- What is function expression vs function declaration?
- What are arrow functions? Differences from normal functions?
- Why arrow functions cannot be used as constructors?

### Scope

- What is lexical scope?
- What is global scope, block scope, and function scope?
- What is scope chain?

---

# 3. CLOSURES & CURRYING

- What is a closure? Real-life example?
- Why closures are used? Advantages?
- How to fix unintended closure issues in loops?
- What is currying? Example?
- Difference between partial application and currying?
- What is memoization?

---

# 4. OBJECTS & PROTOTYPES

- What is prototypal inheritance?
- What are constructor functions?
- What is the prototype chain?
- What is `__proto__` vs `prototype`?
- How does `Object.create()` work?
- How to deep clone an object?
- Difference between shallow copy vs deep copy?
- Why objects are not compared by value?

---

# 5. ASYNCHRONOUS JAVASCRIPT

### Callbacks / Promises

- What is asynchronous programming?
- What is a callback hell?
- What is a Promise? States of a Promise?
- What is promise chaining?
- `Promise.all` vs `Promise.race` vs `Promise.allSettled` vs `Promise.any`?
- What are microtasks and macrotasks?

### Async / Await

- How async/await works internally?
- Why async/await is syntactic sugar?
- Error handling in async/await?

### Event Loop

- Explain JavaScript event loop.
- What are microtasks (Promise) and macrotasks (setTimeout)?
- Event loop order questions.

---

# 6. ES6+ FEATURES

- What are template literals?
- Destructuring arrays and objects?
- Spread operator vs Rest operator?
- What are default parameters?
- Arrow functions difference?
- What are `Map`, `Set`, `WeakMap`, `WeakSet`?
- What is optional chaining?
- What is nullish coalescing `??`?
- What is the difference between `==` and `===`?

---

# 7. DOM & BROWSER CONCEPTS

- What is DOM?
- What is BOM?
- How does event bubbling and capturing work?
- What is event delegation?
- Different event types in JavaScript?
- Difference between `document.querySelector` and `getElementById`?
- What is localStorage vs sessionStorage vs cookies?
- What is same-origin policy?
- What is debouncing? Throttling?

---

# 8. ERROR HANDLING

- What is try/catch/finally?
- Custom errors in JavaScript?
- What is the call stack?
- What is stack overflow?

---

# 9. MEMORY MANAGEMENT

- What is garbage collection?
- What are memory leaks?
- Common causes of memory leaks?
- What is reference counting?

---

# 10. OBJECT ORIENTED JAVASCRIPT (OOP)

- What is class in ES6?
- What is constructor method?
- What is inheritance?
- What is encapsulation?
- What are getters and setters?
- What is static method?
- How `super()` works?

---

# 11. ADVANCED JAVASCRIPT

### Event Loop Advanced

- Explain call stack, heap, queue, microtask queue.
- What is starvation in event loop?

### Execution Context

- What is execution context?
- What happens during creation phase and execution phase?
- What is `this` keyword? Binding rules?
- `call`, `apply`, and `bind` difference?
- Arrow function `this` behavior?

### Modules

- What are ES6 modules?
- `import` vs `require`?
- What is tree shaking?

### Async Patterns

- Observables vs Promises?
- What is Web Workers?
- What is Service Workers?

---

# 12. JAVASCRIPT CODING QUESTIONS

- Reverse a string without using built-in methods.
- Implement custom `map`, `filter`, and `reduce`.
- Implement debounce and throttle functions.
- Flatten nested array.
- Deep clone an object.
- Implement custom Promise.
- Implement memoization.
- Create event emitter.
- Find unique values from array.
- Polyfill questions.

---

# 13. POLYFILLS

- Polyfill for `bind`
- Polyfill for `call`
- Polyfill for `apply`
- Polyfill for `map`
- Polyfill for `filter`
- Polyfill for `reduce`
- Polyfill for `Promise.all`

---

# 14. MOSTLY ASKED PRACTICAL QUESTIONS

- How to optimize a JavaScript application?
- How to improve performance in React / frontend?
- Why is immutability important?
- How to avoid memory leaks?
- Why promises are better than callbacks?

---

# Detailed Answers For 4+ Years Interview

## 1. Basic / Fundamentals

### 1. What are the different data types in JavaScript?
Definition: JavaScript has primitive and non-primitive data types.
Why it matters: Interviewers expect you to know how values behave in memory and comparisons.
Exact answer: Primitive types are `string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, and `null`. Non-primitive types are objects, arrays, and functions.
Example:

```js
const name = "Aslam";
const age = 30;
const isActive = true;
const user = { name: "Aslam" };
```

### 2. Difference between `var`, `let`, and `const`?
Definition: These are variable declaration keywords with different scope and reassignment rules.
Why it matters: It affects hoisting, scope bugs, and immutability.
Exact answer: `var` is function-scoped and can be redeclared. `let` is block-scoped and can be reassigned. `const` is block-scoped and cannot be reassigned.
Example:

```js
var a = 1;
let b = 2;
const c = 3;
```

### 3. What is hoisting in JavaScript?
Definition: Hoisting means declarations are processed before code execution.
Why it matters: It explains why some variables/functions can be used before declaration.
Exact answer: Function declarations are fully hoisted. `var` is hoisted and initialized with `undefined`. `let` and `const` are hoisted but stay in the temporal dead zone.
Example:

```js
console.log(x); // undefined
var x = 10;
```

### 4. What is the difference between `undefined`, `null`, and `NaN`?
Definition: These represent three different kinds of "missing or invalid" values.
Why it matters: Many bugs come from mixing them.
Exact answer: `undefined` means a variable is declared but not assigned. `null` is an intentional empty value. `NaN` means "Not a Number", usually from invalid math operations.
Example:

```js
let a;
let b = null;
let c = Number("abc");
```

### 5. What is type coercion? Examples?
Definition: Type coercion is automatic or explicit conversion from one type to another.
Why it matters: JavaScript often converts values implicitly, which can lead to tricky bugs.
Exact answer: JavaScript may convert values automatically in comparisons or expressions. Example: `"5" + 1` becomes `"51"`, while `"5" - 1` becomes `4`.
Example:

```js
console.log("5" + 1); // "51"
console.log("5" - 1); // 4
```

### 6. What is a primitive vs non-primitive data type?
Definition: Primitive values are immutable and stored by value; non-primitives are stored by reference.
Why it matters: It explains copying and comparison behavior.
Exact answer: Primitive values like numbers and strings are copied directly. Objects and arrays are copied as references, so changes can affect the original.
Example:

```js
let a = 10;
let b = a;
b = 20;

const obj1 = { name: "A" };
const obj2 = obj1;
obj2.name = "B";
```

## 2. Functions & Scope

### 1. What is a higher-order function?
Definition: A higher-order function takes another function as an argument or returns a function.
Why it matters: It is used heavily in modern JavaScript like `map`, `filter`, and event handling.
Exact answer: Higher-order functions make code reusable and functional.
Example:

```js
function greet(fn) {
  fn();
}

greet(() => console.log("Hello"));
```

### 2. Explain pure functions with example.
Definition: A pure function always returns the same output for the same input and has no side effects.
Why it matters: Pure functions are easier to test and debug.
Exact answer: They do not modify external state and are predictable.
Example:

```js
function add(a, b) {
  return a + b;
}
```

### 3. What is a callback function?
Definition: A callback is a function passed into another function to be executed later.
Why it matters: It is the foundation of async JavaScript and event handling.
Exact answer: Callbacks are used in timers, array methods, and event listeners.
Example:

```js
setTimeout(() => {
  console.log("Done");
}, 1000);
```

### 4. What is function expression vs function declaration?
Definition: A function declaration defines a named function directly, while a function expression stores a function in a variable.
Why it matters: Hoisting behavior is different.
Exact answer: Function declarations are fully hoisted. Function expressions behave like normal variable assignments.
Example:

```js
function sayHi() {
  return "Hi";
}

const sayBye = function () {
  return "Bye";
};
```

### 5. What are arrow functions? Differences from normal functions?
Definition: Arrow functions are a shorter syntax for writing functions.
Why it matters: They behave differently with `this`, `arguments`, and constructors.
Exact answer: Arrow functions do not have their own `this`, `arguments`, or `prototype`. They capture `this` from the outer scope.
Example:

```js
const add = (a, b) => a + b;
```

### 6. Why arrow functions cannot be used as constructors?
Definition: Constructors need their own `this` and `prototype`.
Why it matters: It explains a common interview trick question.
Exact answer: Arrow functions do not have a `prototype` and cannot be called with `new`.
Example:

```js
const Person = () => {};
// new Person(); // TypeError
```

### 7. What is lexical scope?
Definition: Lexical scope means inner functions can access variables from outer functions where they are defined.
Why it matters: It is the basis of closures.
Exact answer: Scope is decided by where code is written, not where it is called.
Example:

```js
function outer() {
  const name = "Aslam";
  function inner() {
    console.log(name);
  }
  inner();
}
```

### 8. What is global scope, block scope, and function scope?
Definition: These define where variables are accessible.
Why it matters: Scope mistakes often cause bugs in large apps.
Exact answer: Global scope is available everywhere. Function scope is inside a function. Block scope is inside `{}` and works with `let` and `const`.
Example:

```js
var a = 1;
if (true) {
  let b = 2;
}
function test() {
  var c = 3;
}
```

### 9. What is scope chain?
Definition: Scope chain is how JavaScript looks for variables from inner to outer scope.
Why it matters: It explains variable lookup behavior.
Exact answer: If a variable is not found locally, JavaScript checks outer scopes until global scope.
Example:

```js
const a = 1;
function outer() {
  const b = 2;
  function inner() {
    console.log(a, b);
  }
  inner();
}
```

## 3. Closures & Currying

### 1. What is a closure? Real-life example?
Definition: A closure is when a function remembers variables from its outer scope even after the outer function is done.
Why it matters: It is used in data privacy, callbacks, and reusable logic.
Exact answer: Closures happen because functions keep access to their lexical environment.
Example:

```js
function createCounter() {
  let count = 0;
  return function () {
    return ++count;
  };
}
```

### 2. Why closures are used? Advantages?
Definition: Closures help preserve state without exposing it globally.
Why it matters: They improve encapsulation and modular code.
Exact answer: They are used for private variables, memoization, event handlers, and function factories.
Example:

```js
function secret() {
  const password = "1234";
  return () => password;
}
```

### 3. How to fix unintended closure issues in loops?
Definition: Old loop code with `var` can capture the same variable reference.
Why it matters: This is a classic interview problem.
Exact answer: Use `let` or create a new scope with an IIFE.
Example:

```js
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```

### 4. What is currying? Example?
Definition: Currying transforms a function with multiple arguments into nested functions with one argument each.
Why it matters: It improves reuse and function composition.
Exact answer: Instead of `sum(a, b, c)`, curried form is `sum(a)(b)(c)`.
Example:

```js
const sum = (a) => (b) => (c) => a + b + c;
console.log(sum(1)(2)(3));
```

### 5. Difference between partial application and currying?
Definition: Both reduce the number of required arguments, but they work differently.
Why it matters: Advanced interviewers ask this to test function concepts.
Exact answer: Currying always breaks into one argument per function. Partial application can preset some arguments while accepting the rest together.
Example:

```js
function multiply(a, b, c) {
  return a * b * c;
}

const partial = multiply.bind(null, 2);
console.log(partial(3, 4));
```

### 6. What is memoization?
Definition: Memoization stores results of expensive function calls and reuses them for the same input.
Why it matters: It improves performance.
Exact answer: It is commonly used in calculations and React optimizations.
Example:

```js
function memoize(fn) {
  const cache = {};
  return function (n) {
    if (cache[n]) return cache[n];
    cache[n] = fn(n);
    return cache[n];
  };
}
```

## 4. Objects & Prototypes

### 1. What is prototypal inheritance?
Definition: Objects can inherit properties and methods from another object through the prototype chain.
Why it matters: JavaScript inheritance is prototype-based, not class-based internally.
Exact answer: When a property is not found on an object, JavaScript looks up its prototype.
Example:

```js
const animal = { eat() { console.log("eat"); } };
const dog = Object.create(animal);
dog.eat();
```

### 2. What are constructor functions?
Definition: Constructor functions are regular functions used with `new` to create objects.
Why it matters: They were the pre-ES6 way to simulate classes.
Exact answer: They initialize object properties using `this`.
Example:

```js
function Person(name) {
  this.name = name;
}
const p1 = new Person("Aslam");
```

### 3. What is the prototype chain?
Definition: The prototype chain is the linked sequence of objects JavaScript checks for properties.
Why it matters: It explains inheritance and method lookup.
Exact answer: Lookup continues until `null` is reached.
Example:

```js
console.log([].__proto__);
```

### 4. What is `__proto__` vs `prototype`?
Definition: `prototype` belongs to functions; `__proto__` points to an object's internal prototype.
Why it matters: Interviewers ask this to test deep object knowledge.
Exact answer: `prototype` is used when creating instances with `new`; `__proto__` is the actual link on objects.
Example:

```js
function User() {}
const u = new User();
console.log(User.prototype === u.__proto__);
```

### 5. How does `Object.create()` work?
Definition: It creates a new object with a given prototype.
Why it matters: It is a direct way to set up inheritance.
Exact answer: The created object delegates property lookup to the provided prototype.
Example:

```js
const parent = { role: "admin" };
const child = Object.create(parent);
console.log(child.role);
```

### 6. How to deep clone an object?
Definition: Deep clone creates a fully independent copy of nested data.
Why it matters: Needed for immutability and safe state updates.
Exact answer: Use `structuredClone()` in modern JS or custom recursion for special cases.
Example:

```js
const obj = { a: 1, b: { c: 2 } };
const copy = structuredClone(obj);
```

### 7. Difference between shallow copy vs deep copy?
Definition: Shallow copy copies only first-level properties; deep copy copies nested structures too.
Why it matters: Prevents accidental mutations.
Exact answer: Spread syntax makes shallow copies, while `structuredClone` makes deep copies.
Example:

```js
const obj = { x: { y: 1 } };
const shallow = { ...obj };
const deep = structuredClone(obj);
```

### 8. Why objects are not compared by value?
Definition: Objects are reference types, so comparison checks memory reference.
Why it matters: It explains why two similar objects are not equal.
Exact answer: `{}` === `{}` is false because they are different references.
Example:

```js
console.log({ a: 1 } === { a: 1 }); // false
```

## 5. Asynchronous JavaScript

### 1. What is asynchronous programming?
Definition: Async programming allows tasks to run without blocking the main thread.
Why it matters: It keeps UI responsive during network or delayed operations.
Exact answer: JavaScript delegates async work to browser/Web APIs and handles results later.
Example:

```js
setTimeout(() => console.log("Async"), 1000);
```

### 2. What is callback hell?
Definition: Callback hell is deeply nested callbacks that are hard to read and maintain.
Why it matters: It led to Promises and async/await.
Exact answer: It happens when async flows depend on previous results.
Example:

```js
step1(() => {
  step2(() => {
    step3(() => {});
  });
});
```

### 3. What is a Promise? States of a Promise?
Definition: A Promise represents a future value from an async operation.
Why it matters: It is the core async abstraction in modern JavaScript.
Exact answer: A Promise has `pending`, `fulfilled`, and `rejected` states.
Example:

```js
const promise = new Promise((resolve) => resolve("done"));
promise.then(console.log);
```

### 4. What is promise chaining?
Definition: Promise chaining connects multiple `.then()` calls in sequence.
Why it matters: It helps avoid callback hell.
Exact answer: Each `.then()` returns a new promise.
Example:

```js
Promise.resolve(2)
  .then((n) => n * 2)
  .then((n) => console.log(n));
```

### 5. `Promise.all` vs `Promise.race` vs `Promise.allSettled` vs `Promise.any`?
Definition: These are Promise combinators with different behaviors.
Why it matters: Choosing the wrong one changes app behavior.
Exact answer:
- `Promise.all`: waits for all, rejects if one fails
- `Promise.race`: returns first settled promise
- `Promise.allSettled`: waits for all, returns status of each
- `Promise.any`: resolves with first fulfilled promise
Example:

```js
Promise.all([Promise.resolve(1), Promise.resolve(2)]).then(console.log);
```

### 6. What are microtasks and macrotasks?
Definition: Microtasks have higher priority than macrotasks in the event loop.
Why it matters: It explains execution order questions.
Exact answer: Promise callbacks are microtasks. `setTimeout` callbacks are macrotasks.
Example:

```js
setTimeout(() => console.log("timeout"), 0);
Promise.resolve().then(() => console.log("promise"));
```

### 7. How async/await works internally?
Definition: `async/await` is built on top of Promises.
Why it matters: Senior interviewers ask what happens under the hood.
Exact answer: `async` returns a Promise, and `await` pauses execution inside that async function until the promise settles.
Example:

```js
async function run() {
  const value = await Promise.resolve(10);
  console.log(value);
}
```

### 8. Why async/await is syntactic sugar?
Definition: It is a cleaner syntax over Promises, not a new async model.
Why it matters: It shows conceptual clarity.
Exact answer: The same async behavior still depends on promises and the event loop.
Example:

```js
async function getData() {
  return await Promise.resolve("data");
}
```

### 9. Error handling in async/await?
Definition: Errors can be handled with `try/catch`.
Why it matters: Production apps need robust async error handling.
Exact answer: Awaited promise rejections are caught by `catch` blocks.
Example:

```js
async function fetchData() {
  try {
    await Promise.reject("error");
  } catch (err) {
    console.log(err);
  }
}
```

### 10. Explain JavaScript event loop.
Definition: The event loop coordinates the call stack, task queues, and async callbacks.
Why it matters: It is one of the most asked JavaScript interview topics.
Exact answer: Synchronous code runs first, then microtasks, then macrotasks.
Example:

```js
console.log("start");
setTimeout(() => console.log("timeout"), 0);
Promise.resolve().then(() => console.log("promise"));
console.log("end");
```

### 11. What are microtasks and macrotasks? Event loop order questions.
Definition: Microtasks run before the next macrotask.
Why it matters: It decides actual output order.
Exact answer: Order is synchronous code -> microtasks -> macrotasks.
Example:

```js
console.log(1);
setTimeout(() => console.log(2), 0);
Promise.resolve().then(() => console.log(3));
console.log(4);
```

## 6. ES6+ Features

### 1. What are template literals?
Definition: Template literals are strings written with backticks.
Why it matters: They simplify interpolation and multiline strings.
Exact answer: Use `${}` to embed expressions.
Example:

```js
const name = "Aslam";
console.log(`Hello ${name}`);
```

### 2. Destructuring arrays and objects?
Definition: Destructuring extracts values into variables.
Why it matters: It makes code shorter and clearer.
Exact answer: It works on arrays and objects.
Example:

```js
const [a, b] = [1, 2];
const { name } = { name: "Aslam" };
```

### 3. Spread operator vs Rest operator?
Definition: Spread expands values; rest collects values.
Why it matters: Used heavily in React state and function args.
Exact answer: Same syntax `...`, different use based on position.
Example:

```js
const arr = [1, 2];
const newArr = [...arr, 3];

function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
```

### 4. What are default parameters?
Definition: Default parameters provide fallback values when no argument is passed.
Why it matters: They reduce defensive code.
Exact answer: Used directly in function parameters.
Example:

```js
function greet(name = "Guest") {
  return `Hello ${name}`;
}
```

### 5. Arrow functions difference?
Definition: Arrow functions are shorter and lexically bind `this`.
Why it matters: Interviewers expect the `this` difference.
Exact answer: They do not have their own `this`, `arguments`, or constructor behavior.
Example:

```js
const square = (n) => n * n;
```

### 6. What are `Map`, `Set`, `WeakMap`, `WeakSet`?
Definition: These are specialized collections.
Why it matters: They solve problems that plain objects/arrays do not.
Exact answer:
- `Map`: key-value pairs with any key type
- `Set`: unique values
- `WeakMap`: object keys only, weakly held
- `WeakSet`: object values only, weakly held
Example:

```js
const map = new Map();
map.set("name", "Aslam");

const set = new Set([1, 2, 2, 3]);
```

### 7. What is optional chaining?
Definition: Optional chaining safely accesses nested values.
Why it matters: Prevents errors on `undefined` or `null`.
Exact answer: If a value is missing, it returns `undefined` instead of throwing.
Example:

```js
const user = {};
console.log(user.address?.city);
```

### 8. What is nullish coalescing `??`?
Definition: `??` returns the right value only when the left side is `null` or `undefined`.
Why it matters: It avoids incorrect fallback for `0` or `""`.
Exact answer: It is better than `||` when valid falsy values exist.
Example:

```js
console.log(0 ?? 10); // 0
console.log(null ?? 10); // 10
```

### 9. What is the difference between `==` and `===`?
Definition: `==` does loose comparison, `===` does strict comparison.
Why it matters: Strict equality avoids coercion bugs.
Exact answer: Prefer `===` in real projects.
Example:

```js
console.log(5 == "5"); // true
console.log(5 === "5"); // false
```

## 7. DOM & Browser Concepts

### 1. What is DOM?
Definition: DOM is the browser's tree representation of HTML.
Why it matters: JavaScript uses it to read and update UI.
Exact answer: Every HTML element becomes a node in the DOM tree.
Example:

```js
document.getElementById("title").textContent = "Hello";
```

### 2. What is BOM?
Definition: BOM stands for Browser Object Model.
Why it matters: It gives access to browser-related objects.
Exact answer: It includes `window`, `location`, `history`, `navigator`, etc.
Example:

```js
console.log(window.location.href);
```

### 3. How does event bubbling and capturing work?
Definition: Events travel through the DOM in capturing and bubbling phases.
Why it matters: Important for event handling and debugging.
Exact answer: Capturing goes top to bottom, target phase hits the element, bubbling goes bottom to top.
Example:

```js
parent.addEventListener("click", () => console.log("parent"));
child.addEventListener("click", () => console.log("child"));
```

### 4. What is event delegation?
Definition: Event delegation attaches one listener to a parent instead of many children.
Why it matters: Better performance and works with dynamic elements.
Exact answer: It relies on event bubbling and `event.target`.
Example:

```js
list.addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    console.log(e.target.textContent);
  }
});
```

### 5. Different event types in JavaScript?
Definition: Events are actions triggered by user or browser.
Why it matters: You should know common UI interactions.
Exact answer: Common events include `click`, `input`, `change`, `submit`, `keydown`, `mouseover`, `scroll`, and `load`.
Example:

```js
input.addEventListener("input", () => console.log("typing"));
```

### 6. Difference between `document.querySelector` and `getElementById`?
Definition: Both select DOM elements, but their usage is different.
Why it matters: It affects flexibility and readability.
Exact answer: `getElementById` selects by id only and is very direct. `querySelector` uses CSS selectors and returns the first match.
Example:

```js
document.getElementById("box");
document.querySelector(".box");
```

### 7. What is localStorage vs sessionStorage vs cookies?
Definition: These are browser storage mechanisms.
Why it matters: Used in auth, preferences, and state persistence.
Exact answer:
- `localStorage`: persists until cleared
- `sessionStorage`: persists per tab session
- cookies: small data sent with HTTP requests
Example:

```js
localStorage.setItem("theme", "dark");
sessionStorage.setItem("step", "1");
document.cookie = "token=abc";
```

### 8. What is same-origin policy?
Definition: Browsers restrict resource access across different origins.
Why it matters: It protects users from malicious cross-site actions.
Exact answer: Origin includes protocol, domain, and port. If any differ, it is cross-origin.
Example:

```js
fetch("https://api.example.com/data");
```

### 9. What is debouncing? Throttling?
Definition: Debounce delays repeated calls; throttle limits call frequency.
Why it matters: Used for performance optimization.
Exact answer: Debounce is ideal for search input. Throttle is ideal for scroll/resize.
Example:

```js
function debounce(fn, delay) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

## 8. Error Handling

### 1. What is try/catch/finally?
Definition: It is the main error handling structure in JavaScript.
Why it matters: It prevents crashes and supports graceful recovery.
Exact answer: `try` runs risky code, `catch` handles errors, `finally` always runs.
Example:

```js
try {
  JSON.parse("{");
} catch (err) {
  console.log("Invalid JSON");
} finally {
  console.log("done");
}
```

### 2. Custom errors in JavaScript?
Definition: Custom errors are user-defined error classes or objects.
Why it matters: They make error handling more meaningful.
Exact answer: Extend `Error` for reusable error types.
Example:

```js
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}
```

### 3. What is the call stack?
Definition: The call stack tracks currently executing function calls.
Why it matters: It is central to execution context and debugging.
Exact answer: Functions are pushed when called and popped when finished.
Example:

```js
function one() { two(); }
function two() { console.log("stack"); }
one();
```

### 4. What is stack overflow?
Definition: Stack overflow happens when the call stack grows beyond its limit.
Why it matters: Usually caused by uncontrolled recursion.
Exact answer: The browser or runtime throws an error like `Maximum call stack size exceeded`.
Example:

```js
function loop() {
  loop();
}
```

## 9. Memory Management

### 1. What is garbage collection?
Definition: Garbage collection automatically removes unreachable memory.
Why it matters: It helps manage memory without manual free operations.
Exact answer: JavaScript engines usually use mark-and-sweep algorithms.
Example:

```js
let user = { name: "A" };
user = null;
```

### 2. What are memory leaks?
Definition: Memory leaks happen when memory is no longer needed but still referenced.
Why it matters: It can slow down apps and crash long-running pages.
Exact answer: Common causes include timers, listeners, closures, and retained DOM references.
Example:

```js
const arr = [];
setInterval(() => arr.push(new Array(1000).fill("*")), 1000);
```

### 3. Common causes of memory leaks?
Definition: These are patterns that keep unused objects alive.
Why it matters: Interviewers want practical production awareness.
Exact answer: Unremoved event listeners, uncleared timers, detached DOM nodes, accidental globals, and big caches.
Example:

```js
window.addEventListener("resize", () => console.log("resize"));
```

### 4. What is reference counting?
Definition: Reference counting is a memory strategy based on tracking how many references point to an object.
Why it matters: It helps explain older GC concepts and cyclic reference issues.
Exact answer: Modern JS engines mainly use mark-and-sweep, but reference counting is still a useful concept.
Example:

```js
let obj = {};
let ref = obj;
obj = null;
```

## 10. OOP in JavaScript

### 1. What is class in ES6?
Definition: ES6 class is syntactic sugar over prototypes.
Why it matters: It provides cleaner OOP syntax.
Exact answer: Classes support constructors, inheritance, methods, and `super`.
Example:

```js
class User {
  constructor(name) {
    this.name = name;
  }
}
```

### 2. What is constructor method?
Definition: `constructor` initializes an object when a class instance is created.
Why it matters: It sets up initial state.
Exact answer: It runs automatically with `new`.
Example:

```js
class Person {
  constructor(name) {
    this.name = name;
  }
}
```

### 3. What is inheritance?
Definition: Inheritance allows one class/object to reuse properties and methods of another.
Why it matters: It promotes reuse.
Exact answer: In ES6 classes, use `extends`.
Example:

```js
class Animal {
  speak() {
    console.log("sound");
  }
}

class Dog extends Animal {}
```

### 4. What is encapsulation?
Definition: Encapsulation means hiding internal details and exposing only what is needed.
Why it matters: It protects data and reduces coupling.
Exact answer: Modern JS supports private fields with `#`.
Example:

```js
class Account {
  #balance = 100;
  getBalance() {
    return this.#balance;
  }
}
```

### 5. What are getters and setters?
Definition: Getters and setters control property access.
Why it matters: Useful for validation and computed values.
Exact answer: `get` reads like a property, `set` validates/updates it.
Example:

```js
class User {
  set name(value) {
    this._name = value.trim();
  }
  get name() {
    return this._name;
  }
}
```

### 6. What is static method?
Definition: A static method belongs to the class, not the instance.
Why it matters: Useful for utility methods.
Exact answer: Call it on the class name directly.
Example:

```js
class MathUtil {
  static add(a, b) {
    return a + b;
  }
}
```

### 7. How `super()` works?
Definition: `super()` calls the parent class constructor or methods.
Why it matters: Required when extending classes with constructors.
Exact answer: In child constructors, `super()` must be called before using `this`.
Example:

```js
class Animal {
  constructor(name) {
    this.name = name;
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name);
  }
}
```

## 11. Advanced JavaScript

### 1. Explain call stack, heap, queue, microtask queue.
Definition: These are core runtime concepts.
Why it matters: Senior interviews focus on how JavaScript runs internally.
Exact answer:
- Call stack: runs functions
- Heap: stores objects
- Callback queue: macrotasks
- Microtask queue: promises and high-priority async tasks
Example:

```js
console.log("stack");
Promise.resolve().then(() => console.log("microtask"));
setTimeout(() => console.log("queue"), 0);
```

### 2. What is starvation in event loop?
Definition: Starvation happens when lower-priority tasks keep waiting because higher-priority tasks keep coming.
Why it matters: It can delay UI or timers unexpectedly.
Exact answer: Too many microtasks can delay macrotasks like `setTimeout`.
Example:

```js
function repeat() {
  Promise.resolve().then(repeat);
}
// repeat();
```

### 3. What is execution context?
Definition: Execution context is the environment in which JS code runs.
Why it matters: It defines variables, `this`, and scope.
Exact answer: There are global execution context and function execution contexts.
Example:

```js
function test() {
  const a = 1;
}
```

### 4. What happens during creation phase and execution phase?
Definition: JavaScript execution has setup and run phases.
Why it matters: This explains hoisting and scope preparation.
Exact answer: In creation phase, memory is allocated and bindings are set up. In execution phase, code runs line by line.
Example:

```js
console.log(a);
var a = 5;
```

### 5. What is `this` keyword? Binding rules?
Definition: `this` depends on how a function is invoked.
Why it matters: It is one of the most common JS interview topics.
Exact answer:
- Global/default binding
- Implicit binding via object
- Explicit binding via `call/apply/bind`
- `new` binding
- Lexical binding in arrow functions
Example:

```js
const obj = {
  name: "Aslam",
  show() {
    console.log(this.name);
  }
};
```

### 6. `call`, `apply`, and `bind` difference?
Definition: These explicitly set `this`.
Why it matters: Needed for method borrowing and callbacks.
Exact answer: `call` passes args individually, `apply` as array, `bind` returns a new function.
Example:

```js
function greet(city) {
  console.log(this.name, city);
}
```

### 7. Arrow function `this` behavior?
Definition: Arrow functions use lexical `this`.
Why it matters: Great for callbacks, wrong for methods/constructors.
Exact answer: They do not create their own `this`.
Example:

```js
const obj = {
  name: "A",
  show: () => console.log(this.name)
};
```

### 8. What are ES6 modules?
Definition: ES6 modules split code into reusable files using `export` and `import`.
Why it matters: They support maintainable codebases and tree shaking.
Exact answer: Modules are loaded once and have their own scope.
Example:

```js
export const sum = (a, b) => a + b;
import { sum } from "./math.js";
```

### 9. `import` vs `require`?
Definition: `import` belongs to ES modules; `require` belongs to CommonJS.
Why it matters: You need to know module systems in frontend and Node.
Exact answer: `import` is static and supports tree shaking. `require` is dynamic and runtime-based.
Example:

```js
import fs from "fs";
const path = require("path");
```

### 10. What is tree shaking?
Definition: Tree shaking removes unused code from final bundles.
Why it matters: It reduces bundle size.
Exact answer: Works best with ES modules because imports are statically analyzable.
Example:

```js
import { usedFn } from "./utils.js";
```

### 11. Observables vs Promises?
Definition: Promises handle one future value; Observables can emit multiple values over time.
Why it matters: Asked in frontend architecture interviews.
Exact answer: Observables are cancelable and lazy; Promises are eager and single-value.
Example:

```js
Promise.resolve("one").then(console.log);
```

### 12. What is Web Workers?
Definition: Web Workers run JavaScript in a background thread.
Why it matters: They prevent blocking the main UI thread.
Exact answer: Used for heavy calculations, not direct DOM access.
Example:

```js
const worker = new Worker("worker.js");
worker.postMessage("start");
```

### 13. What is Service Workers?
Definition: Service Workers run in the background and intercept network requests.
Why it matters: Used for caching, offline support, and PWA features.
Exact answer: They sit between app and network.
Example:

```js
navigator.serviceWorker.register("/sw.js");
```

## 12. JavaScript Coding Questions

### 1. Reverse a string without using built-in methods.
Definition: Reverse manually using loop logic.
Why it matters: Tests basic algorithm skills.
Example:

```js
function reverseString(str) {
  let result = "";
  for (let i = str.length - 1; i >= 0; i--) {
    result += str[i];
  }
  return result;
}
```

### 2. Implement custom `map`, `filter`, and `reduce`.
Definition: Recreate built-in array methods.
Why it matters: Tests array iteration and functional thinking.
Example:

```js
Array.prototype.myMap = function (cb) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    result.push(cb(this[i], i, this));
  }
  return result;
};

Array.prototype.myFilter = function (cb) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    if (cb(this[i], i, this)) result.push(this[i]);
  }
  return result;
};

Array.prototype.myReduce = function (cb, acc) {
  let result = acc;
  let start = 0;
  if (result === undefined) {
    result = this[0];
    start = 1;
  }
  for (let i = start; i < this.length; i++) {
    result = cb(result, this[i], i, this);
  }
  return result;
};
```

### 3. Implement debounce and throttle functions.
Definition: Utility functions to control frequent execution.
Why it matters: Common practical frontend interview problem.
Example:

```js
function debounce(fn, delay) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}

function throttle(fn, delay) {
  let last = 0;
  return (...args) => {
    const now = Date.now();
    if (now - last >= delay) {
      last = now;
      fn(...args);
    }
  };
}
```

### 4. Flatten nested array.
Definition: Convert nested arrays into a single-level array.
Why it matters: Tests recursion.
Example:

```js
function flatten(arr) {
  let result = [];
  for (const item of arr) {
    if (Array.isArray(item)) {
      result = result.concat(flatten(item));
    } else {
      result.push(item);
    }
  }
  return result;
}
```

### 5. Deep clone an object.
Definition: Create a nested independent copy.
Why it matters: Important in state handling.
Example:

```js
const clone = (obj) => structuredClone(obj);
```

### 6. Implement custom Promise.
Definition: Basic idea is to store callbacks and resolve later.
Why it matters: Tests async design understanding.
Example:

```js
class MyPromise {
  constructor(executor) {
    this.callbacks = [];
    this.value = undefined;
    this.resolved = false;

    const resolve = (value) => {
      this.resolved = true;
      this.value = value;
      this.callbacks.forEach((cb) => cb(value));
    };

    executor(resolve);
  }

  then(cb) {
    if (this.resolved) cb(this.value);
    else this.callbacks.push(cb);
  }
}
```

### 7. Implement memoization.
Definition: Cache function results.
Why it matters: Performance interview question.
Example:

```js
function memoize(fn) {
  const cache = {};
  return function (n) {
    if (cache[n] !== undefined) return cache[n];
    cache[n] = fn(n);
    return cache[n];
  };
}
```

### 8. Create event emitter.
Definition: A pub-sub utility for events.
Why it matters: Tests architecture thinking.
Example:

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(type, cb) {
    (this.events[type] ||= []).push(cb);
  }

  emit(type, data) {
    (this.events[type] || []).forEach((cb) => cb(data));
  }
}
```

### 9. Find unique values from array.
Definition: Remove duplicates.
Why it matters: Very common coding question.
Example:

```js
const unique = [...new Set([1, 2, 2, 3])];
```

### 10. Polyfill questions.
Definition: Polyfills recreate missing native methods.
Why it matters: Common for 4+ years JS interviews.
Exact answer: The key is using `this`, iteration, and callback behavior correctly.

## 13. Polyfills

### 1. Polyfill for `bind`

```js
Function.prototype.myBind = function (context, ...args1) {
  const fn = this;
  return function (...args2) {
    return fn.apply(context, [...args1, ...args2]);
  };
};
```

### 2. Polyfill for `call`

```js
Function.prototype.myCall = function (context, ...args) {
  context = context || globalThis;
  const key = Symbol();
  context[key] = this;
  const result = context[key](...args);
  delete context[key];
  return result;
};
```

### 3. Polyfill for `apply`

```js
Function.prototype.myApply = function (context, args = []) {
  context = context || globalThis;
  const key = Symbol();
  context[key] = this;
  const result = context[key](...args);
  delete context[key];
  return result;
};
```

### 4. Polyfill for `map`

```js
Array.prototype.myMap = function (cb) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    result.push(cb(this[i], i, this));
  }
  return result;
};
```

### 5. Polyfill for `filter`

```js
Array.prototype.myFilter = function (cb) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    if (cb(this[i], i, this)) result.push(this[i]);
  }
  return result;
};
```

### 6. Polyfill for `reduce`

```js
Array.prototype.myReduce = function (cb, initial) {
  let acc = initial;
  let start = 0;

  if (acc === undefined) {
    acc = this[0];
    start = 1;
  }

  for (let i = start; i < this.length; i++) {
    acc = cb(acc, this[i], i, this);
  }

  return acc;
};
```

### 7. Polyfill for `Promise.all`

```js
function myPromiseAll(promises) {
  return new Promise((resolve, reject) => {
    const result = [];
    let count = 0;

    promises.forEach((promise, index) => {
      Promise.resolve(promise)
        .then((value) => {
          result[index] = value;
          count++;
          if (count === promises.length) resolve(result);
        })
        .catch(reject);
    });
  });
}
```

## 14. Mostly Asked Practical Questions

### 1. How to optimize a JavaScript application?
Definition: Improve speed, bundle size, and runtime efficiency.
Why it matters: This is a real senior-level frontend question.
Exact answer: Use lazy loading, memoization, code splitting, debouncing, throttling, caching, smaller bundles, and efficient DOM updates.
Example:

```js
const expensiveResult = memoize((n) => n * n);
```

### 2. How to improve performance in React / frontend?
Definition: Reduce unnecessary renders and expensive work.
Why it matters: Common 4+ years practical interview topic.
Exact answer: Use `React.memo`, `useMemo`, `useCallback`, code splitting, virtualization, and proper key usage.
Example:

```js
const memoizedValue = useMemo(() => compute(data), [data]);
```

### 3. Why is immutability important?
Definition: Immutability means not changing existing data directly.
Why it matters: It enables predictable updates and easier debugging.
Exact answer: It is especially important in React and Redux because change detection often relies on reference changes.
Example:

```js
const newState = { ...state, count: state.count + 1 };
```

### 4. How to avoid memory leaks?
Definition: Release references that are no longer needed.
Why it matters: Long-running apps can slow down badly otherwise.
Exact answer: Clear timers, remove listeners, cancel subscriptions, and avoid retaining large unused data.
Example:

```js
useEffect(() => {
  const id = setInterval(() => {}, 1000);
  return () => clearInterval(id);
}, []);
```

### 5. Why promises are better than callbacks?
Definition: Promises structure async logic better than nested callbacks.
Why it matters: Cleaner, more maintainable async code is expected at 4+ years level.
Exact answer: Promises support chaining, central error handling, and combinators like `Promise.all`.
Example:

```js
fetch("/api/users")
  .then((res) => res.json())
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```
