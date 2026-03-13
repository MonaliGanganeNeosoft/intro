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
