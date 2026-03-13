# JavaScript and React Code Answers

This file contains coding answers for commonly asked JavaScript and React interview questions.

## 1. Reverse String

### Approach 1: Reverse characters in a string

```js
function reverseString(str) {
  let result = "";

  for (let i = str.length - 1; i >= 0; i--) {
    result += str[i];
  }

  return result;
}

console.log(reverseString("hello how are you"));
// uoy era woh olleh
```

### Approach 2: Reverse words in a sentence

```js
const str = "hello moni how are you";

function reverseWords(sentence) {
  const words = sentence.split(" ");
  let result = "";

  for (let i = words.length - 1; i >= 0; i--) {
    result += words[i] + " ";
  }

  return result.trim();
}

console.log(reverseWords(str));
// you are how moni hello
```

## Notes

1. `reverseString()` reverses all characters.
2. `reverseWords()` reverses the order of words.
3. These are common beginner to medium JavaScript interview questions.

## 2. Built-in Methods

### Approach 3: Reverse characters using built-in methods

```js
function reverseString(str) {
  return str.split("").reverse().join("");
}

console.log(reverseString("hello how are you"));
// uoy era woh olleh
```

### Approach 4: Reverse words using built-in methods

```js
function reverseString(str) {
  return str.split(" ").reverse().join(" ");
}

console.log(reverseString("hello how are you"));
// you are how hello
```

## 3. Check Palindrome String

### Approach 1: Without built-in reverse method

```js
function isPalindrome(str) {
  let reversed = "";

  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }

  return str === reversed;
}

console.log(isPalindrome("madam"));
// true

console.log(isPalindrome("hello"));
// false
```

### Approach 2: Using built-in methods

```js
function isPalindrome(str) {
  return str === str.split("").reverse().join("");
}

console.log(isPalindrome("madam"));
// true

console.log(isPalindrome("hello"));
// false
```

## 4. Find Duplicate Elements in Array

### Approach 1: Without built-in helper methods

```js
function findDuplicates(arr) {
  const duplicates = [];

  for (let i = 0; i < arr.length; i++) {
    let count = 0;

    for (let j = 0; j < arr.length; j++) {
      if (arr[i] === arr[j]) {
        count++;
      }
    }

    let alreadyAdded = false;
    for (let k = 0; k < duplicates.length; k++) {
      if (duplicates[k] === arr[i]) {
        alreadyAdded = true;
        break;
      }
    }

    if (count > 1 && !alreadyAdded) {
      duplicates[duplicates.length] = arr[i];
    }
  }

  return duplicates;
}

console.log(findDuplicates([1, 2, 3, 2, 4, 5, 1]));
// [1, 2]
```

### Approach 2: Using built-in methods

```js
function findDuplicates(arr) {
  return [...new Set(arr.filter((item, index) => arr.indexOf(item) !== index))];
}

console.log(findDuplicates([1, 2, 3, 2, 4, 5, 1]));
// [2, 1]
```

## 5. Remove Duplicates from Array

### Approach 1: Without `Set`

```js
function removeDuplicates(arr) {
  const result = [];

  for (let i = 0; i < arr.length; i++) {
    let exists = false;

    for (let j = 0; j < result.length; j++) {
      if (result[j] === arr[i]) {
        exists = true;
        break;
      }
    }

    if (!exists) {
      result[result.length] = arr[i];
    }
  }

  return result;
}

console.log(removeDuplicates([1, 2, 2, 3, 4, 4, 5]));
// [1, 2, 3, 4, 5]
```

### Approach 2: Using built-in methods

```js
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

console.log(removeDuplicates([1, 2, 2, 3, 4, 4, 5]));
// [1, 2, 3, 4, 5]
```

## 6. Find Second Largest Number in Array

### Approach 1: Without sorting

```js
function secondLargest(arr) {
  let largest = -Infinity;
  let second = -Infinity;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > largest) {
      second = largest;
      largest = arr[i];
    } else if (arr[i] > second && arr[i] !== largest) {
      second = arr[i];
    }
  }

  return second;
}

console.log(secondLargest([10, 5, 8, 20, 15]));
// 15
```

### Approach 2: Using built-in methods

```js
function secondLargest(arr) {
  const unique = [...new Set(arr)];
  unique.sort((a, b) => b - a);
  return unique[1];
}

console.log(secondLargest([10, 5, 8, 20, 15]));
// 15
```

## 7. Flatten Nested Array

### Approach 1: Without built-in `flat()`

```js
function flattenArray(arr) {
  let result = [];

  for (let i = 0; i < arr.length; i++) {
    if (Array.isArray(arr[i])) {
      result = result.concat(flattenArray(arr[i]));
    } else {
      result[result.length] = arr[i];
    }
  }

  return result;
}

console.log(flattenArray([1, [2, [3, 4], 5], 6]));
// [1, 2, 3, 4, 5, 6]
```

### Approach 2: Using built-in methods

```js
function flattenArray(arr) {
  return arr.flat(Infinity);
}

console.log(flattenArray([1, [2, [3, 4], 5], 6]));
// [1, 2, 3, 4, 5, 6]
```

## 8. Debounce Function Implementation

### Approach

```js
function debounce(func, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => {
      func.apply(this, args);
    }, delay);
  };
}

function search(value) {
  console.log("Searching:", value);
}

const debouncedSearch = debounce(search, 500);
debouncedSearch("r");
debouncedSearch("re");
debouncedSearch("react");
// Output after delay:
// Searching: react
```

## 9. Throttle Function Implementation

### Approach

```js
function throttle(func, delay) {
  let lastCall = 0;

  return function (...args) {
    const now = Date.now();

    if (now - lastCall >= delay) {
      lastCall = now;
      func.apply(this, args);
    }
  };
}

function logMessage(message) {
  console.log(message);
}

const throttledLog = throttle(logMessage, 1000);
throttledLog("call 1");
throttledLog("call 2");
// Output:
// call 1
```

## 10. Group Array Objects by Property

### Approach 1: Without `reduce`

```js
function groupBy(arr, key) {
  const result = {};

  for (let i = 0; i < arr.length; i++) {
    const groupKey = arr[i][key];

    if (!result[groupKey]) {
      result[groupKey] = [];
    }

    result[groupKey].push(arr[i]);
  }

  return result;
}

const users = [
  { name: "A", role: "admin" },
  { name: "B", role: "user" },
  { name: "C", role: "admin" }
];

console.log(groupBy(users, "role"));
// { admin: [{...}, {...}], user: [{...}] }
```

### Approach 2: Using `reduce`

```js
function groupBy(arr, key) {
  return arr.reduce((acc, item) => {
    const groupKey = item[key];
    if (!acc[groupKey]) {
      acc[groupKey] = [];
    }
    acc[groupKey].push(item);
    return acc;
  }, {});
}

console.log(groupBy(users, "role"));
// { admin: [{...}, {...}], user: [{...}] }
```

## 11. Count Frequency of Elements in Array

### Approach 1: Using loop

```js
function countFrequency(arr) {
  const result = {};

  for (let i = 0; i < arr.length; i++) {
    const value = arr[i];

    if (result[value]) {
      result[value]++;
    } else {
      result[value] = 1;
    }
  }

  return result;
}

console.log(countFrequency([1, 2, 2, 3, 1, 1, 4]));
// { 1: 3, 2: 2, 3: 1, 4: 1 }
```

### Approach 2: Using `reduce`

```js
function countFrequency(arr) {
  return arr.reduce((acc, item) => {
    acc[item] = (acc[item] || 0) + 1;
    return acc;
  }, {});
}

console.log(countFrequency([1, 2, 2, 3, 1, 1, 4]));
// { 1: 3, 2: 2, 3: 1, 4: 1 }
```

## 12. Find Missing Number in Array

### Approach 1: Sum formula

```js
function findMissingNumber(arr, n) {
  let expectedSum = (n * (n + 1)) / 2;
  let actualSum = 0;

  for (let i = 0; i < arr.length; i++) {
    actualSum += arr[i];
  }

  return expectedSum - actualSum;
}

console.log(findMissingNumber([1, 2, 3, 5], 5));
// 4
```

### Approach 2: Using built-in methods

```js
function findMissingNumber(arr, n) {
  const actualSum = arr.reduce((sum, num) => sum + num, 0);
  const expectedSum = (n * (n + 1)) / 2;
  return expectedSum - actualSum;
}

console.log(findMissingNumber([1, 2, 3, 5], 5));
// 4
```

## 13. Sort Array Without Using `.sort()`

### Approach 1: Bubble sort

```js
function bubbleSort(arr) {
  const result = [...arr];

  for (let i = 0; i < result.length; i++) {
    for (let j = 0; j < result.length - 1 - i; j++) {
      if (result[j] > result[j + 1]) {
        const temp = result[j];
        result[j] = result[j + 1];
        result[j + 1] = temp;
      }
    }
  }

  return result;
}

console.log(bubbleSort([5, 3, 8, 1, 2]));
// [1, 2, 3, 5, 8]
```

### Approach 2: Descending bubble sort

```js
function bubbleSortDescending(arr) {
  const result = [...arr];

  for (let i = 0; i < result.length; i++) {
    for (let j = 0; j < result.length - 1 - i; j++) {
      if (result[j] < result[j + 1]) {
        const temp = result[j];
        result[j] = result[j + 1];
        result[j + 1] = temp;
      }
    }
  }

  return result;
}

console.log(bubbleSortDescending([5, 3, 8, 1, 2]));
// [8, 5, 3, 2, 1]
```

## 14. Implement `Promise.all`

### Approach

```js
function myPromiseAll(promises) {
  return new Promise((resolve, reject) => {
    const results = [];
    let completed = 0;

    if (promises.length === 0) {
      resolve([]);
      return;
    }

    for (let i = 0; i < promises.length; i++) {
      Promise.resolve(promises[i])
        .then((value) => {
          results[i] = value;
          completed++;

          if (completed === promises.length) {
            resolve(results);
          }
        })
        .catch((error) => {
          reject(error);
        });
    }
  });
}

myPromiseAll([
  Promise.resolve("A"),
  Promise.resolve("B"),
  Promise.resolve("C")
]).then((result) => console.log(result));
// ["A", "B", "C"]
```

## 15. Implement Deep Clone

### Approach 1: Recursive deep clone

```js
function deepClone(value) {
  if (value === null || typeof value !== "object") {
    return value;
  }

  if (Array.isArray(value)) {
    const arr = [];

    for (let i = 0; i < value.length; i++) {
      arr[i] = deepClone(value[i]);
    }

    return arr;
  }

  const result = {};

  for (const key in value) {
    result[key] = deepClone(value[key]);
  }

  return result;
}

const user = { name: "Asha", address: { city: "Pune" } };
const copiedUser = deepClone(user);
copiedUser.address.city = "Delhi";

console.log(user.address.city);
// Pune
```

### Approach 2: Using built-in method

```js
const user = { name: "Asha", address: { city: "Pune" } };
const copiedUser = structuredClone(user);
copiedUser.address.city = "Delhi";

console.log(user.address.city);
// Pune
```

## 16. Implement Memoization

### Approach

```js
function memoize(fn) {
  const cache = {};

  return function (...args) {
    const key = JSON.stringify(args);

    if (cache[key] !== undefined) {
      return cache[key];
    }

    const result = fn(...args);
    cache[key] = result;
    return result;
  };
}

function add(a, b) {
  console.log("Calculating...");
  return a + b;
}

const memoizedAdd = memoize(add);

console.log(memoizedAdd(2, 3));
// Calculating...
// 5

console.log(memoizedAdd(2, 3));
// 5
```

## 17. Polyfill for `map`

### Approach

```js
Array.prototype.myMap = function (callback) {
  const result = [];

  for (let i = 0; i < this.length; i++) {
    result[result.length] = callback(this[i], i, this);
  }

  return result;
};

const nums = [1, 2, 3];
console.log(nums.myMap((num) => num * 2));
// [2, 4, 6]
```

## 18. Polyfill for `filter`

### Approach

```js
Array.prototype.myFilter = function (callback) {
  const result = [];

  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      result[result.length] = this[i];
    }
  }

  return result;
};

const nums = [1, 2, 3, 4, 5];
console.log(nums.myFilter((num) => num % 2 === 0));
// [2, 4]
```

## 19. Polyfill for `reduce`

### Approach

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

const nums = [1, 2, 3, 4];
console.log(nums.myReduce((sum, num) => sum + num, 0));
// 10
```

## 20. Event Emitter Implementation

### Approach

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(eventName, listener) {
    if (!this.events[eventName]) {
      this.events[eventName] = [];
    }

    this.events[eventName].push(listener);
  }

  emit(eventName, ...args) {
    if (this.events[eventName]) {
      for (let i = 0; i < this.events[eventName].length; i++) {
        this.events[eventName][i](...args);
      }
    }
  }

  off(eventName, listenerToRemove) {
    if (!this.events[eventName]) return;

    this.events[eventName] = this.events[eventName].filter(
      (listener) => listener !== listenerToRemove
    );
  }
}

const emitter = new EventEmitter();

function greet(name) {
  console.log("Hello", name);
}

emitter.on("welcome", greet);
emitter.emit("welcome", "Moni");
// Hello Moni
```

## 21. Implement LRU Cache

### Approach

```js
class LRUCache {
  constructor(limit) {
    this.limit = limit;
    this.cache = new Map();
  }

  get(key) {
    if (!this.cache.has(key)) {
      return -1;
    }

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

const lru = new LRUCache(2);
lru.put(1, "A");
lru.put(2, "B");
console.log(lru.get(1));
// A

lru.put(3, "C");
console.log(lru.get(2));
// -1
```

## 22. Advanced JavaScript Detailed Notes

### 1. Implement `Promise.all`

#### Idea

1. Accept an array of promises.
2. Resolve when all promises resolve.
3. Reject if any promise rejects.

```js
function promiseAll(promises) {
  return new Promise((resolve, reject) => {
    let results = [];
    let completed = 0;

    promises.forEach((promise, index) => {
      Promise.resolve(promise)
        .then((data) => {
          results[index] = data;
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

#### Usage

```js
promiseAll([
  Promise.resolve(1),
  Promise.resolve(2),
  Promise.resolve(3)
]).then(console.log);
```

#### Output

```js
[1, 2, 3];
```

### 2. Implement Deep Clone

#### Handles

1. Objects
2. Arrays
3. Nested values

```js
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") {
    return obj;
  }

  if (Array.isArray(obj)) {
    return obj.map((item) => deepClone(item));
  }

  let clone = {};

  for (let key in obj) {
    clone[key] = deepClone(obj[key]);
  }

  return clone;
}
```

#### Example

```js
let obj = {
  name: "Monali",
  address: {
    city: "Pune"
  }
};

let copy = deepClone(obj);
copy.address.city = "Mumbai";

console.log(obj.address.city);
```

#### Output

```js
"Pune";
```

### 3. Implement Memoization

#### Idea

Cache results of expensive functions.

```js
function memoize(fn) {
  let cache = {};

  return function (...args) {
    let key = JSON.stringify(args);

    if (cache[key]) {
      return cache[key];
    }

    let result = fn(...args);
    cache[key] = result;

    return result;
  };
}
```

#### Example

```js
function add(a, b) {
  console.log("calculating...");
  return a + b;
}

let memoAdd = memoize(add);

console.log(memoAdd(2, 3));
console.log(memoAdd(2, 3));
```

#### Output

```js
// calculating...
5
5
```

Second call comes from cache.

### 4. Polyfill for `map`

```js
Array.prototype.myMap = function (callback) {
  let result = [];

  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
  }

  return result;
};
```

#### Example

```js
let arr = [1, 2, 3];

let res = arr.myMap((x) => x * 2);

console.log(res);
```

#### Output

```js
[2, 4, 6];
```

### 5. Polyfill for `filter`

```js
Array.prototype.myFilter = function (callback) {
  let result = [];

  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      result.push(this[i]);
    }
  }

  return result;
};
```

#### Example

```js
console.log([1, 2, 3, 4].myFilter((x) => x % 2 === 0));
```

#### Output

```js
[2, 4];
```

### 6. Polyfill for `reduce`

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

#### Example

```js
console.log([1, 2, 3, 4].myReduce((sum, num) => sum + num, 0));
```

#### Output

```js
10;
```

### 7. Event Emitter Implementation

Used in Node.js and React libraries.

```js
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(event, listener) {
    if (!this.events[event]) {
      this.events[event] = [];
    }

    this.events[event].push(listener);
  }

  emit(event, ...args) {
    if (this.events[event]) {
      this.events[event].forEach((fn) => fn(...args));
    }
  }

  off(event, listener) {
    if (this.events[event]) {
      this.events[event] = this.events[event].filter((fn) => fn !== listener);
    }
  }
}
```

#### Usage

```js
const emitter = new EventEmitter();

function greet(name) {
  console.log("Hello", name);
}

emitter.on("greet", greet);
emitter.emit("greet", "Monali");
```

#### Output

```js
// Hello Monali
```

### 8. LRU Cache Implementation

Used in system design interviews.

```js
class LRUCache {
  constructor(limit) {
    this.limit = limit;
    this.cache = new Map();
  }

  get(key) {
    if (!this.cache.has(key)) return -1;

    let value = this.cache.get(key);

    this.cache.delete(key);
    this.cache.set(key, value);

    return value;
  }

  put(key, value) {
    if (this.cache.has(key)) {
      this.cache.delete(key);
    }

    this.cache.set(key, value);

    if (this.cache.size > this.limit) {
      let firstKey = this.cache.keys().next().value;
      this.cache.delete(firstKey);
    }
  }
}
```

#### Usage

```js
let cache = new LRUCache(2);

cache.put(1, 10);
cache.put(2, 20);

cache.get(1);

cache.put(3, 30);

console.log(cache.get(2));
```

#### Output

```js
-1;
```

Because key `2` was least recently used.

## 23. Frequently Asked Hard JavaScript Questions

These are very frequently asked in React interviews:

1. `Promise.allSettled` polyfill
2. Debounce vs Throttle implementation
3. Virtual DOM implementation
4. Flatten object
5. Curry function
6. Retry promise with delay
7. Implement `setInterval` using `setTimeout`
8. Implement `bind`, `call`, and `apply`

## 24. `Promise.allSettled` Polyfill

### Idea

1. Accept an array of promises.
2. Wait for all of them to finish.
3. Return both fulfilled and rejected results.

```js
function myPromiseAllSettled(promises) {
  return new Promise((resolve) => {
    const results = [];
    let completed = 0;

    if (promises.length === 0) {
      resolve([]);
      return;
    }

    promises.forEach((promise, index) => {
      Promise.resolve(promise)
        .then((value) => {
          results[index] = { status: "fulfilled", value };
        })
        .catch((reason) => {
          results[index] = { status: "rejected", reason };
        })
        .finally(() => {
          completed++;
          if (completed === promises.length) {
            resolve(results);
          }
        });
    });
  });
}
```

### Example

```js
myPromiseAllSettled([
  Promise.resolve("A"),
  Promise.reject("Error"),
  Promise.resolve("C")
]).then(console.log);
```

### Output

```js
[
  { status: "fulfilled", value: "A" },
  { status: "rejected", reason: "Error" },
  { status: "fulfilled", value: "C" }
];
```

## 25. Debounce vs Throttle Implementation

### Debounce

Used when you want to call a function only after the user stops triggering the event.

```js
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}

const debounced = debounce((value) => {
  console.log("Debounce:", value);
}, 500);

debounced("h");
debounced("he");
debounced("hello");
// Output after delay:
// Debounce: hello
```

### Throttle

Used when you want to limit how often a function runs.

```js
function throttle(fn, delay) {
  let allowCall = true;

  return function (...args) {
    if (!allowCall) return;

    fn.apply(this, args);
    allowCall = false;

    setTimeout(() => {
      allowCall = true;
    }, delay);
  };
}

const throttled = throttle((value) => {
  console.log("Throttle:", value);
}, 1000);

throttled("scroll 1");
throttled("scroll 2");
// Output:
// Throttle: scroll 1
```

## 26. Virtual DOM Implementation

### Idea

Virtual DOM is a JavaScript object representation of UI.

```js
function createElement(type, props, ...children) {
  return {
    type,
    props: props || {},
    children
  };
}

const virtualDom = createElement(
  "div",
  { id: "app" },
  createElement("h1", null, "Hello World"),
  createElement("p", null, "This is virtual DOM")
);

console.log(virtualDom);
```

### Output

```js
{
  type: "div",
  props: { id: "app" },
  children: [
    { type: "h1", props: {}, children: ["Hello World"] },
    { type: "p", props: {}, children: ["This is virtual DOM"] }
  ]
}
```

## 27. Flatten Object

### Idea

Convert nested object into a single-level object.

```js
function flattenObject(obj, parentKey = "", result = {}) {
  for (let key in obj) {
    const newKey = parentKey ? `${parentKey}.${key}` : key;

    if (typeof obj[key] === "object" && obj[key] !== null && !Array.isArray(obj[key])) {
      flattenObject(obj[key], newKey, result);
    } else {
      result[newKey] = obj[key];
    }
  }

  return result;
}

const user = {
  name: "Monali",
  address: {
    city: "Pune",
    pin: 411001
  }
};

console.log(flattenObject(user));
```

### Output

```js
{
  name: "Monali",
  "address.city": "Pune",
  "address.pin": 411001
}
```

## 28. Curry Function

### Idea

Convert a function with multiple arguments into nested functions.

```js
function curryAdd(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}

console.log(curryAdd(1)(2)(3));
```

### Output

```js
6;
```

## 29. Retry Promise With Delay

### Idea

Retry an async function if it fails.

```js
function retryPromise(fn, retries, delay) {
  return new Promise((resolve, reject) => {
    function attempt(remaining) {
      fn()
        .then(resolve)
        .catch((error) => {
          if (remaining === 0) {
            reject(error);
          } else {
            setTimeout(() => attempt(remaining - 1), delay);
          }
        });
    }

    attempt(retries);
  });
}
```

### Example

```js
let count = 0;

function testApi() {
  return new Promise((resolve, reject) => {
    count++;
    if (count < 3) {
      reject("Failed");
    } else {
      resolve("Success");
    }
  });
}

retryPromise(testApi, 3, 1000)
  .then(console.log)
  .catch(console.error);
```

### Output

```js
"Success";
```

## 30. Implement `setInterval` Using `setTimeout`

### Idea

Call a function repeatedly using recursive `setTimeout`.

```js
function mySetInterval(callback, delay) {
  let timerId;

  function run() {
    timerId = setTimeout(() => {
      callback();
      run();
    }, delay);
  }

  run();

  return function clearMyInterval() {
    clearTimeout(timerId);
  };
}
```

### Example

```js
const stop = mySetInterval(() => {
  console.log("Hello");
}, 1000);

setTimeout(() => {
  stop();
}, 3500);
```

### Output

```js
// Hello
// Hello
// Hello
```

## 31. Implement `bind`, `call`, and `apply`

### `call`

Calls a function immediately with a given `this` value.

```js
function introduce(city) {
  console.log(this.name, city);
}

const user = { name: "Monali" };
introduce.call(user, "Pune");
// Monali Pune
```

### `apply`

Same as `call`, but arguments are passed as an array.

```js
function introduce(city, country) {
  console.log(this.name, city, country);
}

const user = { name: "Monali" };
introduce.apply(user, ["Pune", "India"]);
// Monali Pune India
```

### `bind`

Returns a new function with fixed `this`.

```js
function introduce(city) {
  console.log(this.name, city);
}

const user = { name: "Monali" };
const boundFn = introduce.bind(user);

boundFn("Mumbai");
// Monali Mumbai
```
