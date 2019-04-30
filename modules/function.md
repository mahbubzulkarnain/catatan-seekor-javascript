# [Catatan Seekor: **JAVASCRIPT**](https://github.com/mahbubzulkarnain/catatan-seekor-javascript) / Function
##### by Mahbub Zulkarnain

## Table of Contents
* [Type Data](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/type_data.md)
* [Variables](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/variables.md)
* Function
* [Conditional](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/conditional.md)
* [Looping](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/looping.md)
* [Tips and Tricks](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/tips_and_tricks.md)
* [Links](#links)
* [Forum](#forum)
* [Course](#course)

```javascript
function introduction(name) {
  console.log(`Hai, my name is ${ name }.`);
};

introduction('Mahbub'); // 'Hai, my name is Mahbub.'
```
```javascript
function introduction({ firstName, lastName }) {
  console.log(`Hai, my name is ${ firstName } ${ lastName }.`);
};

introduction({firstName: 'Mahbub', lastName: 'Zulkarnain'}); // 'Hai, my name is Mahbub Zulkarnain.'
```
```javascript
function introduction({ name: { firstName, lastName }, hobby }) {
  console.log(`Hai, my name is ${ firstName } ${ lastName }. My favorite hobby is ${ hobby }.`);
};

introduction(
  {
    name: { firstName: 'Mahbub', lastName: 'Zulkarnain' },
    hobby: 'traveling'
  },
); // 'Hai, my name is Mahbub Zulkarnain. My favorite hobby is traveling.'
```

### Declaration
```javascript
// bisa di gunakan sebelum deklarasi function
console.log(iniFunctionDeclaration()); // 'tampil text ini'

// contoh : deklarasi "function declarations"
function iniFunctionDeclaration() {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionDeclaration()); // 'tampil text ini'
```

### Expression
```javascript
// tidak bisa di gunakan sebelum deklarasi function
console.log(iniFunctionExpressions()); // RefferenceError: iniFunctionExpressions is not defined

// contoh : deklarasi "function expressions"
var iniFunctionExpressions = function() {
  return "tampil text ini";
};

// OR

// contoh : deklarasi "function expressions"
var iniFunctionExpressions = () => {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionExpressions()); // 'tampil text ini'
```

### Async/Await
```javascript
async function asyncFunction() {
  return 'ini function async';
}

asyncFunction().then(console.log); // 'ini function async'
```
```javascript
async function asyncFunction() {
  return 'ini function async';
};

(async () => {
  try {
    console.log(await asyncFunction());    
  } catch (e) {
    console.log(e.message);
  }
})(); // 'ini function async'
```
