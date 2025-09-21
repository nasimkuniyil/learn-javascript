# 🚀 Arrow Function Expression

Arrow function is a **shorter and cleaner way** to write functions in JavaScript.  
It was introduced in **ES6 (2015)**.  

Arrow functions are especially useful for **small functions** and when working with array methods like `map`, `filter`, and `forEach`.

---

## ✨ Key Points

- Uses the `=>` (fat arrow) syntax.  
- Arrow functions **do not have their own `this`**, they **inherit** `this` from the surrounding scope (lexical scope).  
- No `arguments` object inside arrow functions.  
- Cannot be used as constructors (❌ cannot use `new`).  
- Works best for **callbacks and short functions**.  

---

## 📝 Syntax

```js
// Normal arrow function
const add = (a, b) => {
  return a + b;
};

// Shorter version (when function body has one return statement)
const add = (a, b) => a + b;

// One parameter → no need for parentheses
const greet = name => `Hello ${name}`;
```

## Examples

1. Normal function vs Arrow function

```js
// Regular function
function square(x) {
  return x * x;
}

// Arrow function
const squareArrow = x => x * x;

console.log(square(5));      // 25
console.log(squareArrow(5)); // 25

```

2. With array methods

```js
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(n => n * 2);

console.log(doubled); // [2, 4, 6, 8, 10]

```

3. Defference of `this`

```js
const person = {
  name: "Nasim",
  regularFunc: function () {
    console.log("Regular:", this.name);
  },
  arrowFunc: () => {
    console.log("Arrow:", this.name);
  }
};

person.regularFunc(); // Regular: Nasim
person.arrowFunc();   // Arrow: undefined (no own this)

```

## Real World UseCase

Suppose you are building a **Todo list**

```js
const todos = [
  { task: "Learn JavaScript", done: true },
  { task: "Learn React", done: false }
];

// Filter completed tasks using arrow function
const completed = todos.filter(todo => todo.done);

console.log(completed);
// [{ task: "Learn JavaScript", done: true }]

```

## Arrow functions vs Regular functions

**Arrow function**

- syntax : shorter
- `this` binding : inherits from surrounding scop
- `arguments` object : No
- can be used as method : Not recommended (because no own `this`)
- can be used as constructor (new) : no
- best for : small functions and callback

**Regular function**

- syntax : longer
- `this` binding : own this
- `arguments` object : yes
- can be used as method : yes
- can be used as constructor (new) : yes
- best for : complex logic and object methods.
