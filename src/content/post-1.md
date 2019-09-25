---
title: "Reverse Words in String"
date: "2019-09-25"
draft: false
path: "/blog/reverse-words-in-string"
---
SOURCE: [DevMates](https://devmates.co/solutions/reverse_words_in_string)

### Problem 
CHALLENGES: Implementing Jest to test code

TODO: [ ] Implement Jest code

Instructions:
Reverse the words of a given string.
You can't use the language provided methods such as (split, reverse, etc.)

```javascript
Input: 'hello this is devmates'
Output: 'olleh siht si setamved'
```

```javascript
function reverseWordsInString(str) {
    let result = '';
    for (let i = 0; i < str.length; i++) {
        // here we should check if it space or not
        // if not then we should iterate over the current word
    }
    return result;
}
```
We can use while state for iterate over the word. Also we are using the same index i, so we will not iterate over the same word twice. If current character is space '' then we sholud add it directly to our result.

```javascript
function reverseWordsInString(str) {
    let result = ''; 
    for (let i = 0; i < str.length; i++) {
        if (str]i] !== ' ') {
            while(str[i] !== '' && i < str.length) {
                // here we can iterate over the current word.
                i++;
            }
        } else {
            result =+ str[i];
        }
    }
    return result;
}

```
let's accumulate our word to tmp variable in reverse order and save it to result.

``````javascript
function reverseWordsInString(str) {
    let result = '';
    for (let i = 0; i < str.length; i++) {
        let tmp = '';
        if (str[i] !== '') {
            while(str[i] !== '' && i < str.length) {
            tmp = str[i] + tmp;
            i++;
        }
        result += tmp + (str[i] ? str[i] : '');
    } else {
        result =+ str[i];
    }
    return result;
}
```