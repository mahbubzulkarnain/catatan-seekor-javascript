# Classes

```javascript
class Introduction {
  constructor(name) {
    console.log(`Hai, my name is ${name}.`);
  };
}
new Introduction('Mahbub'); // 'Hai, my name is Mahbub.'
```

```javascript
class Person {
  constructor({name: {firstName, lastName}, hobby}) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.hobby = hobby;
  };

  say() {
    console.log(`Hai, my name is ${this.firstName} ${this.lastName}. My favorite hobby is ${this.hobby}.`);
  };
}

const person = new Person({
  name: { firstName: 'Mahbub', lastName: 'Zulkarnain' },
  hobby: 'traveling'
});

person.say(); // 'Hai, my name is Mahbub Zulkarnain. My favorite hobby is traveling.'
```

```javascript
class Person {
  static say() {
    console.log(`Hai, my name is ${this.firstName} ${this.lastName}. My favorite hobby is ${this.hobby}.`);
  };
}

Person.say({
  name: { firstName: 'Mahbub', lastName: 'Zulkarnain' },
  hobby: 'traveling'
}); // 'Hai, my name is Mahbub Zulkarnain. My favorite hobby is traveling.'
```
