Find the output of the code snippets below:

```js
console.log(numA + numB); // NaN becuase we are accessing  the variable  before assigning some value to them
var numA = 21,
  numB = 30;
```

Find the output of the code snippets below:

```js
console.log(numA + numB); //numA is not defined  // because  we are  accessing before we  are initializing some value to a
// becuase in Execution phase it will first logs then initialize the variable with some value
let numA = 21,
  numB = 30;
```

Find the output of the code snippets below:

```js
let numA = 21,
  numB = 30;
console.log(numA + numB); //51
// In declaration phase it will declare the variables and in execution phase first it will initialize the variable then logs the 
// sum of numA + numB
```

Find the output of the code snippets below:

```js
console.log(sayHello()); // Hello
function sayHello() {
  console.log("Hey");
}
function sayHello() {
  console.log("Hello");
}
// in  the above code we are logging the sayHello() function  get the output 
// but here we have redeclared function sayHello function so the output is  Hello
```

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // Tyrion
function sayHello() {
  console.log(username);
}
// in this code we have defined a global variable and also a function sayHello()
// in the sayHello function we are printing the global variable usename  but we are accessing the function before its declaration
// but as we know we during  the  declaration phase function a function has  completely its definition also so that,s why we have 
// output tyrion in the execution phase
```

Find the output of the code snippets below:

```js
sayHello(); // username is not defined
let username = "Tyrion";
function sayHello() {
  console.log(username);
}
```

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); //  'sayHello' is not defined
let sayHello = () => { 
  console.log(username);
};

// this is becuase say hello is a arrow function or function expression and we can not acess a function expression before initialization like function declaration
```

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
let username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
// this is becuase say hello is a arrow function or function expression and we can not acess a function expression before initialization like function declaration
```

Find the output of the code snippets below:

```js
sayHello(); //sayHello is not defined
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
// this is becuase say hello is a arrow function or function expression and we can not acess a function expression before initialization like function declaration
```

Find the output of the code snippets below:

```js
var username = "Tyrion";
sayHello(); // sayHello is not defined
let sayHello = () => {
  console.log(username);
};
// this is becuase say hello is a arrow function or function expression and we can not acess a function expression before initialization like function declaration
```

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  var username = "John";
};
sayHello(); "John"
// we get jhon because we  are redeclaring the variable again inside the sayHello function so we  get John
```

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  var username = "John";
  console.log(username); 
};
sayHello(); // john
// we get jhon because we  are redeclaring the variable again inside the sayHello function so we  get John
```

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  let username = "John"; 
};
sayHello(); // Cannot access 'username' before initialization
```