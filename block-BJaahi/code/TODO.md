For the given code below:

- re-write the code in ways that system will understand

For Example:

1.

```js
var username = 'Arya';
let brothers = ['John', 'Ryan', 'Bran'];

console.log(username, brothers[0]);

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Declaration Phase
var username = undefined;
let brothers;

function sayHello(name) {
  return `Hello ${name}`;
}

let message;
var nextMessage = undefined;

// Execution Phase

username = 'Arya';
brothers = ['John', 'Ryan', 'Bran'];

console.log(username, brothers[0]);

message = sayHello(username);
nextMessage = sayHello('Test');
```

2.

```js
console.log(username, number);

var username = 'Arya';
let number = 21;

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Declaration phase 
var username = undefined;
let number ;
function sayHello(name) {
  return `Hello ${name}`;
}
let message ;
var nextMessage = undefined;
//Execution phase
console.log(username, number); //undefined and number is not defined yet 
// Execution stopped here only due to  a Error 
```

3.

```js
console.log(username, numbers);
let username = 'Arya';
let number = 21;

let sayHello = function (name) {
  return `Hello ${name}`;
};

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Declaration  phase start here 
let username;
let number ;
let sayHello;
let message ;
var nextMessage = undefined ;
//Execution phase start here 

console.log(username,numbers);// Error username is not defined yet
//Execution stopped here becuase we are accessing a variable before initializing the variable
```

4.

```js
let username = 'Arya';
console.log(username, numbers);

let number = 21;
let message = sayHello(username);

let sayHello = function (name) {
  return `Hello ${name}`;
};

var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
//Declaration phase start here 

let username;
let number;
let message;
let sayHello;
var nextMessage = undefined;

// Execution phase start here

username = 'Arya';
console.log(username,number);// Error number is not define
//Execution stopped here becuase we are accessing a variable before initializing the variable
```

5.

```js
console.log(name);
console.log(age);
var name = 'Lydia';
let age = 21;
```

<!-- Answer -->

```js
// Declaration phase start here 
var name  = undefined;
let age ;

//Execution phase start here 

console.log(name);//undefined
console.log(age);// age is not defined
//Execution stopped here becuase we are accessing a variable before initializing the variable
```

6.

```js
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}

sayHi();
```

<!-- Answer -->

```js
//Declaration phase start here 
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}
//Execution Phase start here 

sayHi();
// Now function declaration phase start here 
var name  = undefined;
let age ;

//Execution phase start here 
console.log(name);//undefined
console.log(age);// Cannot access 'age' before initialization
// Got an error and Execution stopped here
```

7.

```js
sayHi();
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}
```

<!-- Answer -->

```js
// Declaration phase start here 
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}
// Execution phase start here 
sayHi();
// Now function declaration phase start here 
var name  = undefined;
let age ;

//Execution phase start here 
console.log(name);//undefined
console.log(age);// Cannot access 'age' before initialization
// Got an error and Execution stopped here
```

8.

```js
sayHi();
let sayHi = function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
};
```

<!-- Answer -->

```js
// Declaration phase 
let sayHi;
// Execution phase 
sayHi();// got an error sayHi is not defined
// Executio stopped due to error
```

9.

```js
let num1 = 21;
console.log(sum);
var sum = num1 + num2;
let num2 = 30;
```

<!-- Answer -->

```js
// Declaration phase start here 
let num1;
var sum = undefined;
let num2;
// Execution phase start here 
num1= 21;
console.log(sum);//undefined
sum =// Got an error  num2 is not defined and Execution stopped here 

```

10.

```js
var num1 = 21;

let sum2 = addAgain(num1, num2, 4, 5, 6);

let add = (a, b, c, d, e) => {
  return a + b + c + d + e;
};
function addAgian(a, b) {
  return a + b;
}
let num2 = 200;

let sum = add(num1, num2, 4, 5, 6);
```

<!-- Answer -->

```js
// Declaration phase start here 
var num1 = undefined;
let sum2;
let add;
function addAgian(a, b) {
  return a + b;
}
let num2;
let sum;

// Execution phase start here

num1 = 21;
sum2 = addAgain(num1,num2,4,5,6);// Error num2 is not defined Execution stopped here 

//Execution stopped due to Error


```

11.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

let add = (a, b) => {
  return a + b;
};
```

<!-- Answer -->

```js
// Declaration phase start here 
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let num1 ;
let add;
//Execution phase start here 
sum = test(100); // test function is called 
// now function execution context
// function declaration start here 
a=undefined;
let num1;
// function execution start here
a=100;
num1= 21;
return add(a,num1); // Got an error add is not defined

// Execution stopped here due to an error.
```

12.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

function add(a, b) {
  return a + b;
}
```

<!-- Answer -->

```js
// Declaration phase start here 
function test(a) {
  let num1 = 21;
  return add(a, num1);
}
let sum ;
function add(a, b) {
  return a + b;
}
//Execution phase start here 
sum = test(200); //function test is called here 

// function Execution Context start here 

       // function declaration start here 
       a= undefined;
       let num1;
       // Function Execution start here 
       a=200;
       num1=21;
       return add(a,num); // add function is called here 

       //Function Execution context for add 
         // declaration for function
         a=  undefined;
         b=undefined;
         // execution of add function 
         a= 200 ;
         b=21;
         return a+b; // 200+21 =221;
// 221 is returned as a output 




```
