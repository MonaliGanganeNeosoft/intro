# Accenture Interview

This file contains commonly asked Accenture L1 interview topics and coding questions for JavaScript, React, and CSS.

## JavaScript Theory Questions

1. Event loop
2. Microtask
3. Closure
4. `this` keyword
5. `call`, `apply`, and `bind` methods
6. Hoisting
7. Temporal dead zone
8. Prototypical inheritance
9. Shallow copy
10. Deep copy
11. Debounce
12. Throttling


## JavaScript Example Snippets

### Delete and Object Reference Example

```js
const obj = { prop: "old" };
const arr = [obj];
delete arr;

console.log(arr[0].prop); // old
```

### Debounce Example

```html
<input id="search" />
```

```js
function search() {
  console.log("searching...");
}

function debounce(func, delay) {
  let timer;

  return function () {
    const context = this;
    const args = arguments;

    clearTimeout(timer);
    timer = setTimeout(() => {
      func.apply(context, args);
    }, delay);
  };
}

const searchInput = document.getElementById("search");
searchInput.addEventListener("input", debounce(search, 500));
```

## React Custom Hook Example

```jsx
// function useCounter(initialValue = 0) {
//   const [count, setCount] = useState(initialValue);
//
//   const increment = () => setCount(count + 1);
//   const decrement = () => setCount(count - 1);
//   const reset = () => setCount(initialValue);
//
//   return { count, increment, decrement, reset };
// }
//
// export default useCounter;

const obj = { prop: "old" };
const arr = [obj];
delete arr;

console.log(arr[0].prop);
```

## CSS Theory Questions

1. Pseudo class
2. Pseudo element
3. Box model
4. Class and id

## JavaScript Coding Questions

1. Debouncing code
2. Array delete code
3. Reverse a string
4. Check palindrome string
5. Find duplicate elements in array
6. Remove duplicates from array
7. Find second largest number in array
8. Flatten nested array
9. Debounce function implementation
10. Throttle function implementation
11. Group array objects by property
12. Count frequency of elements in array
13. Find missing number in array
14. Sort array without using `.sort()`

## Advanced JavaScript Coding Questions

1. Implement `Promise.all`
2. Implement deep clone
3. Implement memoization
4. Polyfill for `map`
5. Polyfill for `filter`
6. Polyfill for `reduce`
7. Event emitter implementation
8. Implement LRU cache

## React Theory Questions

1. Functional component
2. `useEffect` in functional component
3. Unmount
4. Lifecycle methods in class component and function component
5. Virtual DOM
6. Reconciliation
7. Rendering
8. React Fiber
9. Problems solved by hooks
10. Custom hook with example
11. `useEffect` with dependency array
12. Prop drilling
13. Redux Toolkit
14. How to optimize application
15. Code splitting
16. Lazy loading

## React Coding Questions

1. Debounced search input
2. Pagination component
3. Custom Hook - `useDebounce`
4. Custom Hook - `useFetch`
5. Todo app with add, delete, and edit
6. Infinite scrolling
7. Accordion component
8. Modal component
9. Form validation
10. Dropdown with search
11. Drag and drop list
12. Implement `usePrevious` hook
13. Implement `useLocalStorage` hook

## React Concept and Coding Questions

1. Controlled vs uncontrolled component
2. Virtual DOM
3. `useMemo` vs `useCallback`
4. `useEffect` lifecycle
5. React performance optimization
6. Context API example
7. Redux flow
8. Code splitting with `lazy`
9. Error boundaries
10. React reconciliation

---

## Added Answers

### 1. Event loop
Definition: The event loop is the JavaScript mechanism that handles execution of synchronous code, callback queues, and asynchronous tasks.
Why we use it: It allows JavaScript to stay non-blocking even though it runs on a single thread.
How used: The call stack runs current code first, then the event loop checks queues and moves ready callbacks to the stack.

```js
console.log("start");

setTimeout(() => {
  console.log("timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("promise");
});

console.log("end");
// start
// end
// promise
// timeout
```

### 2. Microtask
Definition: A microtask is a high-priority async task that runs after the current synchronous code and before macrotasks like `setTimeout`.
Why we use it: It helps run promise callbacks quickly after current execution finishes.
How used: Promise `.then()`, `.catch()`, `.finally()`, and `queueMicrotask()` use the microtask queue.

```js
console.log("a");

queueMicrotask(() => console.log("microtask"));
setTimeout(() => console.log("macrotask"), 0);

console.log("b");
```

### 3. Closure
Definition: A closure is when an inner function remembers variables from its outer scope even after the outer function has finished.
Why we use it: It helps create private variables and reusable function factories.
How used: Return an inner function that uses an outer variable.

```js
function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const inc = counter();
console.log(inc()); // 1
console.log(inc()); // 2
```

### 4. `this` keyword
Definition: `this` refers to the object that is currently calling the function.
Why we use it: It helps access properties of the current object or execution context.
How used: Its value depends on how a function is called.

```js
const user = {
  name: "Aslam",
  show() {
    console.log(this.name);
  }
};

user.show();
```

### 5. `call`, `apply`, and `bind` methods
Definition: These methods are used to manually set the value of `this` for a function.
Why we use it: They help reuse a function with different objects.
How used: `call` passes arguments one by one, `apply` passes arguments as an array, and `bind` returns a new function.

```js
function greet(city) {
  console.log(this.name, city);
}

const person = { name: "Aslam" };

greet.call(person, "Delhi");
greet.apply(person, ["Mumbai"]);

const bound = greet.bind(person, "Pune");
bound();
```

### 6. Hoisting
Definition: Hoisting means declarations are moved to the top of their scope before execution.
Why we use it: It explains how JavaScript behaves when variables or functions are used before declaration.
How used: `var` is hoisted with `undefined`; function declarations are fully hoisted.

```js
console.log(a); // undefined
var a = 10;

sayHi();
function sayHi() {
  console.log("hi");
}
```

### 7. Temporal dead zone
Definition: The temporal dead zone is the time between entering scope and declaring a `let` or `const` variable.
Why we use it: It prevents using variables before proper initialization.
How used: Accessing `let` or `const` before declaration throws an error.

```js
// console.log(name); // ReferenceError
let name = "Aslam";
```

### 8. Prototypical inheritance
Definition: JavaScript objects can inherit properties and methods from another object through the prototype chain.
Why we use it: It enables code reuse and shared behavior.
How used: Use constructor functions, classes, or `Object.create()`.

```js
const animal = {
  eat() {
    console.log("eating");
  }
};

const dog = Object.create(animal);
dog.bark = function () {
  console.log("barking");
};

dog.eat();
dog.bark();
```

### 9. Shallow copy
Definition: A shallow copy copies only the first level, so nested objects still share the same reference.
Why we use it: It is fast and useful when nested data does not need separate copies.
How used: Use spread syntax or `Object.assign()`.

```js
const user = { name: "Aslam", address: { city: "Delhi" } };
const copy = { ...user };

copy.address.city = "Mumbai";
console.log(user.address.city); // Mumbai
```

### 10. Deep copy
Definition: A deep copy creates a completely independent copy of an object including nested values.
Why we use it: It prevents nested reference sharing.
How used: Use `structuredClone()` or a custom recursive solution.

```js
const user = { name: "Aslam", address: { city: "Delhi" } };
const copy = structuredClone(user);

copy.address.city = "Mumbai";
console.log(user.address.city); // Delhi
```

### 11. Debounce
Definition: Debounce delays function execution until the user stops triggering the event for a given time.
Why we use it: It reduces repeated function calls.
How used: Commonly used in search inputs and resize events.

```js
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

### 12. Throttling
Definition: Throttling ensures a function runs at most once in a specified time period.
Why we use it: It controls high-frequency events and improves performance.
How used: Commonly used in scroll, resize, and mousemove events.

```js
function throttle(fn, delay) {
  let lastCall = 0;

  return function (...args) {
    const now = Date.now();

    if (now - lastCall >= delay) {
      lastCall = now;
      fn(...args);
    }
  };
}
```

### 13. Pseudo class
Definition: A pseudo-class styles an element in a special state.
Why we use it: It helps style hover, focus, visited, and other states without extra classes.
How used: Write it with a single colon like `:hover`.

```css
button:hover {
  background: blue;
  color: white;
}
```

### 14. Pseudo element
Definition: A pseudo-element styles a specific part of an element.
Why we use it: It helps style or insert content without extra HTML.
How used: Write it with double colons like `::before` and `::after`.

```css
p::before {
  content: "Note: ";
  color: red;
}
```

### 15. Box model
Definition: The CSS box model consists of content, padding, border, and margin.
Why we use it: It explains spacing and layout behavior of elements.
How used: Adjust padding, border, and margin to control element size and spacing.

```css
.card {
  width: 200px;
  padding: 20px;
  border: 1px solid black;
  margin: 10px;
}
```

### 16. Class and id
Definition: A class can be reused on multiple elements; an id should be unique for one element.
Why we use it: Classes are used for reusable styling; ids are used for unique targeting.
How used: Use `class=""` for reusable styles and `id=""` for one unique element.

```html
<div class="card">Card 1</div>
<div class="card">Card 2</div>
<div id="header">Header</div>
```
