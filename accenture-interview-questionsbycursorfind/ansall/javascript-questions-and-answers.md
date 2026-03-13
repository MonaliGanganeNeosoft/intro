# JavaScript Interview Questions and Answers

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

This file gives:

1. Definition
2. Why it is used
3. Short answer for interview
4. Coding example where useful

## Theory Questions and Answers

### 1. What is the difference between `var`, `let`, and `const`?

Definition:
`var` is function-scoped and can be redeclared. `let` and `const` are block-scoped. `const` cannot be reassigned after initialization.

Why used:
`let` is used when values need to change. `const` is preferred by default because it prevents accidental reassignment.

Interview answer:
Use `const` by default, `let` when reassignment is needed, and avoid `var` in modern code because of hoisting confusion and function scope.

Example:

```js
function demo() {
  if (true) {
    var a = 10;
    let b = 20;
    const c = 30;
  }

  console.log(a); // 10
  // console.log(b); // ReferenceError
  // console.log(c); // ReferenceError
}
```

### 2. What is hoisting in JavaScript?

Definition:
Hoisting means declarations are moved to the top of their scope during compilation.

Why used:
It is part of how JavaScript parses code before execution.

Interview answer:
Function declarations are fully hoisted. `var` is hoisted with `undefined`. `let` and `const` are hoisted too, but stay in the temporal dead zone until initialized.

Example:

```js
console.log(x); // undefined
var x = 5;

sayHi(); // works
function sayHi() {
  console.log("Hi");
}
```

### 3. What is the temporal dead zone?

Definition:
It is the time between entering a scope and initializing a `let` or `const` variable.

Why used:
It prevents accessing variables before proper initialization.

Interview answer:
Variables declared with `let` and `const` are hoisted but cannot be used before the declaration line.

Example:

```js
// console.log(a); // ReferenceError
let a = 10;
```

### 4. What is lexical scope?

Definition:
Lexical scope means a function can access variables from the scope where it was created.

Why used:
It allows nested functions and closures to work predictably.

Interview answer:
Scope in JavaScript is determined by where code is written, not where it is called.

Example:

```js
const outer = "global";

function parent() {
  const inner = "local";

  function child() {
    console.log(outer, inner);
  }

  child();
}
```

### 5. What are closures, and where do you use them in real applications?

Definition:
A closure is a function that remembers variables from its outer scope even after the outer function has finished.

Why used:
Closures are used for private state, callbacks, event handlers, memoization, and factory functions.

Interview answer:
Closures help preserve data across function calls without exposing it globally.

Example:

```js
function createCounter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

### 6. What is the difference between function declarations, function expressions, and arrow functions?

Definition:
Function declarations are named and hoisted. Function expressions are assigned to variables. Arrow functions are shorter and do not have their own `this`.

Why used:
Arrow functions are common in callbacks. Function declarations are useful for reusable named logic.

Interview answer:
The main differences are hoisting, syntax, and `this` binding behavior.

Example:

```js
function add1(a, b) {
  return a + b;
}

const add2 = function (a, b) {
  return a + b;
};

const add3 = (a, b) => a + b;
```

### 7. How does `this` work in regular functions versus arrow functions?

Definition:
In regular functions, `this` depends on how the function is called. In arrow functions, `this` is inherited from the surrounding scope.

Why used:
Arrow functions avoid manual binding in callbacks.

Interview answer:
Use regular functions when you need dynamic `this`. Use arrow functions when you want lexical `this`.

Example:

```js
const user = {
  name: "Asha",
  regular() {
    console.log(this.name);
  },
  arrow: () => {
    console.log(this.name);
  }
};

user.regular(); // Asha
user.arrow(); // undefined in most cases
```

### 8. What is the event loop?

Definition:
The event loop is the mechanism that handles asynchronous operations in JavaScript.

Why used:
JavaScript is single-threaded, so the event loop coordinates callbacks, promises, and browser APIs.

Interview answer:
Synchronous code runs first, then microtasks like promises, then macrotasks like `setTimeout`.

Example:

```js
console.log("start");

setTimeout(() => console.log("timeout"), 0);
Promise.resolve().then(() => console.log("promise"));

console.log("end");

// start
// end
// promise
// timeout
```

### 9. What is the difference between microtasks and macrotasks?

Definition:
Microtasks include promise callbacks and mutation observers. Macrotasks include `setTimeout`, `setInterval`, and DOM events.

Why used:
Understanding them helps explain execution order.

Interview answer:
After synchronous code finishes, JavaScript processes all microtasks before taking the next macrotask from the queue.

### 10. What is the execution order of `setTimeout`, `Promise`, and synchronous code?

Interview answer:
Synchronous code runs first, then promises, then timers.

Example:

```js
console.log(1);
setTimeout(() => console.log(2), 0);
Promise.resolve().then(() => console.log(3));
console.log(4);

// 1 4 3 2
```

### 11. What is the difference between `==` and `===`?

Definition:
`==` compares after type conversion. `===` compares value and type without coercion.

Why used:
`===` is safer and more predictable.

Interview answer:
Prefer `===` to avoid unexpected coercion bugs.

Example:

```js
console.log(5 == "5"); // true
console.log(5 === "5"); // false
```

### 12. What is type coercion in JavaScript?

Definition:
Type coercion is automatic conversion from one type to another.

Why used:
It happens implicitly in comparisons, arithmetic, and string concatenation.

Interview answer:
JavaScript can convert types automatically, which is convenient but can also cause bugs if not understood.

Example:

```js
console.log("5" + 1); // "51"
console.log("5" - 1); // 4
```

### 13. What are primitive and reference types?

Definition:
Primitive types include string, number, boolean, null, undefined, bigint, and symbol. Objects, arrays, and functions are reference types.

Why used:
This difference matters for copying and comparison.

Interview answer:
Primitives are copied by value. Objects are copied by reference.

Example:

```js
let a = 10;
let b = a;
b = 20;

const obj1 = { name: "A" };
const obj2 = obj1;
obj2.name = "B";
console.log(obj1.name); // B
```

### 14. What is the difference between shallow copy and deep copy?

Definition:
A shallow copy copies only the first level. A deep copy copies nested levels too.

Why used:
Important in React state updates and immutable programming.

Interview answer:
Spread syntax creates shallow copies. For deeply nested objects, use `structuredClone` or a custom deep copy strategy.

Example:

```js
const user = { profile: { city: "Pune" } };
const shallow = { ...user };
shallow.profile.city = "Delhi";

console.log(user.profile.city); // Delhi
```

### 15. How do `map`, `filter`, `reduce`, `find`, and `forEach` differ?

Interview answer:
`map` transforms, `filter` selects, `reduce` accumulates, `find` returns the first match, and `forEach` just iterates without returning a transformed array.

Example:

```js
const nums = [1, 2, 3, 4];

nums.map((n) => n * 2); // [2, 4, 6, 8]
nums.filter((n) => n % 2 === 0); // [2, 4]
nums.reduce((sum, n) => sum + n, 0); // 10
nums.find((n) => n > 2); // 3
nums.forEach((n) => console.log(n));
```

### 16. What is immutability, and why is it important in frontend development?

Definition:
Immutability means not changing existing data directly, but creating new copies with updates.

Why used:
It makes state changes predictable and helps React detect updates.

Interview answer:
Immutable updates improve debugging, performance optimization, and state management reliability.

### 17. What are promises, and how do they differ from callbacks?

Definition:
A promise represents the eventual result of an asynchronous operation.

Why used:
Promises make async code cleaner and easier to chain.

Interview answer:
Promises solve callback nesting problems and support better error handling.

Example:

```js
fetch("/api/user")
  .then((res) => res.json())
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

### 18. How does `async/await` work internally with promises?

Definition:
`async` makes a function return a promise. `await` pauses within that function until the promise resolves or rejects.

Why used:
It makes async code read like synchronous code.

Interview answer:
`async/await` is syntactic sugar on top of promises.

Example:

```js
async function loadUser() {
  try {
    const res = await fetch("/api/user");
    const data = await res.json();
    return data;
  } catch (error) {
    console.error(error);
  }
}
```

### 19. What is error handling best practice in async JavaScript?

Interview answer:
Use `try/catch` with `async/await`, use `.catch()` with promise chains, handle user-friendly fallbacks, and avoid swallowing errors silently.

Example:

```js
async function getUsers() {
  try {
    const res = await fetch("/api/users");
    if (!res.ok) throw new Error("Request failed");
    return await res.json();
  } catch (error) {
    console.error("Failed to load users:", error);
    return [];
  }
}
```

### 20. What is debouncing and throttling?

Definition:
Debouncing delays execution until the user stops triggering an event. Throttling limits execution to once in a time interval.

Why used:
They improve performance for scroll, resize, and search inputs.

Interview answer:
Use debounce for search boxes and throttle for scroll or resize listeners.

### 21. What is event delegation, and why is it useful?

Definition:
Event delegation means attaching one event listener to a parent instead of many child elements.

Why used:
It improves performance and supports dynamic elements.

Interview answer:
It works because events bubble from child to parent.

Example:

```js
document.getElementById("list").addEventListener("click", (event) => {
  if (event.target.matches("button")) {
    console.log("Clicked:", event.target.textContent);
  }
});
```

### 22. What is prototype inheritance?

Definition:
Objects in JavaScript can inherit properties and methods from another object through the prototype chain.

Why used:
It enables method sharing without duplicating logic.

Interview answer:
JavaScript inheritance is prototype-based, not classical by default.

### 23. What is the difference between `Object.create`, constructor functions, and ES6 classes?

Interview answer:
All three create objects with inheritance. `Object.create` is low-level, constructor functions are the older pattern, and classes provide cleaner syntax over prototypes.

Example:

```js
class User {
  constructor(name) {
    this.name = name;
  }

  greet() {
    return `Hi ${this.name}`;
  }
}
```

### 24. How do modules work in JavaScript?

Definition:
Modules split code into reusable files using `export` and `import`.

Why used:
They improve maintainability, reuse, and code organization.

Interview answer:
Modules help isolate logic and avoid polluting the global scope.

Example:

```js
// math.js
export const add = (a, b) => a + b;

// app.js
import { add } from "./math.js";
console.log(add(2, 3));
```

### 25. What is the difference between CommonJS and ES modules?

Interview answer:
CommonJS uses `require` and `module.exports`, mainly in older Node.js code. ES modules use `import` and `export` and are standard in modern JavaScript.

### 26. What are generators, and when would you use them?

Definition:
Generators are functions that can pause and resume using `yield`.

Why used:
They are useful for custom iteration and lazy value generation.

Example:

```js
function* idGenerator() {
  let id = 1;
  while (true) {
    yield id++;
  }
}
```

### 27. What is currying?

Definition:
Currying transforms a function with multiple arguments into nested functions with one argument each.

Why used:
It helps create reusable specialized functions.

Example:

```js
const multiply = (a) => (b) => a * b;
const double = multiply(2);
console.log(double(5)); // 10
```

### 28. What are pure functions?

Definition:
A pure function always returns the same output for the same input and has no side effects.

Why used:
Pure functions are easier to test and reason about.

Example:

```js
const add = (a, b) => a + b;
```

### 29. What are side effects in JavaScript?

Definition:
A side effect is any operation that changes something outside the function, such as modifying DOM, changing global state, or making API calls.

Why used:
Real applications need side effects, but they should be controlled carefully.

Interview answer:
Good architecture keeps side effects isolated from pure business logic.

### 30. What is memoization?

Definition:
Memoization stores results of expensive function calls and reuses them for the same inputs.

Why used:
It improves performance when calculations repeat.

Example:

```js
function memoize(fn) {
  const cache = new Map();
  return function (...args) {
    const key = JSON.stringify(args);
    if (cache.has(key)) return cache.get(key);
    const result = fn(...args);
    cache.set(key, result);
    return result;
  };
}
```

### 31. What is the difference between `call`, `apply`, and `bind`?

Interview answer:
`call` invokes immediately with arguments one by one, `apply` invokes immediately with arguments as an array, and `bind` returns a new function with fixed `this`.

Example:

```js
function greet(city) {
  return `${this.name} from ${city}`;
}

const user = { name: "Riya" };
console.log(greet.call(user, "Mumbai"));
console.log(greet.apply(user, ["Delhi"]));

const bound = greet.bind(user);
console.log(bound("Pune"));
```

### 32. What are optional chaining and nullish coalescing?

Definition:
Optional chaining `?.` safely accesses nested properties. Nullish coalescing `??` returns a default only for `null` or `undefined`.

Why used:
They reduce verbose null checks.

Example:

```js
const user = {};
console.log(user.address?.city); // undefined
console.log(user.age ?? 18); // 18
```

### 33. How do `Set`, `Map`, `WeakSet`, and `WeakMap` differ?

Interview answer:
`Set` stores unique values, `Map` stores key-value pairs, `WeakSet` stores objects weakly, and `WeakMap` stores object keys weakly. Weak collections help with memory management because entries can be garbage collected.

### 34. How does garbage collection work at a high level?

Interview answer:
JavaScript automatically frees memory for values that are no longer reachable from the running program.

Why used:
It simplifies memory management, but developers still need to avoid unnecessary references.

### 35. What is a memory leak in JavaScript, and how can it happen in browser apps?

Definition:
A memory leak happens when memory is no longer needed but still cannot be garbage collected.

Common causes:
Unremoved event listeners, timers, stale closures, detached DOM references, and large cached objects.

Interview answer:
In SPAs, leaks usually happen when components unmount but listeners, intervals, or references remain active.

### 36. What are common security concerns in frontend JavaScript?

Interview answer:
Common concerns are XSS, insecure token storage, exposing sensitive data in client code, unsafe third-party scripts, and trusting user input without validation.

### 37. What is the difference between synchronous, asynchronous, parallel, and concurrent execution in JS apps?

Interview answer:
Synchronous means one task at a time in order. Asynchronous means work can finish later without blocking. Concurrent means multiple tasks make progress over time. Parallel means tasks truly run at the same time using multiple threads or processors.

### 38. How do browser storage APIs differ?

Interview answer:
`localStorage` persists until cleared, `sessionStorage` lasts for the tab session, and cookies are sent with HTTP requests and can have expiry and security flags.

### 39. What is the purpose of AbortController?

Definition:
`AbortController` cancels asynchronous operations like fetch requests.

Why used:
It prevents stale requests, wasted network calls, and state updates after unmount.

Example:

```js
const controller = new AbortController();

fetch("/api/data", { signal: controller.signal })
  .then((res) => res.json())
  .then(console.log)
  .catch((error) => {
    if (error.name === "AbortError") {
      console.log("Request cancelled");
    }
  });

controller.abort();
```

### 40. What are common JavaScript interview output-based trap questions testing?

Interview answer:
They usually test hoisting, closures, event loop order, `this`, async timing, type coercion, and scope behavior.

## Coding and Practical Questions with Answers

### 1. Implement a custom `debounce` function

Why used:
Used in search inputs and resize events to avoid too many calls.

```js
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

### 2. Implement a custom `throttle` function

Why used:
Used in scroll and resize handlers to limit function frequency.

```js
function throttle(fn, delay) {
  let lastCall = 0;

  return function (...args) {
    const now = Date.now();
    if (now - lastCall >= delay) {
      lastCall = now;
      fn.apply(this, args);
    }
  };
}
```

### 3. Write a polyfill for `Array.prototype.map`

```js
Array.prototype.myMap = function (callback) {
  const result = [];

  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
  }

  return result;
};
```

### 4. Write a polyfill for `Array.prototype.filter`

```js
Array.prototype.myFilter = function (callback) {
  const result = [];

  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      result.push(this[i]);
    }
  }

  return result;
};
```

### 5. Write a polyfill for `Array.prototype.reduce`

```js
Array.prototype.myReduce = function (callback, initialValue) {
  let accumulator = initialValue;
  let startIndex = 0;

  if (accumulator === undefined) {
    accumulator = this[0];
    startIndex = 1;
  }

  for (let i = startIndex; i < this.length; i++) {
    accumulator = callback(accumulator, this[i], i, this);
  }

  return accumulator;
};
```

### 6. Flatten a deeply nested array

```js
function flattenArray(arr) {
  return arr.reduce((acc, item) => {
    return acc.concat(Array.isArray(item) ? flattenArray(item) : item);
  }, []);
}
```

### 7. Deep clone a nested object

```js
function deepClone(obj) {
  return structuredClone(obj);
}
```

Note:
If `structuredClone` is not available, use a custom recursive function or a library.

### 8. Write a function to group an array of objects by a key

```js
function groupBy(arr, key) {
  return arr.reduce((acc, item) => {
    const group = item[key];
    if (!acc[group]) acc[group] = [];
    acc[group].push(item);
    return acc;
  }, {});
}
```

### 9. Implement a `once` utility function

```js
function once(fn) {
  let called = false;
  let result;

  return function (...args) {
    if (!called) {
      called = true;
      result = fn.apply(this, args);
    }
    return result;
  };
}
```

### 10. Create a memoization helper

```js
function memoize(fn) {
  const cache = new Map();

  return function (...args) {
    const key = JSON.stringify(args);
    if (cache.has(key)) return cache.get(key);
    const result = fn(...args);
    cache.set(key, result);
    return result;
  };
}
```

### 11. Implement `Promise.all` in a simplified way

```js
function myPromiseAll(promises) {
  return new Promise((resolve, reject) => {
    const results = [];
    let completed = 0;

    if (promises.length === 0) {
      resolve([]);
      return;
    }

    promises.forEach((promise, index) => {
      Promise.resolve(promise)
        .then((value) => {
          results[index] = value;
          completed++;
          if (completed === promises.length) {
            resolve(results);
          }
        })
        .catch(reject);
    });
  });
}
```

### 12. Create a retry wrapper for an async API function

```js
async function retry(fn, retries = 3) {
  let lastError;

  for (let i = 0; i < retries; i++) {
    try {
      return await fn();
    } catch (error) {
      lastError = error;
    }
  }

  throw lastError;
}
```

### 13. Write a function to cancel a fetch request using AbortController

```js
function fetchWithCancel(url) {
  const controller = new AbortController();

  const promise = fetch(url, { signal: controller.signal }).then((res) => res.json());

  return {
    promise,
    cancel: () => controller.abort()
  };
}
```

### 14. Build a simple event emitter class

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(eventName, listener) {
    if (!this.events[eventName]) this.events[eventName] = [];
    this.events[eventName].push(listener);
  }

  emit(eventName, ...args) {
    const listeners = this.events[eventName] || [];
    listeners.forEach((listener) => listener(...args));
  }

  off(eventName, listenerToRemove) {
    this.events[eventName] = (this.events[eventName] || []).filter(
      (listener) => listener !== listenerToRemove
    );
  }
}
```

### 15. Write a function to detect duplicate values in an array

```js
function hasDuplicates(arr) {
  return new Set(arr).size !== arr.length;
}
```

### 16. Sort an array of objects by multiple keys

```js
function sortByMultiple(arr) {
  return arr.sort((a, b) => {
    if (a.age !== b.age) return a.age - b.age;
    return a.name.localeCompare(b.name);
  });
}
```

### 17. Convert callback-based code to promise-based code

```js
function readData() {
  return new Promise((resolve, reject) => {
    oldApi((error, data) => {
      if (error) reject(error);
      else resolve(data);
    });
  });
}
```

### 18. Write a utility to compare two objects shallowly

```js
function shallowEqual(obj1, obj2) {
  const keys1 = Object.keys(obj1);
  const keys2 = Object.keys(obj2);

  if (keys1.length !== keys2.length) return false;

  for (const key of keys1) {
    if (obj1[key] !== obj2[key]) return false;
  }

  return true;
}
```

### 19. Build a pagination helper for frontend data

```js
function paginate(items, page, pageSize) {
  const start = (page - 1) * pageSize;
  return items.slice(start, start + pageSize);
}
```

### 20. Create a function that returns unique objects by `id`

```js
function uniqueById(arr) {
  const seen = new Set();

  return arr.filter((item) => {
    if (seen.has(item.id)) return false;
    seen.add(item.id);
    return true;
  });
}
```

### 21. Implement currying for a sum function

```js
function currySum(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}

console.log(currySum(1)(2)(3)); // 6
```

### 22. Write code to print numbers with correct async timing behavior

```js
for (let i = 1; i <= 3; i++) {
  setTimeout(() => {
    console.log(i);
  }, i * 1000);
}
```

Reason:
Use `let` because it creates block scope for each loop iteration.

### 23. Solve output-based questions involving closures inside loops

Wrong:

```js
for (var i = 1; i <= 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

Output:
`4 4 4`

Correct:

```js
for (let i = 1; i <= 3; i++) {
  setTimeout(() => console.log(i), 1000);
}
```

### 24. Build a simple LRU cache in JavaScript

```js
class LRUCache {
  constructor(limit) {
    this.limit = limit;
    this.cache = new Map();
  }

  get(key) {
    if (!this.cache.has(key)) return -1;
    const value = this.cache.get(key);
    this.cache.delete(key);
    this.cache.set(key, value);
    return value;
  }

  put(key, value) {
    if (this.cache.has(key)) {
      this.cache.delete(key);
    } else if (this.cache.size >= this.limit) {
      const oldestKey = this.cache.keys().next().value;
      this.cache.delete(oldestKey);
    }

    this.cache.set(key, value);
  }
}
```

### 25. Implement event delegation for a list of buttons

```js
document.getElementById("button-list").addEventListener("click", (event) => {
  if (event.target.matches("button")) {
    console.log("Clicked button:", event.target.dataset.id);
  }
});
```

Why used:
One parent listener can handle current and future child buttons.

## Accenture L2 Style JavaScript Answers

### 1. Explain the event loop with a real browser example

Best answer:
When a user clicks a button, synchronous code runs first. If that code starts a fetch or a timeout, the browser handles it outside the call stack. Once complete, callbacks are queued. Promise callbacks run in the microtask queue before timer callbacks in the macrotask queue.

### 2. Why do API calls often move from callbacks to promises to `async/await` in enterprise applications?

Best answer:
Because maintainability improves. Promises avoid callback nesting, and `async/await` makes flows like retry, error handling, loading states, and cleanup much easier to read and test.

### 3. How do you prevent memory leaks in large single-page applications?

Best answer:
Clean up event listeners, intervals, subscriptions, and pending requests. Avoid keeping unnecessary references in closures and caches. Profile memory in browser dev tools.

### 4. How do you debug slow screens caused by repeated re-renders and heavy JavaScript logic?

Best answer:
Profile first. Identify expensive loops, repeated calculations, large JSON parsing, or duplicate API calls. Memoize where needed, debounce user actions, paginate or virtualize large data, and move heavy work off the critical render path.

### 5. How would you structure reusable utility functions in a production codebase?

Best answer:
Group them by purpose like date, array, object, async, and validation helpers. Keep them pure where possible, test them independently, and avoid one huge generic utility file.

### 6. How do you handle API retries, cancellation, timeout, and fallback states?

Best answer:
Use `AbortController` for cancellation, wrap requests with retry logic for transient failures, implement timeouts where needed, and always show proper loading, error, and empty states in UI.

### 7. What JavaScript patterns help maintainability in large teams?

Best answer:
Use modules, pure functions, clear naming, shared utilities, consistent error handling, small focused functions, linting, and avoid hidden side effects.

### 8. How do you avoid race conditions when multiple async requests update the same UI?

Best answer:
Track the latest request, cancel stale ones, or ignore old responses if a newer request already exists.

### 9. What is the difference between optimistic updates and confirmed updates?

Best answer:
Optimistic updates change UI before server confirmation for faster experience. Confirmed updates wait for server success before updating UI. Optimistic updates need rollback handling.

### 10. How would you review a teammate's JavaScript for performance, readability, and edge cases?

Best answer:
Check naming clarity, function size, duplicate logic, async error handling, null cases, performance hotspots, mutation bugs, and whether tests cover edge conditions.

## Quick Revision Notes

1. Prefer `const` by default.
2. Understand closures, scope, hoisting, and `this`.
3. Be very strong in promises, `async/await`, event loop, and microtasks.
4. Practice debounce, throttle, polyfills, and array methods.
5. Know object copying, immutability, and memory leak prevention.
6. For Accenture L2, focus on practical scenario-based answers, not only definitions.
