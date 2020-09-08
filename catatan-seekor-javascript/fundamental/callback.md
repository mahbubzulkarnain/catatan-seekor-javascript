# Callback

```javascript
function callFather(message) {
  console.log("Dad! " + message)
}

function callMother(message) {
  console.log("Mom! " + message)
}

function talk(...call) {
  call.forEach((fn) => {
    fn(`I'm hungry...`)
  })
}

talk(callFather, callMother);
/* output
Dad! I'm hungry...
Mom! I'm hungry...
*/
```

