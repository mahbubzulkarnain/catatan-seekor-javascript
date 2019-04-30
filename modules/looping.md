# [Catatan Seekor: **JAVASCRIPT**](https://github.com/mahbubzulkarnain/catatan-seekor-javascript) / Looping
##### by Mahbub Zulkarnain

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
