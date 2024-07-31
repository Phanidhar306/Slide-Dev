---
theme: frankfurt
infoLine: true
author: "Sai Phanidhar Guttula"
title: "Types of Functions"
date: "2024/07/16"
---

# JavaScript Function Types

<v-clicks>

JavaScript supports several types of functions, each serving different purposes and providing varying levels of flexibility. Here are some common types:

</v-clicks>

<v-clicks>

1. **Named Function**
2. **Anonymous Function**
3. **Arrow Function**
4. **Immediately Invoked Function Expression (IIFE)**
5. **Function Constructor**

</v-clicks>

---

<v-clicks>
  
  <Item title="1. Named Function">
  
  **Definition**: A function is a relation that uniquely associates members of one set with members of another set.

![width:300px](https://media0.giphy.com/media/P5wPrhzZDdeJW/giphy.webp?cid=790b7611fu165b15ppp52aoft8zsx4aa8uy9esvv6460gnzj&ep=v1_gifs_search&rid=giphy.webp&ct=g)

  </Item>

</v-clicks>

<v-clicks>

### Example code.

Named functions are defined using the function keyword followed by a name. They can be reused by calling their name. -->

```javascript
function calculateHypotenuse(a, b) {
  return Math.sqrt(a * a + b * b);
}
console.log(calculateHypotenuse(3, 4)); // Output: 5
```

</v-clicks>

---

<v-clicks>

  <Item title="2. Anonymous Function">
  
  **Definition**: An anonymous function does not have a name. It is often used as a callback function.

![width:100px](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExN2MzejVoMG43cms1YWhsM2JqamxxOWp0OG1kcWluMHNwdHo0Zm84ZyZlcD12MV9naWZzX3NlYXJjaCZjdD1n/3og0ILLVvPp8d64Jd6/giphy.webp)

  </Item>

</v-clicks>

<v-click>

### Example code.

Anonymous functions do not have a name and are often assigned to variables or used as arguments to other functions. They are useful for creating quick, throwaway functions.

</v-click>

<v-click>

```javascript
const greet = function () {
  console.log("Hello, World!");
};

greet(); // Output: Hello, World!
```

</v-click>

---

<v-clicks>

<Item title="3. Arrow Function">

**Definition**: Arrow functions provide a more concise syntax and do not have their own this context.

![width:300px](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlRZM9QHx8SUu-cG_FyM-dwsawZYr4KPrpTQ&s)

</Item>

</v-clicks>

### Example code.

Arrow functions provide a concise syntax and lexically bind the this value. They are especially useful for writing short functions.

<v-clicks>

```javascript
const greet = () => {
  console.log("Hello, World!");
};

greet(); // Output: Hello, World!
```

</v-clicks>

---

<v-clicks>

<Item title="4. Immediately Invoked Function Expression (IIFE)">

**Definition**: An IIFE is a function that runs as soon as it is defined.

![width:300px](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQgxu149_TExIRdbmTRjuEdGhFLIvLyIFweoQ&s)

</Item>

</v-clicks>

### Example code.

An IIFE is a function that runs as soon as it is defined. This pattern is often used to create a local scope to avoid polluting the global namespace.

<v-clicks>

```javascript
(function () {
  console.log("Hello, World!");
})(); // Output: Hello, World!
```

</v-clicks>

---

<v-clicks>

<Item title="5. Function Constructor">

**Definition**: Functions can also be defined using the Function constructor.

![width:100px](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTYxNjloczRkZ2c0dGMyYTQzbG5ubXFlc2Q0emcxbHhoZWp0eDJxNSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/qt73FYHjuXqAj241m8/giphy.webp)

</Item>

</v-clicks>

---

### Example code.

Functions can be created using the Function constructor, which dynamically generates a new function. This method is less common and generally not recommended due to performance and security concerns.

<v-clicks>

```javascript
const greet = new Function('console.log("Hello, World!");');

greet(); // Output: Hello, World!
```

</v-clicks>

---

<Item title="6. Generator Function">

**Definition**: Generator functions can pause execution and resume at a later point.

</Item>

![width:25px](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2JkdXQ4YWc3eHZiOWVhZGFrYXpidTlkcjQwdTlncjZsZmZxbnd1MCZlcD12MV9naWZzX3NlYXJjaCZjdD1n/3o6gEaLDVsHUcmyTZe/200.webp)

---

### Example code.

Generator functions can pause execution using the yield keyword and can be resumed later. They are useful for creating iterators and managing asynchronous operations.

```javascript
function* greet() {
  yield "Hello";
  yield "World";
}

const greeter = greet();
console.log(greeter.next().value); // Output: Hello
console.log(greeter.next().value); // Output: World
```

---

<Item title="7. Async Function">

**Definition**: Async functions allow writing asynchronous code in a more synchronous manner.

</Item>

### Example code.

To incorporate code into boxes for definitions, lemmas, theorems, etc., you can use blockquotes or HTML for enhanced styling. Here are some

```javascript
async function greet() {
  return "Hello, World!";
}

greet().then(console.log); // Output: Hello, World!
```

---
