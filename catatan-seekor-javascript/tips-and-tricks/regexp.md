# RegExp

```javascript
// validation email
const email = /(^[a-zA-Z][a-zA-Z0-9._]+[a-zA-Z0-9])@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
console.log(email.test('mahbubzulkarnain@domain.com')); // true
```

```javascript
// validation password
// Min 6 characters which contain at least one numeric digit, one uppercase letter, one lowercase letter, and one special character
const password = /^(?=.*\d)(?=.*[A-Z])(?=.*[a-z])(?=.*[^a-zA-Z0-9])(?!.*\s).{6,}$/;
console.log(password.test('Mahbub!23')); // true
```

```javascript
// validation url
const url = /^(http:\/\/www\.|https:\/\/www\.|http:\/\/|https:\/\/)?[a-z0-9]+([-.]{1}[a-z0-9]+)*\.[a-z]{2,5}(:[0-9]{1,5})?(\/.*)?$/;
console.log(url.test('https://github.com/mahbubzulkarnain')); // true
```

```javascript
// validation username
const username = /(^[a-zA-Z][a-zA-Z0-9._]+[a-zA-Z0-9]).{6,}$/g;
console.log(username.test('mahbubzulkarnain')); // true
```

