---
title: "countBy"
date: "2019-09-25"
draft: false
path: "/blog/js-countBy"
---
TODO: 
[  ] 

Groups the elements of an array based on the given function and returns the count of elements in each group.

Use 
```javascript 
Array.prototype.reduce()
``` 
to map the values of an array to a function or property name. Use 
```javascript 
Array.prototype.reduce()
```
to create an object, where the keys are produced from the mapped results.

```javascript
const countBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val) => {
    acc[val] = acc[val] || 0) + 1;
  }, {});
```
```javascript
countBy([6.1, 4.2, 6.3], Math.floor); // {4: 1, 6: 2}
countBy(['one', 'two', 'three'], 'length'); // {3: 2, 5: 1}
```

