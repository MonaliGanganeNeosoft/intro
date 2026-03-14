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
