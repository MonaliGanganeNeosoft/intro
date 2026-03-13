# JavaScript Interview Questions

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

## Theory Questions

1. What is the difference between `var`, `let`, and `const`?
2. What is hoisting in JavaScript?
3. What is the temporal dead zone?
4. What is lexical scope?
5. What are closures, and where do you use them in real applications?
6. What is the difference between function declarations, function expressions, and arrow functions?
7. How does `this` work in regular functions versus arrow functions?
8. What is the event loop?
9. What is the difference between microtasks and macrotasks?
10. What is the execution order of `setTimeout`, `Promise`, and synchronous code?
11. What is the difference between `==` and `===`?
12. What is type coercion in JavaScript?
13. What are primitive and reference types?
14. What is the difference between shallow copy and deep copy?
15. How do `map`, `filter`, `reduce`, `find`, and `forEach` differ?
16. What is immutability, and why is it important in frontend development?
17. What are promises, and how do they differ from callbacks?
18. How does `async/await` work internally with promises?
19. What is error handling best practice in async JavaScript?
20. What is debouncing and throttling?
21. What is event delegation, and why is it useful?
22. What is prototype inheritance?
23. What is the difference between `Object.create`, constructor functions, and ES6 classes?
24. How do modules work in JavaScript?
25. What is the difference between CommonJS and ES modules?
26. What are generators, and when would you use them?
27. What is currying?
28. What are pure functions?
29. What are side effects in JavaScript?
30. What is memoization?
31. What is the difference between `call`, `apply`, and `bind`?
32. What are optional chaining and nullish coalescing?
33. How do `Set`, `Map`, `WeakSet`, and `WeakMap` differ?
34. How does garbage collection work at a high level?
35. What is a memory leak in JavaScript, and how can it happen in browser apps?
36. What are common security concerns in frontend JavaScript?
37. What is the difference between synchronous, asynchronous, parallel, and concurrent execution in JS apps?
38. How do browser storage APIs differ?
39. What is the purpose of AbortController?
40. What are common JavaScript interview output-based trap questions testing?

## Coding and Practical Questions

1. Implement a custom `debounce` function.
2. Implement a custom `throttle` function.
3. Write a polyfill for `Array.prototype.map`.
4. Write a polyfill for `Array.prototype.filter`.
5. Write a polyfill for `Array.prototype.reduce`.
6. Flatten a deeply nested array.
7. Deep clone a nested object.
8. Write a function to group an array of objects by a key.
9. Implement a `once` utility function.
10. Create a memoization helper.
11. Implement `Promise.all` in a simplified way.
12. Create a retry wrapper for an async API function.
13. Write a function to cancel a fetch request using AbortController.
14. Build a simple event emitter class.
15. Write a function to detect duplicate values in an array.
16. Sort an array of objects by multiple keys.
17. Convert callback-based code to promise-based code.
18. Write a utility to compare two objects shallowly.
19. Build a pagination helper for frontend data.
20. Create a function that returns unique objects by `id`.
21. Implement currying for a sum function.
22. Write code to print numbers with correct async timing behavior.
23. Solve output-based questions involving closures inside loops.
24. Build a simple LRU cache in JavaScript.
25. Implement event delegation for a list of buttons.

## Accenture L2 Focus Questions

1. Explain the event loop with a real browser example.
2. Why do API calls often move from callbacks to promises to `async/await` in enterprise applications?
3. How do you prevent memory leaks in large single-page applications?
4. How do you debug slow screens caused by repeated re-renders and heavy JavaScript logic?
5. How would you structure reusable utility functions in a production codebase?
6. How do you handle API retries, cancellation, timeout, and fallback states?
7. What JavaScript patterns help maintainability in large teams?
8. How do you avoid race conditions when multiple async requests update the same UI?
9. What is the difference between optimistic updates and confirmed updates?
10. How would you review a teammate's JavaScript for performance, readability, and edge cases?
11. What are common output-based JavaScript questions asked in experienced frontend interviews?
12. How do closures help and hurt in large applications?

## Senior-Level Scenario Questions

1. A search box makes too many API calls while typing. How would you solve it?
2. A page shows stale data because requests return in the wrong order. How would you fix it?
3. Your team has duplicated utility logic across many modules. What refactor would you propose?
4. A component leaks memory after repeated mount and unmount cycles. What JavaScript causes would you investigate?
5. A business-critical screen freezes with large JSON responses. How would you optimize the code path?
