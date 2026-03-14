# Aslam Question List

## Screen 1

1. Difference between normal function and arrow function
2. Features of ECMAScript
3. `let`, `var`, `const`, and `package.json`
4. How to pass data from child to parent
5. Promises
6. Difference between XML / XHR and `fetch`
7. Difference between `git fetch` and `git pull`
8. Class component and function component
9. Stateless and stateful components
10. Controlled and uncontrolled components
11. `useCallback` and `useMemo`
12. How do you make synchronous code asynchronous?
13. Hoisting with example
14. Closures with example
15. `export`, `import`, `require`, and ES modules

## Screen 2

1. Redux and `useContext` with example
2. Lifecycle methods in React
3. Props and state
4. `splice()` and `slice()` method, and `hasOwnProperty()`
5. Routing in React JS
6. Callback, HOC, and HOF
7. What is DOM and Virtual DOM?
8. `async` / `await`
9. `setTimeout()` and `setInterval()`
10. Spread and rest operators
11. Shallow copy and deep copy
12. Code optimization
13. API call methods and HTTP methods
14. Difference between React JS and React Native
15. Redux and Flux
16. Why does CORS error occur?

## Screen 3

1. Fibonacci series
2. Factorial
3. Prime number
4. Unique number
5. Count how many repeated elements
6. Highest second number
7. Palindrome
8. Generate possibilities / pairs
9. Count vowels
10. Pattern logic
11. Longest substring without repeating characters
12. Find subarray in array
13. Find missing number in array
14. Deep clone

## Screen 4

1. Custom hooks
2. Counter to timer
3. Redux counter
4. Progress bar
5. API call with `fetch`
6. Color changer
7. Filter card
8. Generate random color
9. Form validation
10. Multi-select with all options
11. Target value from array by index
12. Change positions
13. Negative numbers from array
14. Longest substring

## Screen 5

1. Show / hide text
2. API call on click
3. Show list of response in two columns
4. Dropdown sorting: ascending and descending
5. Filter based on status code
6. 3 input fields with submit button, show data in table, and empty after submit
7. Create counter
8. Create timer with play, stop, and reset
9. Pagination with limit and make responsive

## Screen 6

1. What is pure component?
2. What does `key` do in React?
3. Error boundaries in React
4. Strict mode
5. Conditional rendering
6. What are hooks?
7. What is `ref` and `forwardRef`?
8. What is props drilling?
9. ESLint plugin and faulty pattern in React
10. Redux Thunk and Redux Saga
11. How to create a React app
12. What is JWT?

---

# Screen Wise Answers

## Screen 1 Answers

1. Difference between normal function and arrow function  
   Answer: A normal function has its own `this`, `arguments`, and can be used as a constructor with `new`. An arrow function does not have its own `this`; it uses lexical `this` from the parent scope and cannot be used as a constructor.

2. Features of ECMAScript  
   Answer: Common ECMAScript features include `let` and `const`, arrow functions, template literals, destructuring, spread/rest operators, promises, classes, modules, optional chaining, and async/await.

3. `let`, `var`, `const`, and `package.json`  
   Answer: `var` is function-scoped and can be redeclared; `let` is block-scoped and can be reassigned; `const` is block-scoped and cannot be reassigned. `package.json` stores project metadata, scripts, dependencies, and configuration.

4. How to pass data from child to parent  
   Answer: In React, data is usually passed from child to parent using a callback function given through props. The child calls that function and sends the value back.

5. Promises  
   Answer: A Promise represents the result of an asynchronous operation. It has three states: `pending`, `fulfilled`, and `rejected`, and is handled using `.then()`, `.catch()`, and `.finally()`.

6. Difference between XML / XHR and `fetch`  
   Answer: `XMLHttpRequest` is the older way to make HTTP requests and is more verbose. `fetch` is modern, promise-based, cleaner to read, and works well with async/await.

7. Difference between `git fetch` and `git pull`  
   Answer: `git fetch` only downloads latest changes from the remote repository. `git pull` downloads the changes and also merges or rebases them into the current local branch.

8. Class component and function component  
   Answer: Class components use ES6 classes and lifecycle methods like `componentDidMount`. Function components are simpler and now support state and side effects using React Hooks.

9. Stateless and stateful components  
   Answer: A stateless component only receives props and renders UI. A stateful component manages its own state and can change behavior or UI over time.

10. Controlled and uncontrolled components  
   Answer: In a controlled component, form data is managed by React state. In an uncontrolled component, the form data is handled by the DOM and usually accessed using `ref`.

11. `useCallback` and `useMemo`  
   Answer: `useCallback` memoizes a function so the same function reference can be reused. `useMemo` memoizes a computed value so expensive calculations are not repeated unnecessarily.

12. How do you make synchronous code asynchronous?  
   Answer: You can move work into asynchronous APIs like `setTimeout`, promises, `fetch`, web workers, or async functions so the main thread is not blocked.

13. Hoisting with example  
   Answer: Hoisting means declarations are moved to the top of their scope during execution. `var` is hoisted and initialized as `undefined`, while `let` and `const` are hoisted but stay in the temporal dead zone until declared.

14. Closures with example  
   Answer: A closure happens when an inner function remembers variables from its outer function even after the outer function has finished. This is commonly used for data privacy and function factories.

15. `export`, `import`, `require`, and ES modules  
   Answer: `export` and `import` belong to ES modules and are the modern JavaScript module system. `require` belongs to CommonJS, mostly used in older Node.js code.

## Screen 2 Answers

1. Redux and `useContext` with example  
   Answer: Redux is a global state management library with a store, actions, and reducers. `useContext` shares data through the component tree without prop drilling and is useful for simpler shared state.

2. Lifecycle methods in React  
   Answer: In class components, common lifecycle methods are `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`. In function components, `useEffect` is used to handle similar lifecycle behavior.

3. Props and state  
   Answer: Props are read-only values passed from parent to child. State is managed inside the component and can change over time, causing re-rendering.

4. `splice()` and `slice()` method, and `hasOwnProperty()`  
   Answer: `slice()` returns a shallow copy of part of an array without modifying the original array. `splice()` changes the original array by adding, removing, or replacing items. `hasOwnProperty()` checks whether an object contains a property directly on itself.

5. Routing in React JS  
   Answer: Routing in React is usually handled by `react-router-dom`. It maps URLs to components and supports navigation, route parameters, nested routes, and protected routes.

6. Callback, HOC, and HOF  
   Answer: A callback is a function passed into another function. An HOC is a Higher Order Component that takes a component and returns an enhanced component. An HOF is a Higher Order Function that takes or returns another function.

7. What is DOM and Virtual DOM?  
   Answer: The DOM is the real browser representation of HTML. The Virtual DOM is a lightweight JavaScript copy React uses to compare changes and update only the necessary parts of the real DOM.

8. `async` / `await`  
   Answer: `async` makes a function return a promise, and `await` pauses inside that function until the promise resolves or rejects. It makes asynchronous code easier to read than chained `.then()` calls.

9. `setTimeout()` and `setInterval()`  
   Answer: `setTimeout()` runs code once after a delay. `setInterval()` runs code repeatedly at a fixed time interval until it is cleared.

10. Spread and rest operators  
   Answer: The spread operator expands values from arrays or objects, for example in copying or merging. The rest operator collects multiple values into a single array or object.

11. Shallow copy and deep copy  
   Answer: A shallow copy copies only the first level, so nested objects still share references. A deep copy creates fully independent nested values.

12. Code optimization  
   Answer: Code optimization means improving performance, readability, and maintainability. In React it often includes memoization, lazy loading, reducing unnecessary renders, and efficient API usage.

13. API call methods and HTTP methods  
   Answer: Common HTTP methods are `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`. API calls are made using tools like `fetch` or `axios` to communicate with the backend.

14. Difference between React JS and React Native  
   Answer: React JS is used for web applications and renders HTML in the browser. React Native is used for mobile apps and renders native mobile components instead of HTML.

15. Redux and Flux  
   Answer: Flux is a general unidirectional data-flow pattern. Redux is a library inspired by Flux that centralizes state in one store and uses reducers for predictable updates.

16. Why does CORS error occur?  
   Answer: A CORS error happens when a browser blocks a request from one origin to another origin because the server did not allow that origin in its CORS headers.

## Screen 3 Answers

1. Fibonacci series  
   Answer: In a Fibonacci series, each number is the sum of the previous two numbers, such as `0, 1, 1, 2, 3, 5, 8`. It can be generated using loops or recursion.

2. Factorial  
   Answer: The factorial of `n` is the product of all positive integers from `1` to `n`. Example: `5! = 5 * 4 * 3 * 2 * 1 = 120`.

3. Prime number  
   Answer: A prime number is a number greater than `1` that has only two factors: `1` and itself. Example: `2`, `3`, `5`, and `7`.

4. Unique number  
   Answer: A unique number in an array is a value that appears only once. It can be found using frequency counting, a hash map, or XOR in some cases.

5. Count how many repeated elements  
   Answer: Repeated elements can be counted using an object or `Map` where each value is stored with its frequency. Any frequency greater than `1` means the item is repeated.

6. Highest second number  
   Answer: The second highest number is the largest number after removing the maximum value. It can be found in one pass by tracking the largest and second largest values.

7. Palindrome  
   Answer: A palindrome is a string or number that reads the same forward and backward, like `madam` or `121`. It can be checked by reversing and comparing.

8. Generate possibilities / pairs  
   Answer: This usually means generating combinations, permutations, or all possible pairs from a string or array. Nested loops or recursion are common approaches.

9. Count vowels  
   Answer: Vowels are `a`, `e`, `i`, `o`, and `u`. You can count them by looping through the string and checking each character.

10. Pattern logic  
   Answer: Pattern logic questions print shapes like triangles, pyramids, or stars. They are usually solved with nested loops controlling rows, spaces, and symbols.

11. Longest substring without repeating characters  
   Answer: This is commonly solved using a sliding window and a `Set` or `Map`. The window expands until a repeated character appears, then shrinks from the left.

12. Find subarray in array  
   Answer: A subarray is a continuous part of an array. Depending on the problem, you can find it using loops, prefix sums, or sliding window techniques.

13. Find missing number in array  
   Answer: If numbers are expected in a sequence, the missing one can be found using the expected sum formula or XOR. Example: for `1` to `n`, missing = expected sum - actual sum.

14. Deep clone  
   Answer: Deep clone means creating a completely independent copy of an object, including nested objects and arrays. Common options are `structuredClone()`, recursion, or library helpers.

## Screen 4 Answers

1. Custom hooks  
   Answer: A custom hook is a reusable JavaScript function whose name starts with `use` and that can use other hooks. It helps share logic between components.

2. Counter to timer  
   Answer: A counter can be converted into a timer by increasing or decreasing the count at regular intervals using `setInterval()` and cleaning it up properly.

3. Redux counter  
   Answer: A Redux counter example stores count in the Redux store and updates it through actions like increment and decrement handled by a reducer.

4. Progress bar  
   Answer: A progress bar visually shows completion percentage. In React it is usually built by changing width based on state or API progress.

5. API call with `fetch`  
   Answer: `fetch()` is used to make HTTP requests and returns a promise. A typical flow is `fetch(url).then(res => res.json())` or using async/await with error handling.

6. Color changer  
   Answer: A color changer updates a color value in state and applies it to the UI, usually through inline styles or class changes.

7. Filter card  
   Answer: A filter card usually displays a list of items and filters them based on category, search text, or selected options using array `.filter()`.

8. Generate random color  
   Answer: A random color can be generated using random RGB values or a random hexadecimal string like `#A1B2C3`.

9. Form validation  
   Answer: Form validation checks user input before submission, such as required fields, email format, password rules, and value length.

10. Multi-select with all options  
   Answer: A multi-select allows selecting multiple items, and a "Select All" option updates the selected list to include every option or clear all.

11. Target value from array by index  
   Answer: If the index is known, the value is accessed directly using `arr[index]`. If the question means finding an index by value, methods like `indexOf()` or `findIndex()` are used.

12. Change positions  
   Answer: Change positions usually means swapping elements in an array. This can be done with a temporary variable or array destructuring.

13. Negative numbers from array  
   Answer: Negative numbers can be extracted using `.filter(num => num < 0)`. This returns only values less than zero.

14. Longest substring  
   Answer: The longest substring problem often refers to longest substring without duplicates or longest valid substring by a rule. Sliding window is a common solution for such questions.

## Screen 5 Answers

1. Show / hide text  
   Answer: This is usually done using a boolean state like `show`, and rendering the text conditionally when the value is `true`.

2. API call on click  
   Answer: Instead of calling an API on page load, attach the request function to a button click handler so the request runs only when the user clicks.

3. Show list of response in two columns  
   Answer: The response array can be rendered using CSS Grid or Flexbox with two columns. Each item is mapped into a card or row.

4. Dropdown sorting: ascending and descending  
   Answer: Use a select dropdown to choose sort order, then sort the array using a compare function such as `(a, b) => a - b` for ascending.

5. Filter based on status code  
   Answer: If each item has a status code, use `.filter()` to return only the records matching the selected status like `200`, `404`, or `500`.

6. 3 input fields with submit button, show data in table, and empty after submit  
   Answer: Store the three field values in state, push them into an array on submit, render the array in a table, and reset the input states after submission.

7. Create counter  
   Answer: A counter is built using `useState` with increment, decrement, and reset handlers that update the count value.

8. Create timer with play, stop, and reset  
   Answer: A timer uses `setInterval()` to update time when play starts, `clearInterval()` to stop it, and resets the value back to initial state when reset is clicked.

9. Pagination with limit and make responsive  
   Answer: Pagination divides a large list into pages using a page number and item limit. Responsiveness is handled with flexible layout and proper mobile-friendly controls.

## Screen 6 Answers

1. What is pure component?  
   Answer: A Pure Component in React avoids unnecessary re-renders by doing a shallow comparison of props and state. In function components, similar behavior is achieved with `React.memo`.

2. What does `key` do in React?  
   Answer: A `key` helps React identify which list items changed, were added, or removed. Stable keys improve list rendering and reconciliation.

3. Error boundaries in React  
   Answer: Error boundaries catch JavaScript errors in child component trees during rendering, lifecycle methods, and constructors, then show fallback UI instead of crashing the whole app.

4. Strict mode  
   Answer: `React.StrictMode` is a development-only tool that highlights unsafe patterns, deprecated APIs, and side-effect issues. It does not affect production output.

5. Conditional rendering  
   Answer: Conditional rendering means showing different UI based on a condition, usually with `if`, ternary operators, logical `&&`, or early returns.

6. What are hooks?  
   Answer: Hooks are React functions like `useState`, `useEffect`, and `useRef` that let function components use state, side effects, refs, and reusable logic.

7. What is `ref` and `forwardRef`?  
   Answer: `ref` gives direct access to a DOM element or component instance value. `forwardRef` lets a parent pass a ref through a component to one of its child DOM nodes.

8. What is props drilling?  
   Answer: Props drilling happens when data is passed through many intermediate components just to reach a deeply nested child. Context API or state management tools can reduce it.

9. ESLint plugin and faulty pattern in React  
   Answer: ESLint plugins like `eslint-plugin-react` and `eslint-plugin-react-hooks` help catch bad patterns such as missing hook dependencies, unused variables, and invalid JSX practices.

10. Redux Thunk and Redux Saga  
   Answer: Redux Thunk handles async logic by allowing action creators to return functions. Redux Saga uses generator functions for more advanced async flows like retries, cancellation, and background tasks.

11. How to create a React app  
   Answer: A React app can be created using tools like `create-react-app` or `Vite`. Example: `npm create vite@latest my-app` or `npx create-react-app my-app`.

12. What is JWT?  
   Answer: JWT stands for JSON Web Token. It is a compact token format used for authentication and authorization, usually containing a header, payload, and signature.

---

# Screen Wise Code Examples

## Screen 1 Code Examples

### 4. How to pass data from child to parent

```jsx
import React, { useState } from "react";

function Child({ sendData }) {
  return <button onClick={() => sendData("Hello Parent")}>Send</button>;
}

export default function Parent() {
  const [message, setMessage] = useState("");

  return (
    <div>
      <Child sendData={setMessage} />
      <p>{message}</p>
    </div>
  );
}
```

### 5. Promises

```js
function getData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve("Data loaded"), 1000);
  });
}

getData()
  .then((res) => console.log(res))
  .catch((err) => console.error(err));
```

### 11. `useCallback` and `useMemo`

```jsx
import React, { useCallback, useMemo, useState } from "react";

export default function App() {
  const [count, setCount] = useState(0);
  const [num, setNum] = useState(5);

  const multiply = useMemo(() => num * 10, [num]);
  const handleClick = useCallback(() => {
    console.log("Button clicked");
  }, []);

  return (
    <div>
      <p>{multiply}</p>
      <button onClick={() => setCount(count + 1)}>Count {count}</button>
      <button onClick={handleClick}>Click</button>
    </div>
  );
}
```

### 13. Hoisting example

```js
console.log(a); // undefined
var a = 10;

// console.log(b); // ReferenceError
let b = 20;
```

### 14. Closures example

```js
function outer() {
  let count = 0;

  return function inner() {
    count++;
    return count;
  };
}

const fn = outer();
console.log(fn()); // 1
console.log(fn()); // 2
```

### 15. `export` and `import`

```js
// math.js
export const sum = (a, b) => a + b;

// app.js
import { sum } from "./math.js";
console.log(sum(2, 3));
```

## Screen 2 Code Examples

### 1. `useContext` example

```jsx
import React, { createContext, useContext } from "react";

const UserContext = createContext();

function Child() {
  const user = useContext(UserContext);
  return <h1>{user}</h1>;
}

export default function App() {
  return (
    <UserContext.Provider value="Aslam">
      <Child />
    </UserContext.Provider>
  );
}
```

### 8. `async` / `await`

```js
async function getUsers() {
  try {
    const res = await fetch("https://jsonplaceholder.typicode.com/users");
    const data = await res.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

getUsers();
```

### 9. `setTimeout()` and `setInterval()`

```js
setTimeout(() => {
  console.log("Runs once after 1 second");
}, 1000);

const id = setInterval(() => {
  console.log("Runs every 2 seconds");
}, 2000);

setTimeout(() => clearInterval(id), 7000);
```

### 10. Spread and rest operators

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // [1, 2, 3, 4]

function total(...nums) {
  return nums.reduce((sum, item) => sum + item, 0);
}

console.log(total(1, 2, 3, 4)); // 10
```

### 11. Shallow copy and deep copy

```js
const user = { name: "Aslam", address: { city: "Delhi" } };

const shallow = { ...user };
const deep = structuredClone(user);

shallow.address.city = "Mumbai";

console.log(user.address.city); // Mumbai
console.log(deep.address.city); // Delhi
```

## Screen 3 Code Examples

### 1. Fibonacci series

```js
function fibonacci(n) {
  const result = [0, 1];

  for (let i = 2; i < n; i++) {
    result.push(result[i - 1] + result[i - 2]);
  }

  return result;
}

console.log(fibonacci(7));
```

### 2. Factorial

```js
function factorial(n) {
  let result = 1;

  for (let i = 1; i <= n; i++) {
    result *= i;
  }

  return result;
}

console.log(factorial(5)); // 120
```

### 3. Prime number

```js
function isPrime(num) {
  if (num <= 1) return false;

  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }

  return true;
}

console.log(isPrime(7)); // true
```

### 6. Second highest number

```js
function secondLargest(arr) {
  const unique = [...new Set(arr)].sort((a, b) => b - a);
  return unique[1];
}

console.log(secondLargest([10, 20, 30, 40, 30])); // 30
```

### 7. Palindrome

```js
function isPalindrome(str) {
  return str === str.split("").reverse().join("");
}

console.log(isPalindrome("madam")); // true
```

### 9. Count vowels

```js
function countVowels(str) {
  return str.match(/[aeiou]/gi)?.length || 0;
}

console.log(countVowels("javascript")); // 3
```

### 11. Longest substring without repeating characters

```js
function longestSubstring(s) {
  let set = new Set();
  let left = 0;
  let max = 0;

  for (let right = 0; right < s.length; right++) {
    while (set.has(s[right])) {
      set.delete(s[left]);
      left++;
    }

    set.add(s[right]);
    max = Math.max(max, right - left + 1);
  }

  return max;
}

console.log(longestSubstring("abcabcbb")); // 3
```

### 13. Find missing number in array

```js
function missingNumber(arr, n) {
  const expected = (n * (n + 1)) / 2;
  const actual = arr.reduce((sum, item) => sum + item, 0);
  return expected - actual;
}

console.log(missingNumber([1, 2, 3, 5], 5)); // 4
```

### 14. Deep clone

```js
const obj = { a: 1, b: { c: 2 } };
const copy = structuredClone(obj);

copy.b.c = 99;

console.log(obj.b.c); // 2
console.log(copy.b.c); // 99
```

## Screen 4 Code Examples

### 1. Custom hooks

```jsx
import { useEffect, useState } from "react";

function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener("resize", handleResize);
    return () => window.removeEventListener("resize", handleResize);
  }, []);

  return width;
}
```

### 5. API call with `fetch`

```jsx
import React, { useEffect, useState } from "react";

export default function App() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then((res) => res.json())
      .then((data) => setUsers(data));
  }, []);

  return (
    <ul>
      {users.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}
```

### 8. Generate random color

```js
function randomColor() {
  const letters = "0123456789ABCDEF";
  let color = "#";

  for (let i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }

  return color;
}

console.log(randomColor());
```

### 9. Form validation

```jsx
import React, { useState } from "react";

export default function App() {
  const [email, setEmail] = useState("");
  const [error, setError] = useState("");

  const handleSubmit = () => {
    if (!email.includes("@")) {
      setError("Invalid email");
      return;
    }

    setError("");
    alert("Submitted");
  };

  return (
    <div>
      <input value={email} onChange={(e) => setEmail(e.target.value)} />
      <button onClick={handleSubmit}>Submit</button>
      <p>{error}</p>
    </div>
  );
}
```

### 10. Multi-select with all options

```jsx
import React, { useState } from "react";

export default function App() {
  const options = ["HTML", "CSS", "JS"];
  const [selected, setSelected] = useState([]);

  const handleAll = () => {
    setSelected(selected.length === options.length ? [] : options);
  };

  return (
    <div>
      <button onClick={handleAll}>Select All</button>
      {options.map((item) => (
        <div key={item}>
          <input
            type="checkbox"
            checked={selected.includes(item)}
            onChange={() =>
              setSelected((prev) =>
                prev.includes(item)
                  ? prev.filter((x) => x !== item)
                  : [...prev, item]
              )
            }
          />
          {item}
        </div>
      ))}
    </div>
  );
}
```

## Screen 5 Code Examples

### 1. Show / hide text

```jsx
import React, { useState } from "react";

export default function App() {
  const [show, setShow] = useState(false);

  return (
    <div>
      <button onClick={() => setShow(!show)}>Toggle</button>
      {show && <p>Hello World</p>}
    </div>
  );
}
```

### 2. API call on click

```jsx
import React, { useState } from "react";

export default function App() {
  const [users, setUsers] = useState([]);

  const getUsers = async () => {
    const res = await fetch("https://jsonplaceholder.typicode.com/users");
    const data = await res.json();
    setUsers(data);
  };

  return (
    <div>
      <button onClick={getUsers}>Load Users</button>
      {users.map((user) => (
        <p key={user.id}>{user.name}</p>
      ))}
    </div>
  );
}
```

### 4. Dropdown sorting

```js
const numbers = [30, 10, 50, 20];

const asc = [...numbers].sort((a, b) => a - b);
const desc = [...numbers].sort((a, b) => b - a);

console.log(asc);
console.log(desc);
```

### 6. 3 input fields and table

```jsx
import React, { useState } from "react";

export default function App() {
  const [form, setForm] = useState({ name: "", email: "", city: "" });
  const [rows, setRows] = useState([]);

  const handleSubmit = () => {
    setRows((prev) => [...prev, form]);
    setForm({ name: "", email: "", city: "" });
  };

  return (
    <div>
      <input value={form.name} onChange={(e) => setForm({ ...form, name: e.target.value })} />
      <input value={form.email} onChange={(e) => setForm({ ...form, email: e.target.value })} />
      <input value={form.city} onChange={(e) => setForm({ ...form, city: e.target.value })} />
      <button onClick={handleSubmit}>Submit</button>

      <table>
        <tbody>
          {rows.map((item, index) => (
            <tr key={index}>
              <td>{item.name}</td>
              <td>{item.email}</td>
              <td>{item.city}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}
```

### 7. Create counter

```jsx
import React, { useState } from "react";

export default function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <button onClick={() => setCount(count - 1)}>-</button>
      <span>{count}</span>
      <button onClick={() => setCount(count + 1)}>+</button>
    </div>
  );
}
```

### 8. Timer with play, stop, and reset

```jsx
import React, { useRef, useState } from "react";

export default function App() {
  const [time, setTime] = useState(0);
  const timerRef = useRef(null);

  const start = () => {
    if (timerRef.current) return;
    timerRef.current = setInterval(() => {
      setTime((prev) => prev + 1);
    }, 1000);
  };

  const stop = () => {
    clearInterval(timerRef.current);
    timerRef.current = null;
  };

  const reset = () => {
    stop();
    setTime(0);
  };

  return (
    <div>
      <p>{time}</p>
      <button onClick={start}>Play</button>
      <button onClick={stop}>Stop</button>
      <button onClick={reset}>Reset</button>
    </div>
  );
}
```

### 9. Pagination with limit

```jsx
import React, { useState } from "react";

export default function App() {
  const items = ["A", "B", "C", "D", "E", "F"];
  const [page, setPage] = useState(1);
  const limit = 2;

  const start = (page - 1) * limit;
  const visible = items.slice(start, start + limit);

  return (
    <div>
      {visible.map((item) => (
        <p key={item}>{item}</p>
      ))}
      <button disabled={page === 1} onClick={() => setPage(page - 1)}>Prev</button>
      <button disabled={start + limit >= items.length} onClick={() => setPage(page + 1)}>Next</button>
    </div>
  );
}
```

## Screen 6 Code Examples

### 3. Error boundaries

```jsx
import React from "react";

class ErrorBoundary extends React.Component {
  state = { hasError: false };

  static getDerivedStateFromError() {
    return { hasError: true };
  }

  render() {
    if (this.state.hasError) {
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children;
  }
}
```

### 5. Conditional rendering

```jsx
function App({ isLoggedIn }) {
  return <div>{isLoggedIn ? <h1>Welcome</h1> : <h1>Please Login</h1>}</div>;
}
```

### 7. `ref` and `forwardRef`

```jsx
import React, { forwardRef, useRef } from "react";

const Input = forwardRef((props, ref) => {
  return <input ref={ref} {...props} />;
});

export default function App() {
  const inputRef = useRef(null);

  return (
    <div>
      <Input ref={inputRef} />
      <button onClick={() => inputRef.current.focus()}>Focus</button>
    </div>
  );
}
```

### 11. How to create a React app

```bash
npm create vite@latest my-app
cd my-app
npm install
npm run dev
```

### 12. JWT example

```js
const token = "header.payload.signature";
const payload = {
  userId: 101,
  role: "admin"
};

console.log(token);
console.log(payload);
```
