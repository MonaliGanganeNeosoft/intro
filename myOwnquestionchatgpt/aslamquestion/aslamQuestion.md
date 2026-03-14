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

---

# Detailed Interview Format

## Screen 1 Detailed Notes

### 1. Difference between normal function and arrow function
Definition: A normal function has its own `this`, while an arrow function uses `this` from the parent scope.
Why: It matters when working with event handlers, objects, and callbacks.
When: Use arrow functions for short callbacks. Use normal functions when you need your own `this`.
Where: Common in React handlers, array methods, and object methods.

```js
const obj = {
  name: "Aslam",
  normal: function () {
    console.log(this.name);
  },
  arrow: () => {
    console.log(this.name);
  }
};
```

### 2. Features of ECMAScript
Definition: ECMAScript is the JavaScript standard that introduces language features.
Why: It makes code shorter, cleaner, and easier to maintain.
When: Use modern syntax in new projects.
Where: Used in frontend, backend, and tooling.

```js
const user = { name: "Aslam" };
const { name } = user;
const msg = `Hello ${name}`;
console.log(msg);
```

### 3. `let`, `var`, `const`, and `package.json`
Definition: `var` is function-scoped, `let` and `const` are block-scoped, and `package.json` holds project metadata.
Why: Correct variable choice prevents bugs; `package.json` manages scripts and dependencies.
When: Use `const` by default, `let` when reassignment is needed, avoid `var` in modern code.
Where: Used in all JavaScript projects and Node/React apps.

```js
let count = 1;
const appName = "demo-app";
var oldValue = "legacy";
```

```json
{
  "name": "demo-app",
  "scripts": {
    "start": "vite"
  }
}
```

### 4. How to pass data from child to parent
Definition: The child sends data to the parent by calling a function passed through props.
Why: React data flow is mainly top to bottom, so callbacks help send values back up.
When: Use it when a child input or button needs to update parent state.
Where: Forms, modals, dropdowns, and reusable child components.

```jsx
function Child({ onSend }) {
  return <button onClick={() => onSend("hello")}>Send</button>;
}
```

### 5. Promises
Definition: A Promise represents an async operation that may resolve or reject later.
Why: It helps handle async code without deeply nested callbacks.
When: Use for API calls, timers, and async tasks.
Where: `fetch`, database calls, file operations, and custom async logic.

```js
new Promise((resolve) => {
  setTimeout(() => resolve("done"), 1000);
}).then(console.log);
```

### 6. Difference between XML / XHR and `fetch`
Definition: XHR is the older browser API for requests; `fetch` is the modern promise-based API.
Why: `fetch` is cleaner and works naturally with async/await.
When: Prefer `fetch` in modern applications.
Where: Frontend API requests.

```js
fetch("/api/users")
  .then((res) => res.json())
  .then((data) => console.log(data));
```

### 7. Difference between `git fetch` and `git pull`
Definition: `git fetch` downloads remote changes only; `git pull` downloads and merges them.
Why: It helps avoid accidental merges.
When: Use `fetch` when you want to review first, `pull` when ready to update local branch.
Where: Git repositories and team workflows.

```bash
git fetch origin
git pull origin main
```

### 8. Class component and function component
Definition: Class components use ES6 classes; function components are plain functions that return JSX.
Why: Function components are simpler and work well with Hooks.
When: Use function components in modern React.
Where: React web apps and React Native apps.

```jsx
function Welcome() {
  return <h1>Hello</h1>;
}
```

### 9. Stateless and stateful components
Definition: Stateless components only use props; stateful components manage their own state.
Why: It helps separate presentational and logic-heavy parts.
When: Use stateless for display-only UI, stateful for interactive UI.
Where: Buttons, forms, modals, counters.

```jsx
function Title({ text }) {
  return <h1>{text}</h1>;
}
```

### 10. Controlled and uncontrolled components
Definition: Controlled inputs are managed by React state; uncontrolled inputs are managed by the DOM.
Why: Controlled components give better validation and predictability.
When: Use controlled inputs for most React forms.
Where: Login, signup, search, filters.

```jsx
const [name, setName] = useState("");
<input value={name} onChange={(e) => setName(e.target.value)} />;
```

### 11. `useCallback` and `useMemo`
Definition: `useCallback` caches a function; `useMemo` caches a calculated value.
Why: They help avoid unnecessary renders or recalculations.
When: Use when passing callbacks to memoized children or doing expensive calculations.
Where: Performance-sensitive React components.

```jsx
const total = useMemo(() => items.length, [items]);
const handleClick = useCallback(() => console.log("clicked"), []);
```

### 12. How do you make synchronous code asynchronous?
Definition: You move work into async APIs like promises, timers, or async functions.
Why: It prevents blocking the main thread.
When: Use when handling I/O, API calls, or deferred work.
Where: API requests, delayed tasks, large computations.

```js
setTimeout(() => {
  console.log("async task");
}, 0);
```

### 13. Hoisting with example
Definition: Hoisting means JavaScript moves declarations to the top of scope during compilation.
Why: It explains why `var` behaves differently from `let` and `const`.
When: Important while debugging variable access before declaration.
Where: Functions, variables, and interview questions.

```js
console.log(a);
var a = 10;
```

### 14. Closures with example
Definition: A closure is when an inner function remembers variables from its outer scope.
Why: It enables private state and reusable function factories.
When: Use for counters, memoization, and callbacks.
Where: JavaScript utilities and React event logic.

```js
function outer() {
  let value = 0;
  return () => ++value;
}
```

### 15. `export`, `import`, `require`, and ES modules
Definition: `export` and `import` are ES module syntax; `require` is CommonJS syntax.
Why: Modules organize code into reusable files.
When: Use ES modules in modern frontend and Node projects.
Where: React apps, Node apps, libraries.

```js
export const sum = (a, b) => a + b;
import { sum } from "./math.js";
```

## Screen 2 Detailed Notes

### 1. Redux and `useContext` with example
Definition: Redux is a full state management library; `useContext` shares data across components without prop drilling.
Why: They simplify shared state handling.
When: Use `useContext` for light shared state, Redux for complex app-wide state.
Where: Authentication, theme, cart, dashboards.

```jsx
const ThemeContext = React.createContext("light");
const theme = React.useContext(ThemeContext);
```

### 2. Lifecycle methods in React
Definition: Lifecycle methods define what happens when a component mounts, updates, and unmounts.
Why: They help run side effects at the right time.
When: Use `useEffect` in function components for lifecycle-like behavior.
Where: API calls, subscriptions, cleanup.

```jsx
useEffect(() => {
  console.log("mounted");
  return () => console.log("unmounted");
}, []);
```

### 3. Props and state
Definition: Props are inputs from parent; state is internal component data.
Why: This is the core of React component design.
When: Use props for external data, state for local changes.
Where: All React components.

```jsx
function Card({ title }) {
  const [open, setOpen] = useState(false);
  return <button onClick={() => setOpen(!open)}>{title}</button>;
}
```

### 4. `splice()` and `slice()` method, and `hasOwnProperty()`
Definition: `slice()` copies data, `splice()` mutates arrays, and `hasOwnProperty()` checks direct object properties.
Why: These are common JavaScript interview methods.
When: Use `slice` for copy, `splice` for edit, `hasOwnProperty` for property checks.
Where: Arrays, objects, data transforms.

```js
const arr = [1, 2, 3, 4];
console.log(arr.slice(1, 3));
arr.splice(1, 1);
console.log({ a: 1 }.hasOwnProperty("a"));
```

### 5. Routing in React JS
Definition: Routing maps URLs to React components.
Why: It enables page-like navigation in single-page apps.
When: Use when your app has multiple views.
Where: Dashboards, e-commerce, admin panels.

```jsx
<Routes>
  <Route path="/" element={<Home />} />
</Routes>
```

### 6. Callback, HOC, and HOF
Definition: A callback is a passed function, HOF works with functions, and HOC wraps components.
Why: They improve reuse and abstraction.
When: Use callbacks for async/events, HOF/HOC for shared logic.
Where: Utilities, React wrappers, event handlers.

```js
function greet(fn) {
  fn();
}
greet(() => console.log("hello"));
```

### 7. What is DOM and Virtual DOM?
Definition: DOM is the browser tree; Virtual DOM is React's in-memory copy for comparison.
Why: Virtual DOM improves update efficiency.
When: Important when understanding React rendering.
Where: All React UI updates.

```jsx
const element = <h1>Hello</h1>;
```

### 8. `async` / `await`
Definition: `async` makes a function return a promise and `await` pauses until the promise resolves.
Why: It makes async code easier to read.
When: Use in API calls and async workflows.
Where: Frontend and backend JavaScript.

```js
async function load() {
  const res = await fetch("/api/users");
  return res.json();
}
```

### 9. `setTimeout()` and `setInterval()`
Definition: `setTimeout` runs once after a delay; `setInterval` runs repeatedly.
Why: They schedule code execution.
When: Use for timers, polling, delayed UI actions.
Where: Countdowns, animations, alerts.

```js
setTimeout(() => console.log("once"), 1000);
setInterval(() => console.log("repeat"), 2000);
```

### 10. Spread and rest operators
Definition: Spread expands values; rest collects remaining values.
Why: They reduce boilerplate in arrays, objects, and functions.
When: Use for copying, merging, and variable argument functions.
Where: React props, state updates, utility functions.

```js
const a = [1, 2];
const b = [...a, 3];
function sum(...nums) {
  return nums.reduce((x, y) => x + y, 0);
}
```

### 11. Shallow copy and deep copy
Definition: Shallow copy copies only first-level values; deep copy duplicates nested data too.
Why: It avoids unwanted shared references.
When: Use deep copy when nested objects must be fully independent.
Where: State updates and object cloning.

```js
const user = { info: { city: "Delhi" } };
const copy = structuredClone(user);
```

### 12. Code optimization
Definition: Code optimization means improving performance and reducing unnecessary work.
Why: It makes apps faster and more scalable.
When: Use when rendering is slow or data is heavy.
Where: Large lists, API-heavy pages, dashboards.

```jsx
const MemoList = React.memo(List);
```

### 13. API call methods and HTTP methods
Definition: HTTP methods like `GET`, `POST`, `PUT`, and `DELETE` define request type.
Why: They standardize communication with servers.
When: Use the method based on create, read, update, or delete action.
Where: REST APIs and backend integration.

```js
fetch("/api/users", { method: "POST", body: JSON.stringify({ name: "Aslam" }) });
```

### 14. Difference between React JS and React Native
Definition: React JS builds web UIs; React Native builds native mobile apps.
Why: Same React concepts can be used on different platforms.
When: Use React JS for browsers, React Native for Android/iOS.
Where: Web apps and mobile apps.

```jsx
// React JS
<div>Hello</div>

// React Native
<Text>Hello</Text>
```

### 15. Redux and Flux
Definition: Flux is an architecture pattern; Redux is a library inspired by Flux.
Why: Both support one-way data flow.
When: Use Redux when app state grows complex.
Where: Large React applications.

```js
const reducer = (state = 0, action) =>
  action.type === "INC" ? state + 1 : state;
```

### 16. Why does CORS error occur?
Definition: CORS blocks requests between different origins unless the server allows them.
Why: It is a browser security feature.
When: It happens in cross-origin frontend-backend communication.
Where: Localhost frontend calling another domain/API.

```js
fetch("https://api.example.com/data");
```

## Screen 3 Detailed Notes

### 1. Fibonacci series
Definition: In Fibonacci, each number is the sum of the previous two numbers.
Why: It tests loops, recursion, and sequence logic.
When: Asked in basic coding rounds.
Where: JavaScript coding interviews and algorithm practice.

```js
function fibonacci(n) {
  let a = 0, b = 1;
  for (let i = 0; i < n; i++) {
    console.log(a);
    [a, b] = [b, a + b];
  }
}
```

### 2. Factorial
Definition: Factorial of `n` is the product of all integers from `1` to `n`.
Why: It checks loops, recursion, and base conditions.
When: Common beginner coding problem.
Where: Interview coding rounds.

```js
function factorial(n) {
  return n <= 1 ? 1 : n * factorial(n - 1);
}
```

### 3. Prime number
Definition: A prime number has exactly two factors: `1` and itself.
Why: It checks divisor logic and optimization.
When: Common number-based coding question.
Where: JavaScript and DSA interviews.

```js
function isPrime(num) {
  if (num <= 1) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
}
```

### 4. Unique number
Definition: A unique number appears only once in a list.
Why: It tests counting and lookup logic.
When: Use when finding non-repeated values.
Where: Array interview questions.

```js
const arr = [1, 2, 2, 3, 3];
const unique = arr.find((n) => arr.indexOf(n) === arr.lastIndexOf(n));
```

### 5. Count how many repeated elements
Definition: This means finding frequency of duplicate values.
Why: It checks map/object counting skills.
When: Use when data has repeated items.
Where: Arrays, reporting, analytics.

```js
const arr = [1, 2, 2, 3, 3, 3];
const count = arr.reduce((acc, item) => {
  acc[item] = (acc[item] || 0) + 1;
  return acc;
}, {});
```

### 6. Highest second number
Definition: It means finding the second largest distinct value in an array.
Why: It tests comparison logic.
When: Use when ranking values.
Where: Coding interviews and leaderboard logic.

```js
const second = [...new Set([10, 20, 30, 40, 30])].sort((a, b) => b - a)[1];
```

### 7. Palindrome
Definition: A palindrome reads the same forward and backward.
Why: It checks string handling.
When: Use in text validation and coding rounds.
Where: String algorithm questions.

```js
function isPalindrome(str) {
  return str === str.split("").reverse().join("");
}
```

### 8. Generate possibilities / pairs
Definition: It means generating combinations or all possible pairs.
Why: It tests nested loops or recursion.
When: Use when pairing items or generating combinations.
Where: Scheduling, combinations, string problems.

```js
const arr = ["a", "b", "c"];
for (let i = 0; i < arr.length; i++) {
  for (let j = i + 1; j < arr.length; j++) {
    console.log(arr[i], arr[j]);
  }
}
```

### 9. Count vowels
Definition: It means counting `a`, `e`, `i`, `o`, and `u` in a string.
Why: It checks string iteration and conditions.
When: Basic string-processing tasks.
Where: Form input checks and interview questions.

```js
function countVowels(str) {
  return (str.match(/[aeiou]/gi) || []).length;
}
```

### 10. Pattern logic
Definition: Pattern logic means printing shapes like triangles or pyramids.
Why: It tests nested loop understanding.
When: Asked in logic-building rounds.
Where: Coding practice and interviews.

```js
for (let i = 1; i <= 3; i++) {
  console.log("*".repeat(i));
}
```

### 11. Longest substring without repeating characters
Definition: It means finding the maximum-length substring with all unique characters.
Why: It tests sliding window technique.
When: Medium-level string problem.
Where: Coding interviews and algorithm practice.

```js
function longestLength(s) {
  let set = new Set(), left = 0, max = 0;
  for (let right = 0; right < s.length; right++) {
    while (set.has(s[right])) set.delete(s[left++]);
    set.add(s[right]);
    max = Math.max(max, right - left + 1);
  }
  return max;
}
```

### 12. Find subarray in array
Definition: A subarray is a continuous part of an array.
Why: It tests iteration, ranges, and sometimes sliding window.
When: Use for sum, range, and target matching problems.
Where: Array algorithm questions.

```js
const arr = [1, 2, 3, 4];
const sub = arr.slice(1, 3); // [2, 3]
```

### 13. Find missing number in array
Definition: It means finding the number missing from an expected sequence.
Why: It tests math and array reduction.
When: Use when sequence range is known.
Where: Coding interviews and data checks.

```js
function missing(arr, n) {
  return (n * (n + 1)) / 2 - arr.reduce((sum, x) => sum + x, 0);
}
```

### 14. Deep clone
Definition: Deep clone creates a full independent copy, including nested objects.
Why: It prevents accidental mutation of original data.
When: Use before modifying nested structures.
Where: State management and object transformations.

```js
const original = { user: { name: "Aslam" } };
const cloned = structuredClone(original);
```

## Screen 4 Detailed Notes

### 1. Custom hooks
Definition: A custom hook is a reusable function that starts with `use` and contains hook logic.
Why: It helps share logic across components.
When: Use when repeated hook logic appears in multiple components.
Where: Form logic, fetch logic, resize logic.

```jsx
function useCounter() {
  const [count, setCount] = useState(0);
  return { count, setCount };
}
```

### 2. Counter to timer
Definition: It means turning a count value into time-based increment or decrement logic.
Why: It tests interval handling and cleanup.
When: Use for stopwatch and countdown tasks.
Where: Quiz apps, timers, productivity tools.

```js
let count = 0;
setInterval(() => console.log(++count), 1000);
```

### 3. Redux counter
Definition: It is a simple Redux example with increment/decrement actions.
Why: It shows store, reducer, and dispatch basics.
When: Use when learning Redux state flow.
Where: Interview demos and Redux examples.

```js
const reducer = (state = 0, action) =>
  action.type === "INC" ? state + 1 : state;
```

### 4. Progress bar
Definition: A progress bar visually shows task completion percentage.
Why: It improves user feedback.
When: Use in uploads, loaders, and steps.
Where: Forms, downloads, dashboards.

```jsx
<div style={{ width: "200px", border: "1px solid #000" }}>
  <div style={{ width: "60%", background: "green", color: "#fff" }}>60%</div>
</div>
```

### 5. API call with `fetch`
Definition: `fetch` requests data from a server.
Why: It is the standard browser API for network requests.
When: Use to load or send backend data.
Where: User lists, product lists, form submission.

```js
fetch("/api/data")
  .then((res) => res.json())
  .then(console.log);
```

### 6. Color changer
Definition: It changes UI color based on state or user action.
Why: It tests event handling and dynamic styles.
When: Use in theme toggles and UI demos.
Where: Buttons, cards, theme switches.

```jsx
const [color, setColor] = useState("red");
<button style={{ background: color }} onClick={() => setColor("blue")} />;
```

### 7. Filter card
Definition: A filter card displays items and filters them based on a rule.
Why: It checks array filtering and state updates.
When: Use in product or user listing UIs.
Where: E-commerce, dashboards, admin panels.

```js
const filtered = items.filter((item) => item.category === "books");
```

### 8. Generate random color
Definition: It means creating a random RGB or HEX color value.
Why: It tests random number generation and string building.
When: Use in demo apps and styling generators.
Where: Theme demos and UI practice tasks.

```js
const color = "#" + Math.floor(Math.random() * 16777215).toString(16);
```

### 9. Form validation
Definition: Form validation checks if user input is valid before submit.
Why: It avoids bad or incomplete data.
When: Use in all user input forms.
Where: Login, signup, contact, checkout.

```js
if (!email.includes("@")) {
  console.log("Invalid email");
}
```

### 10. Multi-select with all options
Definition: It allows selecting multiple choices, including a select-all action.
Why: It improves bulk selection UX.
When: Use in filters and permission settings.
Where: Admin panels, forms, dashboards.

```js
const allSelected = selected.length === options.length;
```

### 11. Target value from array by index
Definition: It means accessing an item by its position.
Why: Index-based access is basic array usage.
When: Use when position is known.
Where: Lists, tables, loops.

```js
const arr = ["a", "b", "c"];
console.log(arr[1]); // b
```

### 12. Change positions
Definition: It means swapping or reordering array items.
Why: It tests array mutation and destructuring.
When: Use in drag-and-drop or reorder tasks.
Where: Lists, ranking, playlists.

```js
let arr = [1, 2, 3];
[arr[0], arr[2]] = [arr[2], arr[0]];
```

### 13. Negative numbers from array
Definition: It means extracting only numbers less than zero.
Why: It tests filtering logic.
When: Use when categorizing numbers.
Where: Reports, analytics, math logic.

```js
const negatives = [1, -2, 3, -4].filter((n) => n < 0);
```

### 14. Longest substring
Definition: It means finding the longest valid string segment based on a condition.
Why: It tests window logic and string processing.
When: Use in medium-level string questions.
Where: Coding interviews and text analysis.

```js
console.log("abcabcbb".substring(0, 3));
```

## Screen 5 Detailed Notes

### 1. Show / hide text
Definition: It means conditionally displaying content based on state.
Why: It is a common UI interaction pattern.
When: Use in accordions, password toggles, and help text.
Where: Forms, FAQ sections, details panels.

```jsx
const [show, setShow] = useState(false);
{show && <p>Hello</p>}
```

### 2. API call on click
Definition: It means calling an API only after user action instead of on load.
Why: It avoids unnecessary network requests.
When: Use for search, button actions, or manual loading.
Where: Dashboards, user actions, reports.

```jsx
<button onClick={loadUsers}>Load Users</button>
```

### 3. Show list of response in two columns
Definition: It means displaying API data in a two-column layout.
Why: It improves readability and use of screen space.
When: Use when list items should be visually balanced.
Where: Product cards, user cards, gallery grids.

```css
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```

### 4. Dropdown sorting: ascending and descending
Definition: It means sorting data based on dropdown selection.
Why: It gives users control over order.
When: Use in tables, lists, and search results.
Where: Products, scores, names, dates.

```js
const sorted = [...arr].sort((a, b) => a - b);
```

### 5. Filter based on status code
Definition: It means showing records matching a selected status code.
Why: It helps users quickly narrow down results.
When: Use in logs, API data views, and dashboards.
Where: Admin panels and monitoring tools.

```js
const okItems = data.filter((item) => item.status === 200);
```

### 6. 3 input fields with submit button, show data in table, and empty after submit
Definition: It is a form handling task where submitted data is listed and fields reset.
Why: It tests forms, arrays, tables, and controlled components.
When: Use in CRUD basics and form assignments.
Where: Registration forms, admin panels, contact tables.

```jsx
setRows((prev) => [...prev, form]);
setForm({ name: "", email: "", city: "" });
```

### 7. Create counter
Definition: A counter increments or decrements a numeric state.
Why: It is the simplest React state example.
When: Use while learning `useState`.
Where: Demos, quantity controls, simple tools.

```jsx
const [count, setCount] = useState(0);
```

### 8. Create timer with play, stop, and reset
Definition: A timer updates state every interval and supports start/stop/reset controls.
Why: It tests timer cleanup and state control.
When: Use in stopwatch and countdown apps.
Where: Quiz apps, productivity apps, games.

```js
const id = setInterval(() => setTime((t) => t + 1), 1000);
clearInterval(id);
```

### 9. Pagination with limit and make responsive
Definition: Pagination splits data into pages with a fixed item limit.
Why: It improves performance and readability of large lists.
When: Use when many records are shown.
Where: Tables, product lists, blogs.

```js
const start = (page - 1) * limit;
const visible = items.slice(start, start + limit);
```

## Screen 6 Detailed Notes

### 1. What is pure component?
Definition: A Pure Component re-renders only when shallowly compared props or state change.
Why: It reduces unnecessary rendering.
When: Use when props are stable and performance matters.
Where: Large lists and reusable UI blocks.

```jsx
const UserCard = React.memo(function UserCard({ name }) {
  return <p>{name}</p>;
});
```

### 2. What does `key` do in React?
Definition: A `key` gives each list item a stable identity.
Why: It helps React update lists efficiently.
When: Use whenever rendering arrays.
Where: `map()` loops in JSX.

```jsx
items.map((item) => <li key={item.id}>{item.name}</li>);
```

### 3. Error boundaries in React
Definition: Error boundaries catch rendering errors in child components and show fallback UI.
Why: They prevent the whole app from crashing.
When: Use around major feature sections.
Where: Dashboard widgets, routes, risky third-party UI.

```jsx
<ErrorBoundary>
  <Dashboard />
</ErrorBoundary>
```

### 4. Strict mode
Definition: Strict Mode is a React development tool that highlights unsafe patterns.
Why: It helps find bugs early.
When: Use during development.
Where: Root React app wrapper.

```jsx
<React.StrictMode>
  <App />
</React.StrictMode>
```

### 5. Conditional rendering
Definition: Conditional rendering shows different UI based on a condition.
Why: It makes UI dynamic.
When: Use for auth, loading, and error states.
Where: Almost every React application.

```jsx
return isLoggedIn ? <Home /> : <Login />;
```

### 6. What are hooks?
Definition: Hooks are React functions that let function components use state and lifecycle features.
Why: They simplify component logic and reuse.
When: Use in modern function components.
Where: All modern React apps.

```jsx
const [count, setCount] = useState(0);
useEffect(() => console.log(count), [count]);
```

### 7. What is `ref` and `forwardRef`?
Definition: `ref` accesses a DOM node directly; `forwardRef` passes that ref through a component.
Why: It helps with focus, scroll, and integrations.
When: Use for imperative actions.
Where: Inputs, modals, custom components.

```jsx
const inputRef = useRef(null);
inputRef.current.focus();
```

### 8. What is props drilling?
Definition: Props drilling is passing data through many intermediate components just to reach a child.
Why: It can make code harder to maintain.
When: It appears in deeply nested trees.
Where: Large component hierarchies.

```jsx
<Parent user={user} />
```

### 9. ESLint plugin and faulty pattern in React
Definition: ESLint plugins check React code for mistakes and bad patterns.
Why: They improve code quality and consistency.
When: Use during development and CI.
Where: React project linting setup.

```json
{
  "extends": ["plugin:react/recommended", "plugin:react-hooks/recommended"]
}
```

### 10. Redux Thunk and Redux Saga
Definition: Thunk handles async logic with functions; Saga handles async flows with generators.
Why: They manage side effects outside components.
When: Use Thunk for simple async needs, Saga for complex workflows.
Where: Large apps with API-heavy state logic.

```js
const fetchUsers = () => async (dispatch) => {
  const res = await fetch("/api/users");
  dispatch({ type: "SET_USERS", payload: await res.json() });
};
```

### 11. How to create a React app
Definition: It means bootstrapping a new React project with a tool like Vite.
Why: It gives you a ready project setup.
When: Use when starting a new React application.
Where: Any new frontend project.

```bash
npm create vite@latest my-app
cd my-app
npm install
```

### 12. What is JWT?
Definition: JWT is a token format used to securely send user-related claims.
Why: It is commonly used for authentication and authorization.
When: Use when backend returns a signed auth token.
Where: Login systems and protected APIs.

```js
const token = "header.payload.signature";
localStorage.setItem("token", token);
```
