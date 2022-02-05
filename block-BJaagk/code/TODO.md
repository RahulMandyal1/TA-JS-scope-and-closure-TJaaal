1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

//Function Expression or Anonymous function
let percentage = function(marks,total){
  return (marks*100)/total;
}

//Arrow function 

let percentage= (marks,total)=>  (marks*100)/total;

```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) { // function declaration
  return (marks * 100) / total;
}

```

```js
let percentage = function percentage(marks, total) { // function Expression 
  return (marks * 100) / total;
};
```

```js
let percentage = function (marks, total) { //function expression
  return (marks * 100) / total;
};
```

```js
let percentage = (marks, total) => { // arrow function or function expression
  return (marks * 100) / total;
};
```

```js
let percentage = (marks, total) => (marks * 100) / total; // Arrow function one  line implicit return 
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

Function Definition - A function declared with a  function  keyword  and followed by the name of that function 
 is known as  function definition.

Function Expresssion = A function which is stored  inside a  variable  is known as  function Expression

Example  :
let sum = function (a,b){
  return a+b ;
}

4. Why is a function call an expression in JavaScript?

 AN Expression is something that result into a value .A function is  an  object in javascript  or an object result into an Expression . so that,s  why a function call an expression in the javascript
5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3);  //5
five = add; // Return a function definition
five = five(10, 11);  //21
five = function () {
  return 'Hello';
}; //  Hello
```

6. What is the difference between function definition and function call? Explain with an example.
A function definition is  the number of steps that needs to be performed  and  a function call is the execution of that function.
by calling that function we are  executing those number of steps we have defined earlier in the function definition.

function mul(numberFirst ,numberSecond){
  return numberFirst * numberSecond ;
}

// now call this function to perform multiplication 
mul(4,5); //answer is 20

7. What is the similarities between function definition and function call?
In function definition we are defining some task that needs to be done . And in the function call we are completing that task .
8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // Sam Function is onjec in the javascript so we  can do like this  or either we can use this function
```

9. What is higher order function explain with an example.

higher order function are those   function which accept  a function definion as  a parameter or either return a function definition as a return type of that function.

Example :
function sum (){
  return function (a,b){
    return a + b;
  }
}
10. Explain what is callback function. Why you can pass a function inside a function?
A function which  is passed inside  a function as a function argument that passed function refernce is known as callback function
A function is an object in javascript an object result into expression so that,s why we can pass a fucntion inside a function

In order to do not repeat some time we need to reuse code again and again and in some cases it,s better to create a function so the code is not to be rewrite again and again and we  can follow do not repeat approach .  So  in order to follow do no repeat approach we can pass function inside  a function and we can make  a high order function.