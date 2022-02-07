1. What does thread of execution means in JavaScript?
Thread of Execution means we are  executing the code line by line .
2. Where the JavaScript code gets executed?
Once  a javascript program is loaded in the javascript engine javascript engine cretes a global execution context for each program . And it created only once for a program .
javascript engine will executes the code line  by line  in the Global execution context .
3. What does context means in Global Execution Context?
 Context menas the Enviorment in which we are Executing  the code in the javascript.
4. When do you create a global execution context.
As soon as we  Execute a code snippet javascript  engine creates a global Execution context for a program .
5. Execution context consists of what all things?
Context contains a specific section known as  memory section used for storing the data .
6. What are the different types of execution context?
two types  of Execution context Global execution context and function Execution context.
7. When global and function execution context gets created?
Global and function execution context gets created only when we Execute  a code snippet. and function execution context get created inside the global execution context but only when we  execute a function  a function execution context gets created multiple times inside  the global execution context but the global execution context gets cretaed for only once .
8. Function execution gets created during function execution or while declaring a function.

Function Execution Context gets cretaed  during the  function execution  not  while the function declaration.
9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.



```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->





```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount){
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

![](./img/image-name.jpg)



```js
var age = 21;

function customeMessage(userAge){
  if(userAge > 18){
    return `You are an adult`;
  }else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](./img/image-name.jpg)