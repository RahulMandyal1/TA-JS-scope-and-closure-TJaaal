## Understanding Scope and the difference between var, let and const

Watch this video before doing the exercise: https://www.youtube.com/watch?v=XgSjoHgy3Rk

1. Guess the output:

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

console.log(
  window.firstName,// undefined
  window.lastName,//undefined
  window.knownAs//'no one'
);
```

2. Guess the output:

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

function fullName(a, b) {
  return a + b;
}

console.log(window.fullName(firstName, lastName));//AryaStark
```

3. Make a Execution Context Diagram for the following JS and write the output.

```js
fucntion addOne(num){
  return num + 1;
}
var one = addOne(0);
var two = addOne(1);
console.log(one, two);// 1 2
```

4. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
fucntion addOne(num){
  return num + 1;
}
var two = addOne(1);
console.log(one, two);//1 2
```

5. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0)); //1
fucntion addOne(num){
  return num + 1;
}
var two = addOne(1);
console.log(two); //2
```

6. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);//error addOne is not Defined yet
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

7. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0));//error addOne is not Defined yet
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

8. What will be the output of the following

```js
function isAwesome() {
  var awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome();//undefined function with no return type  and aweosme value remain undefined becuase if block 
// does not execute in this case 
```

9. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (true) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome();
// true
```

10. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome(); // awesome not  defined
```

11. What will be the output of the following

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

function fullName(a, b) {
  return a + b;
}
const name = fullName(firstName, lastName);
console.log(name);//AryaStark
```

12. Guess the output of the code below with a reason.

```js
function sayHello() {
  let name = 'Arya Stark';
}
sayHello();

console.log(name);// name is not defined
```

13. Guess the output of the code below with a reason.

```js
if (true) {
  var name = 'Arya Stark';
}
console.log(name); // Arya Stark becuase var is not block scoped
```

14. Guess the output of the code below with a reason.

```js
if (true) {
  let name = 'Arya Stark';
}
console.log(name); // Error name is not defined becuase let is block scoped and there is no name variable in the global scope
```

15. Guess the output of the code below with a reason.

```js
for (var i = 0; i < 20; i++) {
  //
}
console.log(i); //20  because var is not  block scoped and value of is is at last 20 
```

16. Guess the output of the code below with a reason.

```js
for (let i = 0; i < 20; i++) {
  //
}
console.log(i); // i  is not defined Reference Error  Because let is block scoped 
```

17. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    var username = 'John Snow';
  }
  console.log(username); // 'John Snow '// Becuase if block gets executed and value assigned to the username so 
  // var is not block scoped so output is 'jhon Snow'
}
sample();
```

18. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    let username = 'John Snow';
  }
  console.log(username);
}
sample();//Refernce erorr  Because usename is declared inside  the block and let is block scoped
```

19. Guess the output and the reason behind that.

```js
function sample() {
  var username = 'Arya Stark';
  if (true) {
    var username = 'John Snow';
    console.log(username);
  }
  console.log(username, 'second');
}
sample(); //  Jhon Snow
//'Jhon Snow second '
// becuase var is not   block scoped so it will redeclare the variable and now value is John  Snow so it wil console the above
//Output
```

20. Guess the output and the reason behind that.

```js
function sample() {
  let username = 'Arya Stark';
  if (true) {
    let username = 'John Snow';
    console.log(username, 'first');
  }
  console.log(username, 'second');
}
sample();
'Jhon Snow first'
'Arya Stark second'
// let is not block scope and we  can define  variable in the block scope or the local scope with any name  means the
// name does not collide  so the output is above given
```

21. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    let message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}

sample('First', 'Second', 'Third');
Hello I am First
Hello I am Second
 Hello I am Third
// Reason ...args means we can pass  any number of values
// so by using loop we are iterating that number of values and returning that number of messages
```

22. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    const message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}
// Reason ...args means we can pass  any number of values
// so by using loop we are iterating that number of values and returning that number of messages
```

23. Guess the output and the reason behind that.

```js
if (true) {
  const myFunc = function () {
    console.log(username, 'Second');
  };
  console.log(username, 'First');
  let username = 'Hello World!';
  myFunc();
}//
// Error we can not  access the username before initialization
// becuase behind the scene in the declaration phase we only decalre a single variable with no value means emty
// and in execution phase we  are acessing that variable before initialization
```

24. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    console.log(
      `I love this movie called ${movie.toUpperCase()}`
    );
  }
  inner();
}

outer();
// I love this movie called MAD MAX: FURY ROAD
// this is because  in function outer we are calling inner so inner has also access to outer scope so 
//it will console movie name with a message
```

25. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    let movie = 'Before Sunrise';
    console.log(
      `I love this movie called ${movie.toUpperCase()}`
    );
  }
  inner();
}

outer();
//I love this movie called BEFORE SUNRISE
// this is because  in function outer we are calling inner  
//it will console movie name with a message since inner already have a variable name movie in its scope so it do not
//go outside and  print the movie name with a message
```

26. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    let movie = 'Before Sunrise';
    function extraInner() {
      let movie = 'Gone Girl';
      console.log(
        `I love this movie called ${movie.toUpperCase()}`
      );
    }
    extraInner();
  }
  inner();
}
outer();
//I love this movie called BEFORE SUNRISE
// this is because  in function outer we are calling inner  
//it will console movie name with a message since etrainner already have a variable name movie in its scope so it do not
//go outside and  print the movie name with a message
```

30. Using reduce find the final value when the initial value passed is `100`. You have to pass the output of one function into the input of next function in the array `allFunctions` starts with `addOne` ends with `half`.

```js
const addOne = (num) => {
  return num + 1;
};
const subTwo = (num) => {
  return num - 2;
};
const multiplyThree = (num) => {
  return num * 3;
};
const half = (num) => {
  return num / 2;
};

let allFunctions = [
  addOne,
  subTwo,
  multiplyThree,
  addOne,
  multiplyThree,
  half,
];
allFunction.reduce((acc,cv)=>{
  acc= cv(acc);
  return acc;
},100);

// Answer is: 447
```
