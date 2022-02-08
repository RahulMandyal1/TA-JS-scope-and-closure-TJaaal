Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(useranme); // output
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); // Uncaught ReferenceError: useranme is not defined
```
 In the  above  code we  are looking  for a variable name 'username' . But there is no variable `username` in the global scope 
 . The variable is inside a block scope  so we can nto access it from outside so it will through an  error Reference Error Like.

 The above code will throw an error `Reference Error username is not defined`.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(useranme); // Uncaught ReferenceError: useranme is not defined
```

In the  above  code we  are looking  for a variable name 'username' . But there is no variable `username` in the global scope 
The variable is inside a block scope  so we can not access it from outside so it will through an  error Reference Error Like.

 The above code will throw an error `Reference Error username is not defined`.
4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(username); // 'Arya'

In the  above  code we  are looking  for a variable name `username` and username is inside a block but var is not block scoped so 
we can access the value of username as  a global variable.
 so the output is 'Arya'
```

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  var username = 'Arya';
}
console.log(username); //Arya

The output of the above code is Arya because we can redeclare the variable with the  var keyword as  much we can and Since  var does not have block scope so that,s why it is redeclaring the variable again  and reassigning the value again.
```

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(username); // 'John'
in this code  we are  logging the value of the username that is also present in the global scope and also  in the block scope .
since  let  has  a block scope so we can not access the variable from a block but  we can access a global variable  so that,s why the output is John 
```

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(useranme); // John

 in this code we are declaring a variable named as username with a value  of Jhon and we are also declaring a function declaration with some function scoped variable and returning nothing from that function .
 A function with no return type always return undefined 
 so when we call this function we  can undefined.

 and at last  we are  consoling  the variable username that is already presen in the global scope

```

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
//  the output is 
 0 'First'
 1 'First'
 2 'First'
 3 'First'
 4 'First'
 5 'First'
 6 'First'
 7 'First'
 8 'First'
 9 'First'

console.log(i, 'Second'); //  10 , Second

In this above code we  are repeating i from 0 to 9 and every time First  is repeated with the number and after that we are trying to log i and along it with a string "Second" so it will print 10 and also Second this is because var is not block scoped so we can use its i variable in the gobal scope also.

```

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); 
}
//  the output is 
 0 'First'
 1 'First'
 2 'First'
 3 'First'
 4 'First'
 5 'First'
 6 'First'
 7 'First'
 8 'First'
 9 'First'
console.log(i, 'Second'); // Reference Error Becuase i is not Defined in the Global scope 
This is because in the above loop i is defined but it is block scoped and since let  is block scope so we  can not access the i outside the block scope
```
