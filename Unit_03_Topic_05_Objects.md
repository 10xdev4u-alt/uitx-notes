---
title: "Unit III: JavaScript Objects"
id: unit3-topic5-objects
tags:
  - unit-3
  - javascript
  - objects
  - properties
  - methods
  - object-literal
aliases:
  - "JS Objects"
links:
  - "[[UITx/Unit_03_Topic_04_Functions_and_Scope.md|Functions and Scope]]"
  - "[[UITx/Unit_03_Topic_06_Array_Date_and_Math_Objects.md|Array, Date and Math Objects]]"
---

# Unit III, Topic 5: JavaScript Objects

> [!quote] In JavaScript, almost everything is an object. They are the fundamental building blocks for structuring complex data and behavior, allowing us to model real-world entities with properties and actions. Understanding objects is key to mastering JavaScript's dynamic and flexible nature. Let us now delve into their essence.

## 1. What are JavaScript Objects?

An **object** in JavaScript is a standalone entity, with properties and types. Think of it as a container that can hold multiple named values. These named values are called **properties**, and if a property's value is a function, it's called a **method**.

Objects are a complex (non-primitive) data type. They are unordered collections of key-value pairs. The keys (or property names) are strings (or Symbols), and the values can be any JavaScript data type, including other objects, functions, or primitive values.

## 2. Creating Objects

There are several ways to create objects in JavaScript.

### a) Object Literal (Most Common)
This is the simplest and most common way to create an object.

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    isStudent: false,
    // A method (a function as a property)
    greet: function() {
        return `Hello, my name is ${this.firstName} ${this.lastName}.`;
    }
};
console.log(person.greet()); // Output: Hello, my name is John Doe.
```

### b) Using the `new Object()` Constructor
Less common, but equivalent to the object literal.

```javascript
const car = new Object();
car.make = "Toyota";
car.model = "Camry";
car.year = 2020;
console.log(car); // Output: { make: "Toyota", model: "Camry", year: 2020 }
```

### c) Using Constructor Functions (Pre-ES6)
Before ES6 classes, constructor functions were used to create multiple objects of the same "type."

```javascript
function Book(title, author, year) {
    this.title = title;
    this.author = author;
    this.year = year;
    this.getSummary = function() {
        return `${this.title} by ${this.author}, published in ${this.year}.`;
    };
}

const book1 = new Book("The Hobbit", "J.R.R. Tolkien", 1937);
console.log(book1.getSummary()); // Output: The Hobbit by J.R.R. Tolkien, published in 1937.
```

### d) Using ES6 Classes (Syntactic Sugar over Prototypes)
Introduced in ES6, classes provide a cleaner, more familiar syntax for creating objects and handling inheritance. (We will cover classes in more detail later).

```javascript
class Animal {
    constructor(name, species) {
        this.name = name;
        this.species = species;
    }
    makeSound() {
        return "Generic animal sound";
    }
}

const dog = new Animal("Buddy", "Dog");
console.log(dog.makeSound()); // Output: Generic animal sound
```

## 3. Accessing Object Properties and Methods

There are two main ways to access properties and methods of an object:

### a) Dot Notation (Preferred)
-   Use when you know the property name beforehand.
    ```javascript
    console.log(person.firstName); // Output: John
    console.log(person.age);      // Output: 30
    ```

### b) Bracket Notation
-   Use when the property name is dynamic (e.g., stored in a variable) or contains special characters (like spaces or hyphens).
    ```javascript
    const key = "lastName";
    console.log(person[key]); // Output: Doe
    console.log(person["isStudent"]); // Output: false
    ```

## 4. Modifying Objects

Objects are mutable, meaning their properties can be changed after creation.

### a) Adding New Properties
```javascript
person.email = "john.doe@example.com";
console.log(person.email); // Output: john.doe@example.com
```

### b) Modifying Existing Properties
```javascript
person.age = 31;
console.log(person.age); // Output: 31
```

### c) Deleting Properties
```javascript
delete person.isStudent;
console.log(person.isStudent); // Output: undefined
```

## 5. The `this` Keyword

The `this` keyword refers to the object that is currently executing the code. Its value depends on *how* a function is called.

-   **Method Call:** If a function is called as a method of an object (e.g., `person.greet()`), `this` refers to that object (`person`).
-   **Simple Function Call:** In non-strict mode, `this` refers to the global object (e.g., `window` in browsers). In strict mode, `this` is `undefined`.
-   **Arrow Functions:** Arrow functions do not have their own `this` context; they inherit `this` from their enclosing lexical context.

**Example:**
```javascript
const user = {
    name: "Alice",
    sayName: function() {
        console.log(this.name); // 'this' refers to 'user'
    }
};
user.sayName(); // Output: Alice

const anotherUser = { name: "Bob" };
anotherUser.sayName = user.sayName; // Assign the method
anotherUser.sayName(); // Output: Bob (because 'this' refers to 'anotherUser')

const unboundSayName = user.sayName;
// unboundSayName(); // In non-strict: undefined (or global object's name if it exists)
                    // In strict: TypeError: Cannot read properties of undefined (reading 'name')
```

## 6. Iterating Over Object Properties

### a) `for...in` Loop
Iterates over enumerable properties of an object (including inherited ones, unless filtered).

```javascript
for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

### b) `Object.keys()`, `Object.values()`, `Object.entries()` (ES6+)
These methods return arrays of an object's own enumerable property names, values, or key-value pairs, respectively.

```javascript
console.log(Object.keys(person));   // ["firstName", "lastName", "age", "isStudent", "greet", "email"]
console.log(Object.values(person)); // ["John", "Doe", 30, false, ƒ, "john.doe@example.com"]
console.log(Object.entries(person)); // [["firstName", "John"], ["lastName", "Doe"], ...]
```

## 7. Exam-Oriented Insights

Objects are central to JavaScript programming.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is a JavaScript object?**
>     *Answer:* A JavaScript object is a standalone entity, a complex data type that is an unordered collection of key-value pairs, where values can be any data type, including functions (methods).
> 2.  **Name two ways to create an object in JavaScript.**
>     *Answer:* Object literal syntax (`{}`), `new Object()`, constructor functions, ES6 classes (any two).
> 3.  **Differentiate between accessing an object property using dot notation vs. bracket notation.**
>     *Answer:* Dot notation (`object.property`) is preferred when the property name is known and static. Bracket notation (`object['property']`) is used when the property name is dynamic (e.g., stored in a variable) or contains special characters.
> 4.  **What does the `this` keyword refer to when a function is called as a method of an object?**
>     *Answer:* When a function is called as a method of an object, `this` refers to that object itself.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write JavaScript code to create an object using the object literal syntax, add a method to it, and then access and modify its properties. Explain the concept of mutability in JavaScript objects. Discuss the different contexts of the `this` keyword and how its value changes based on how a function is invoked.
