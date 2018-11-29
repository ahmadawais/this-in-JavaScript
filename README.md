<h1 align="center">
<img src="https://on.ahmda.ws/ouIP/c">
<br><br>

  The Concept of `this` in JavaScript
</h1>

<br><br>

![image](https://on.ahmda.ws/ou4S/c)

## TL;DR

1. If a function is called with the new keyword, `this` will be the resulting object.
1. If a function is called with `.call()`, `.apply()` or `.bind()`, `this` will be the object that is passed in.
1. If a function is called on an object, `obj.foo()`, `this` will be the object it was called on.
1. If a function is called on its own, `sayMyName()`, `this` will be either `undefined` (if in `use strict;` mode) or the global object (if in non-strict mode).

<br><br>

![image](https://on.ahmda.ws/ouTw/c)

### Concept #1

If a function is called with the new keyword, `this` will be the resulting object.

```js
let myName = new String('Ahmad Awais');
typeOf(myName); // object <================== this is the resulting object.
```
<br><br>

![image](https://on.ahmda.ws/ouBd/c)

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

![Img](https://on.ahmda.ws/ouNb/c)

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

![image](https://on.ahmda.ws/ouRL/c)

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

![image](https://on.ahmda.ws/ou7U/c)

### ES6 TIP:
An arrow function expression has a shorter syntax than a function expression and does not have its own `this`.

<br><br>

---

![image](https://on.ahmda.ws/ou71/c)

## License & Attribution

MIT © [Ahmad Awais](https://AhmadAwais.com/).

[Kyle Simpson](https://github.com/getify) for his incredible work on [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS) and the good folks at [Icons8](https://icons8.com/).

<table width='100%' align="center">
    <tr>
        <td align='left' width='100%' colspan='2'>
            <strong>The Concept of `this` in JavaScript</strong><br />
            🔰 Learn the concept of `this` in JavaScript! — [five simple concepts].
        </td>
    </tr>
    <tr>
        <td>
            A FOSS (Free & Open Source Software) project developed by <a href='https://github.com/ahmadawais'>Ahmad Awais</a>.
        </td>
        <td align='center'>
            <a href='https://AhmadAwais.com/'>
                <img src='https://i.imgur.com/Asg4d3k.png' width='100' />
            </a>
        </td>
    </tr>
    <tr><td><sup> Follow Ahmad's #FOSS work on GitHub <a href='https://github.com/ahmadawais'>@AhmadAwais</a> —   Say Hi on Twitter <a href="https://twitter.com/mrahmadawais/">@MrAhmadAwais</a></sup></td><td  align='center'>👋</td></tr>
</table>
<br>

![Hello](https://on.ahmda.ws/ouK5/c)

#### **Hello, we're the [WordPress Couple](https://WPCouple.com)**!

I ([Ahmad Awais](https://twitter.com/mrahmadawais/)) am a Full Stack Web Developer and a regular core contributor at WordPress. My significant other ([Maedah Batool](https://twitter.com/MaedahBatool/)) is a Technical Project Manager, and she's also a WordPress Core Contributor. Together with our [team](https://WPCouple.com/team), we run the [WPCouple.com](https://WPCouple.com/).

If you'd like to get insights into our love for open source software, professional full stack development, WordPress community, the growth of JavaScript or growing a family, building, and bootstrapping a business, then subscribe to our premium newsletter called ↣ [The WordPress Takeaway](https://WPTakeaway.club)!


<br>

![Partners](https://on.ahmda.ws/ou6K/c)

#### Project Backers & [WPCouple Partners](https://WPCouple.com/partners) ⚡️

This FOSS (free and open source software) project is updated and maintained with the help of awesome businesses listed below.

— _What/How? [Read more about it →](https://WPCouple.com/partners)_

<table width='100%'>
	<tr>
		<td width='333.33'><a target='_blank' href='https://www.gravityforms.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtrE/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://kinsta.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mu5O/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://wpengine.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mto3/c' /></a></td>
	</tr>
	<tr>
		<td width='333.33'><a target='_blank' href='https://www.sitelock.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtyZ/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://wp-rocket.me/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtrv/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://blogvault.net/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtph/c' /></a></td>
	</tr>
	<tr>
		<td width='333.33'><a target='_blank' href='https://cridio.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtmy/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://wecobble.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtrW/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://www.cloudways.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mu0C/c' /></a></td>
	</tr>
	<tr>
		<td width='333.33'><a target='_blank' href='https://www.cozmoslabs.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mu9W/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://wpgeodirectory.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtwv/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://www.wpsecurityauditlog.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtkh/c' /></a></td>
	</tr>
	<tr>
		<td width='333.33'><a target='_blank' href='https://mythemeshop.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/n3ug/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://www.liquidweb.com/?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mtnt/c' /></a></td>
		<td width='333.33'><a target='_blank' href='https://WPCouple.com/contact?utm_source=WPCouple&utm_medium=Partner'><img src='https://on.ahmda.ws/mu3F/c' /></a></td>
	</tr>
</table>

<br>
