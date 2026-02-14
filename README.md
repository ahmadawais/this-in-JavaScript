<h1 align="center">
  The Concept of `this` in JavaScript
</h1>

<br><br>


## TL;DR

1. If a function is called with the new keyword, `this` will be the resulting object.
1. If a function is called with `.call()`, `.apply()` or `.bind()`, `this` will be the object that is passed in.
1. If a function is called on an object, `obj.foo()`, `this` will be the object it was called on.
1. If a function is called on its own, `sayMyName()`, `this` will be either `undefined` (if in `use strict;` mode) or the global object (if in non-strict mode).

<br><br>


### Concept #1

If a function is called with the new keyword, `this` will be the resulting object.

```js
let myName = new String('Ahmad Awais');
typeOf(myName); // object <================== this is the resulting object.
```
<br><br>


### Concept #2

If a function is called with `.call()`, `.apply()` or `.bind()`, `this` will be the object that is passed in.

```js
let person = {
  name: "Ahmad Awais"
};

let sayMyName = function() {
  console.log(this.name);
};

sayMyName.call(person); // Ahmad Awais — <================== this is the object that is passed in i.e. person.
```

<br><br>


### Concept #3

If a function is called on an object, `obj.foo()`, `this` will be the object it was called on.

 ```js
 let person = {
  name: "Ahmad Awais",
  sayMyName: function() {
    console.log(this.name);
  }
};

person.sayMyName(); // Ahmad Awais <================== this is the object on which the functions was called i.e. person.
```

<br><br>


### Concept #4

If a function is called on its own, `sayMyName()`, `this` will be either `undefined` (if in `use strict;` mode) or the global object (if in non-strict mode).

```js
"use strict";

let name = "Ahmad Awais";

let sayMyName = function() {
  console.log(this.name);
};

sayMyName(); // undefined <================== this is undefined.
```

<br><br>


### ES6 TIP:
An arrow function expression has a shorter syntax than a function expression and does not have its own `this`.

<br><br>

---


## License & Attribution

MIT © [Ahmad Awais](https://AhmadAwais.com/).

[Kyle Simpson](https://github.com/getify) for his incredible work on [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS) and the good folks at [Icons8](https://icons8.com/).

<br>

