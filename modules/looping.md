# [Catatan Seekor: **JAVASCRIPT**](https://github.com/mahbubzulkarnain/catatan-seekor-javascript) / Looping
##### by Mahbub Zulkarnain

## Table of Contents
* [Type Data](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/type_data.md)
* [Variables](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/variables.md)
* [Function](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/function.md)
* [Conditional](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/conditional.md)
* Looping
* [Tips and Tricks](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/tips_and_tricks.md)
* [Links](https://github.com/mahbubzulkarnain/catatan-seekor-javascript#links)
* [Forum](https://github.com/mahbubzulkarnain/catatan-seekor-javascript#forum)
* [Course](https://github.com/mahbubzulkarnain/catatan-seekor-javascript#course)

### The for Statement
```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = "";
  for (let i = 0; i < input.length; i++){
    output += input[i];
  } 
  return output
})()); // 'true'
```

### The while Statement
```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = ""; let i = 0;
  while(i < input.length){
    output += input[i];
    i++;
  } 
  return output
})()); // 'true'
```
