

1. Function Declaration:

   * In JavaScript, we don't need a class for declaring a function.
   * We don't need to define return type, parameter data types, or access modifiers.

   function add(a, b) {
   return a + b;
   }

   In Java:
   public static int add(int a, int b)

2. Functions as Values:

   * JavaScript allows you to store a function inside a variable.

   const add = function(a, b) {
   return a + b;
   };

   * A function can be treated like a value.
   * This is called a First-Class Function.
   * This concept is very important in React.

3. Function Declaration vs Function Expression:

   a) Function Declaration:
   function greet() {
   console.log("Hello");
   }

   b) Function Expression:
   const greet = function() {
   console.log("Hello");
   };

   * Both can be called using greet();
   * They are created differently.
   * Function Declaration → can generally be called before its declaration.
   * Function Expression with const → must be initialized before calling.

4. Arrow Functions:

   * JavaScript provides a shorter way to write functions.

   const add = (a, b) => a + b;

   * Arrow functions are used very frequently in React.

5. Missing Arguments:

   * JavaScript allows you to provide fewer arguments than the number of parameters.

   function add(a, b) {
   return a + b;
   }

   add(10);

   * Here b becomes undefined.
   * 10 + undefined → NaN.

6. Default Parameters:

   * We can provide a default value for a parameter.

   function greet(name = "Guest") {
   console.log("Hello " + name);
   }

   greet("Neha");  → Hello Neha
   greet();        → Hello Guest

7. Passing a Function as an Argument:

   * JavaScript allows us to pass a function to another function.

   function greet() {
   console.log("Hello");
   }

   function executeSomething(fn) {
   fn();
   }

   executeSomething(greet);

   Important:
   executeSomething(greet);   → passes the function
   executeSomething(greet());  → executes the function immediately

   greet     → function itself
   greet()   → executes the function

8. Callback Function:

   * When a function is passed to another function and is executed by that function, it is called a callback function.

   function greet(name) {
   console.log("Hello " + name);
   }

   function processUser(callback) {
   callback("Neha");
   }

   processUser(greet);

   * Here, greet is the callback function.

9. React Event Handlers:

   * React uses functions as callbacks.

   <button onClick={handleClick}>
       Click
   </button>

   Meaning:
   React, here is the handleClick function. Call it when the button is clicked.

   Correct:
   onClick={handleClick}

   Wrong:
   onClick={handleClick()}

   * handleClick → gives React the function
   * handleClick() → executes the function immediately

10. Functions Can Return Functions:

    * A function can return another function.

    function outer() {
    return function inner() {
    console.log("Hello");
    };
    }

    * This concept leads to Closures, which are important later in React.

11. Main JavaScript Function Concept:
    A function can be:

    * Declared
    * Stored in a variable
    * Passed as an argument
    * Returned from another function

    Most important distinction:

    greet    → function itself
    greet()  → execute the function
