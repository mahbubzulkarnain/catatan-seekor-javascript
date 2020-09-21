# Looping

## The _for_ Statement

```javascript
let input = ['t','','r','','u','','e','1','2'];

console.log((() => {
  let output = "";
  for (let i = 0; i < input.length; i++){
    if( input[i] === '') continue;
    if( output.length > 3) break;
    output += input[i];
  } 
  return output
})()); // 'true'
```

## The _while_ Statement

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

## The _do while_ Statement

```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = ""; let i = 0;
  do {
    output += input[i];
    i++;
  } while(i < input.length) 
  return output
})()); // 'true'
```

