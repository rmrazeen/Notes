Here’s your comprehensive JavaScript notes in **GitHub-flavored Markdown (`.md`) format**, including the requested topics (`class`, `prototype`, `constructor`, `Set`, `Map`, `Promise`, `callback functions`):

```markdown
# JavaScript Notes

## Table of Contents
- [Basics](#basics)
- [Functions](#functions)
- [Arrays](#arrays)
- [Objects](#objects)
- [Classes & OOP](#classes--oop)
- [Prototypes](#prototypes)
- [Constructor Functions](#constructor-functions)
- [Set & Map](#set--map)
- [Asynchronous JS](#asynchronous-js)
  - [Callbacks](#callbacks)
  - [Promises](#promises)
- [DOM Manipulation](#dom-manipulation)

---

## Basics

### 1. Random Number & Even/Odd Check
```javascript
let num = Math.floor(Math.random() * 100) + 1;
if (num % 2 === 0) {
  console.log(`${num} is even`);
} else {
  console.log(`${num} is odd`);
}
```

### 2. Ternary Operator
```javascript
let age = 25;
let result = age >= 18 ? "Adult" : "Child";
console.log(result); // "Adult"
```

---

## Functions

### 3. Callback Functions
```javascript
function greet(name, callback) {
  console.log(`Hello, ${name}!`);
  callback();
}

function sayGoodbye() {
  console.log("Goodbye!");
}

greet("Alice", sayGoodbye);
// Output:
// Hello, Alice!
// Goodbye!
```

---

## Arrays

### 4. Array Methods
```javascript
let nums = [1, 2, 3];

// Map
let doubled = nums.map(num => num * 2); // [2, 4, 6]

// Filter
let evens = nums.filter(num => num % 2 === 0); // [2]

// Reduce
let sum = nums.reduce((acc, curr) => acc + curr, 0); // 6
```

---

## Objects

### 5. Object Iteration
```javascript
let student = {
  name: "Rahul",
  age: 25
};

for (let key in student) {
  console.log(`${key}: ${student[key]}`);
}
```

---

## Classes & OOP

### 6. Class Syntax
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, I'm ${this.name}`);
  }
}

const person1 = new Person("Alice", 30);
person1.greet(); // "Hello, I'm Alice"
```

---

## Prototypes

### 7. Prototype Inheritance
```javascript
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(`${this.name} makes a noise.`);
};

function Dog(name) {
  Animal.call(this, name);
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

const dog = new Dog("Rex");
dog.speak(); // "Rex makes a noise."
```

---

## Constructor Functions

### 8. Constructor Pattern
```javascript
function Car(make, model) {
  this.make = make;
  this.model = model;
  this.drive = function() {
    console.log(`Driving ${this.make} ${this.model}`);
  };
}

const myCar = new Car("Toyota", "Camry");
myCar.drive(); // "Driving Toyota Camry"
```

---

## Set & Map

### 9. Set (Unique Values)
```javascript
let set = new Set();
set.add(1);
set.add(2);
set.add(1); // Duplicate ignored
console.log(set.size); // 2
```

### 10. Map (Key-Value Pairs)
```javascript
let map = new Map();
map.set("name", "Alice");
map.set("age", 25);
console.log(map.get("name")); // "Alice"
```

---

## Asynchronous JS

### 11. Promises
```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Data fetched!");
    }, 1000);
  });
}

fetchData()
  .then(data => console.log(data)) // "Data fetched!"
  .catch(err => console.error(err));
```

### 12. Async/Await
```javascript
async function getData() {
  try {
    let data = await fetchData();
    console.log(data); // "Data fetched!"
  } catch (err) {
    console.error(err);
  }
}
```

---

## DOM Manipulation

### 13. Query Selectors
```javascript
let button = document.querySelector("#btn");
button.addEventListener("click", () => {
  console.log("Button clicked!");
});
```

### 14. Create & Append Elements
```javascript
let div = document.createElement("div");
div.textContent = "Hello, DOM!";
document.body.appendChild(div);
```

---

## Key Takeaways
- **Classes**: Syntactic sugar over prototypes.
- **Prototypes**: Shared properties/methods for memory efficiency.
- **Sets/Maps**: Better alternatives for unique values and key-value pairs.
- **Promises**: Cleaner async handling than callbacks.
- **Callbacks**: Foundational for async operations.

```

### Features Added:
1. **Classes**: ES6 `class` syntax with inheritance.
2. **Prototypes**: How JavaScript implements inheritance.
3. **Constructors**: Traditional object creation pattern.
4. **Set/Map**: Modern collections for unique values and key-value pairs.
5. **Promises**: Async/await and `.then()` syntax.
6. **Callbacks**: Foundation for async programming.

Would you like me to expand any section further? 😊
