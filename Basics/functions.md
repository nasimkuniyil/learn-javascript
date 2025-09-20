# Functions in JavaScript

A function is a reusable block of code that performs a specific task
It helps in *modularity, readability, maintainability, and reusability* of code

---

## Types of Function

### Based on Definition Style

1. Regular Function (Function Declaration)

```js
function greet() {
  console.log("Hello!");
}
```

2. Function Expression

```js
const great = function (){
    console.log("hello");
}
```

3. Arrow Function (Introduced in ES6)

```js
const great = ()=>{
    console.log("hello");
}
```

4. Anonymous Function (function without name, often used as arguments)

```js
setTimeout(function(){
    console.log("this is anonymous function");
},1000);
```

5. Callback Function (function passed as an argument to aonther function)

```js
function process(callback){
    callback();
}
process(()=>console.log("Callback executed"));
```

6. First-Class Functions

- In JavaScript, Funcitons are treated as first-class citizens.
- This means functions can be:
  - Assigned to variables
  - Passed as arguments
  - Returned from other functions

7. Higher-Order Function (HOF)

- A function that takes another function as an argument or returns another function.

```js
function higherOrder(fn){
    return function(){
        fn();
    }
}
```

8. Immediately Invoked Function Expression (IIFE)

```js
(function(){
    console.log("IIFE invoked.");
})()
```

### Based on Arguments and Return value

1. Function without argument without return value
2. Function with argument with return value
3. Function with argument without return value
4. Function without argument with return value

## Extra points about functions

- Functions can be named or anonymous.
- Default Parameters can be used in function.
- Functions in JavaScript are objects with properties and methods.
