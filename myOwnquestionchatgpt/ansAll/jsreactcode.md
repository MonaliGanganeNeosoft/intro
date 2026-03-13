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
