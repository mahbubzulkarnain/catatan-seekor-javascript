# [Catatan Seekor: **JAVASCRIPT**](https://github.com/mahbubzulkarnain/catatan-seekor-javascript) / Conditional
##### by Mahbub Zulkarnain

## Table of Contents
* [Type Data](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/type_data.md)
* [Variables](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/variables.md)
* [Function](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/function.md)
* Conditional
* [Looping](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/looping.md)
* [Tips and Tricks](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/tips_and_tricks.md)
* [Links](#links)
* [Forum](#forum)
* [Course](#course)

### Comparison and Logical Operator
```javascript
const conditional = !false // true
```
```javascript
let dataIsNotEmpty = '';
let dataIsNotEmpty = 0;
let dataIsNotEmpty = null;
let dataIsNotEmpty = undefined;

console.log(!dataIsNotEmpty);           // true
console.log(!!dataIsNotEmpty);          // false
console.log(!!!dataIsNotEmpty);         // true
console.log(!!!!!!!!!!dataIsNotEmpty);  // ?
```
```javascript
console.log(0 == 0);                    // true
console.log(0 == '0');                  // true
console.log(0 != '0');                  // false
console.log(true != 'true');            // true
console.log(!(true != 'true'));         // false
```
```javascript
console.log(0 < -1);                    // false
console.log(-1 <= '-1');                // true
console.log(0 > '-2');                  // true
console.log(-1 >= -1);                  // true
console.log(true && !false);            // true
console.log(true || false);             // true
```
```javascript
console.log(0 === 0);                   // true
console.log(0 === '0');                 // false
console.log(0 !== '0');                 // true

console.log(!!+'1337');                 // true
console.log(!+'satu');                  // true
```

### The if Statement
```javascript
const condition = true;
const isTrue = 'text true';

console.log((() => {
  if (condition) return isTrue; 
})()); // 'text true'

console.log((() => {
  return (condition) && isTrue
})()); // 'text true'

console.log((() => {
  return (!condition) || isTrue
})()); // 'text true'
```

### The else Statement
```javascript
const condition = true;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else return isFalse;
})()); // 'text true'

console.log((() => {
  return condition ? isTrue : isFalse
})()); // 'text true'
```

### The else if Statement
```javascript
const condition = true;
const condition2 = false;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else if (condition2) return 'else if true'; 
  else return isFalse;
})()); // 'text true'
```

### The switch case Statement
```javascript
const condition = 1;
const isTrue = 'text true';
const isFalse = 'text false';


console.log((() => {
  let output;
  switch (condition) {
    case 0:
      output = isFalse;
      break;
    case 1:
    case 2:
      output = 'With case 2'
      break;
    default:
      output = "default";
      break;
  }
  return output;
})()); // 'With case 2'
```
