# Conditional

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

### The _if_ Statement

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

### The _else_ Statement

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

### The _else if_ Statement

```javascript
const condition = false;
const condition2 = true;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else if (condition2) return 'else if true'; 
  else return isFalse;
})()); // 'else if true'

console.log((() => {
  return condition 
  ? isTrue 
  : condition2 
    ? 'else if true'
    : isFalse
})()); // 'else if true'
```

### The _switch case_ Statement

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

### The _try catch finally_ Statement

```javascript
try {
  // tryCode - Block of code to try
}
catch(err) {
  // catchCode - Block of code to handle errors
} 
finally {
  // finallyCode - Block of code to be executed regardless of the try / catch result
}
```

source [https://www.w3schools.com/jsref/jsref\_try\_catch.asp](https://www.w3schools.com/jsref/jsref_try_catch.asp)

```javascript
const isError = true;
let message = '';

try {
  if( isError ) throw 'throw from block try';
  message += 'from block try. ';
}
catch (e) {
  message += `from block catch, with message: "${e}". `;
}
finally {
  message += 'from block finally. ';
}

console.log(message); // from block catch, with message: "throw from block try". from block finally.
```
