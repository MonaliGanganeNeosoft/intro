# JavaScript and React Code Answers

This file contains coding answers for commonly asked JavaScript and React interview questions.

## 1. Reverse a String

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