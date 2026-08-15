1. In JavaScript We dont need a class for function declaration and defination . 
2. WE dont need to define scope and return type of functions. 
3.JavaScript allows you to put a function inside a variable.
  for example, [const add = function(a, b) {
                return a + b;}]
A function can be treated like a value.
This is called a first-class function.
And this concept is extremely important for React.

4.  Function Declaration vs Function Expression
  a]Declaration:
  function greet() {
    console.log("Hello");}

  b]Expression  :
  const greet = function() {
    console.log("Hello");};
Note:
Both can be called like:
greet();
But they are created differently.
Function declaration
→ can generally be called before its declaration

Function expression with const
→ must be initialized before calling

5.Arrow Functions.
const add = (a, b) => a + b;  we can write a function in js like this. 
6.JavaScript allows missing arguments
for example, function add(a, b) {
    return a + b;}
     add(10);
     =>here b becomes undefined so 10+ undefined -> NaN
7. Default parameters

JavaScript provides a very convenient feature:
function greet(name = "Guest") {
    console.log("Hello " + name);
}   
greet("Neha");->Hello Neha
greet();->Hello Guest

8.function greet() {
    console.log("Hello");}
function executeSomething(fn) {
    fn();}
    executeSomething(greet);  //Note :  executeSomething(greet()); this gives error . 

9.13. Callback functions
When you pass a function to another function, that function can be called a callback.  
function greet(name) {
    console.log("Hello " + name);
}

function processUser(callback) {
    callback("Neha");
}

processUser(greet);

10. REact use 
Correct:

<button onClick={handleClick}>

This means:
React, here is the function. Call it when the button is clicked.
This is why understanding functions as values is so important.
    




    
  
