# Catatan Seekor: **JAVASCRIPT**
##### by Mahbub Zulkarnain

## Type Data

### String
```javascript
iniString = 'Type Data String';
iniString = "Type Data String";
iniString = `Type Data String`;
```
```javascript
console.log(typeof iniString) // string
```

### Number
```javascript
iniNumber = 0;
iniNumber = 0.1;
iniNumber = 1337e1;                  // 13370
iniNumber = 1337e-2;                 // 13.37
iniNumber = Number.MAX_VALUE;        // 1.7976931348623157e+308
iniNumber = Number.MIN_VALUE;        // 5e-324
iniNumber = Number.MAX_SAFE_INTEGER; // 9007199254740991
iniNumber = Number.MIN_SAFE_INTEGER; // -9007199254740991
```
```javascript
console.log(typeof iniNumber); // number
```

### Boolean
```javascript
iniBoolean = true;
iniBoolean = false;
```
```javascript
console.log(typeof iniBoolean); // boolean
```

### Function
```javascript
iniFunction = function() {};
iniFunction = ()=>{};
```
```javascript
console.log(typeof iniFunction); // function
console.log(iniFunction instanceof Function); // true
```

### Array
```javascript
iniArray = [];
```
```javascript
console.log(typeof iniArray); // object
console.log(iniArray instanceof Array); // true
```

### Object
```javascript
iniObject = {};
```
```javascript
console.log(typeof iniObject); // object
console.log(iniObject instanceof Object); // true
```

### Null
```javascript
iniNull = null;
```
```javascript
console.log(typeof iniNull); // object
```

### Undefined
```javascript
iniUndefined = undefined;
```
```javascript
console.log(typeof iniUndefined); // undefined
```


## Variables
### VAR ( Global )
```javascript
var iniVariableGlobal = TYPE_DATA;
```

### LET ( Local )
```javascript
let iniVariableGlobal = TYPE_DATA;
```

### CONST ( Read Only )
```javascript
let iniVariableGlobal = TYPE_DATA;
```

## Assignment Operator
```javascript
a  = 1;              // a = 1;
a += 1;              // a = a + 1;
a -= 1;              // a = a - 1;
a *= 1;              // a = a * 1;
a /= 1;              // a = a / 1;
a %= 1;              // a = a % 1;
```
```javascript
a  = 1 + 1;          //  1  + 1 = 2
b  = a + 1;          // (2) + 1 = 3
c  = a = b = 3;      // c = 3, a = 3, b = 3
d  = a += b /= c;    // ? 
```

## Function
### Declaration
```javascript
// bisa di gunakan sebelum deklarasi function
console.log(iniFunctionDeclaration()); // tampil text ini

// contoh : deklarasi "function declarations"
function iniFunctionDeclaration() {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionDeclaration()); // tampil text ini
```

### Expression
```javascript
// tidak bisa di gunakan sebelum deklarasi function
console.log(iniFunctionDeclaration()); // RefferenceError: iniFunctionDeclaration is not defined

// contoh : deklarasi "function expressions"
var iniFunctionDeclaration = function() {
  return "tampil text ini";
};

// OR

// contoh : deklarasi "function expressions"
var iniFunctionDeclaration = () => {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionDeclaration()); // tampil text ini
```

## Conditional
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
})()) // 'text true'

console.log((()=>{
  return (condition) && isTrue
})()) // 'text true'

console.log((()=>{
  return (!condition) || isTrue
})()) // 'text true'
```

### The else Statement
```javascript
const condition = true;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else return isFalse;
})()) // 'text true'

console.log((()=>{
  return condition ? isTrue : isFalse
})()) // 'text true'
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
})()) // 'text true'
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
})()) // 'With case 2'
```

## Looping
### The for Statement
```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = "";
  for (let i = 0; i < input.length; i++){
    output += input[i];
  } 
  return output
})()) // 'true'
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
})()) // 'true'
```
