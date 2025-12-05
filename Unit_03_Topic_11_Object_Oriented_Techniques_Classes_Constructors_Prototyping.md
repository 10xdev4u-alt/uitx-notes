---
title: "Unit III: JavaScript Object-Oriented Techniques (Classes, Constructors, Prototyping)"
id: unit3-topic11-oop-classes-prototyping
tags:
  - unit-3
  - javascript
  - oop
  - classes
  - constructors
  - prototyping
  - inheritance
aliases:
  - "JS OOP"
  - "JS Classes"
  - "JS Prototyping"
links:
  - "[[UITx/Unit_03_Topic_10_Form_Handling_and_Validations.md|Form Handling and Validations]]"
  - "[[UITx/Unit_03_Topic_12_JSON.md|JSON]]"
---

# Unit III, Topic 11: JavaScript Object-Oriented Techniques (Classes, Constructors, Prototyping)

> [!quote] As our programs grow in complexity, organizing code into modular, reusable structures becomes paramount. Object-Oriented Programming (OOP) provides a powerful paradigm for this, and JavaScript, with its unique blend of prototyping and modern class syntax, offers flexible ways to implement it. Let us now master the art of structuring our code with objects.

## 1. Introduction to Object-Oriented Programming (OOP) in JavaScript

OOP is a programming paradigm based on the concept of "objects", which can contain data (properties) and code (methods). The main principles of OOP include:
-   **Encapsulation:** Bundling data and methods that operate on the data within a single unit (object).
-   **Inheritance:** Allowing new objects to take on the properties and methods of existing objects.
-   **Polymorphism:** The ability of objects of different classes to respond to the same method call in different ways.
-   **Abstraction:** Hiding complex implementation details and showing only the necessary features of an object.

JavaScript is a **prototype-based** object-oriented language, meaning objects inherit directly from other objects. However, with the introduction of ES6, it gained a `class` syntax, which is syntactic sugar over its existing prototype-based inheritance.

## 2. Constructor Functions (Pre-ES6 OOP)

Before ES6 classes, **constructor functions** were the primary way to create multiple objects of the same type and implement inheritance. A constructor function is a regular function that is invoked with the `new` keyword.

-   **`this` keyword:** Inside a constructor, `this` refers to the newly created instance of the object.
-   **Properties:** Defined directly on `this`.
-   **Methods:** Often defined on the constructor's `prototype` to avoid duplicating them for every instance (improving memory efficiency).

### Example:
```javascript
// Constructor Function
function Person(name, age) {
    this.name = name;
    this.age = age;
}

// Adding a method to the prototype
Person.prototype.greet = function() {
    return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
};

// Creating instances
const person1 = new Person("Alice", 30);
const person2 = new Person("Bob", 25);

console.log(person1.greet()); // Output: Hello, my name is Alice and I am 30 years old.
console.log(person2.greet()); // Output: Hello, my name is Bob and I am 25 years old.
```

## 3. Prototyping and Prototype Chain

Every JavaScript object has a **prototype**. A prototype is also an object. All objects inherit properties and methods from their prototype. This forms a **prototype chain**.

-   When you try to access a property or method on an object, JavaScript first looks for it directly on the object.
-   If it doesn't find it, it looks on the object's prototype.
-   If still not found, it looks on the prototype's prototype, and so on, until it reaches `null` (the end of the chain).

### Example:
```javascript
const animal = {
    eats: true,
    walk() {
        console.log("Animal walks.");
    }
};

const rabbit = {
    jumps: true,
    __proto__: animal // rabbit inherits from animal
};

const longEar = {
    earLength: 10,
    __proto__: rabbit // longEar inherits from rabbit
};

longEar.walk(); // Output: Animal walks. (Method inherited from animal)
console.log(longEar.eats); // Output: true (Property inherited from animal)
```
The `__proto__` property (or `Object.getPrototypeOf()`) is how you access an object's prototype.

## 4. ES6 Classes (Syntactic Sugar)

Introduced in ES6 (ECMAScript 2015), **classes** provide a cleaner, more object-oriented syntax for creating objects and handling inheritance. It's important to remember that JavaScript classes are *not* true classes in the sense of traditional OOP languages like Java or C++; they are primarily syntactic sugar over JavaScript's existing prototype-based inheritance.

### a) Class Declaration
```javascript
class Animal {
    // Constructor method: called when a new instance is created
    constructor(name, species) {
        this.name = name;
        this.species = species;
    }

    // Method: automatically added to the prototype
    makeSound() {
        return "Generic animal sound";
    }

    // Static method: belongs to the class itself, not instances
    static identify() {
        return "This is an Animal class.";
    }
}

const dog = new Animal("Buddy", "Dog");
console.log(dog.makeSound()); // Output: Generic animal sound
console.log(Animal.identify()); // Output: This is an Animal class.
// console.log(dog.identify()); // Error: dog.identify is not a function
```

### b) Inheritance with `extends` and `super`
Classes support inheritance using the `extends` keyword. The `super()` keyword is used in the constructor of a subclass to call the parent class's constructor.

```javascript
class Dog extends Animal {
    constructor(name, breed) {
        super(name, "Dog"); // Call parent (Animal) constructor
        this.breed = breed;
    }

    // Override parent method
    makeSound() {
        return "Woof! Woof!";
    }

    fetch() {
        return `${this.name} is fetching!`;
    }
}

const myDog = new Dog("Max", "Golden Retriever");
console.log(myDog.makeSound()); // Output: Woof! Woof!
console.log(myDog.fetch());     // Output: Max is fetching!
console.log(myDog.species);     // Output: Dog (inherited from Animal constructor)
```

## 5. Exam-Oriented Insights

OOP concepts are crucial for structuring larger JavaScript applications.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary purpose of a constructor function in JavaScript?**
>     *Answer:* A constructor function is used to create and initialize multiple objects of a similar type, setting their initial properties.
> 2.  **Explain the concept of the prototype chain in JavaScript.**
>     *Answer:* The prototype chain is the mechanism by which JavaScript objects inherit properties and methods from other objects. When a property is accessed, JavaScript traverses up this chain until the property is found or the end of the chain (`null`) is reached.
> 3.  **How does ES6 `class` syntax relate to JavaScript's prototype-based inheritance?**
>     *Answer:* ES6 `class` syntax is primarily syntactic sugar over JavaScript's existing prototype-based inheritance, providing a cleaner and more familiar way to define constructor functions and their prototypes.
> 4.  **What is the role of the `super()` keyword in class inheritance?**
>     *Answer:* The `super()` keyword is used in the constructor of a subclass to call the constructor of its parent (superclass), ensuring that the parent's properties are correctly initialized.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a constructor function and then refactor it into an ES6 class, demonstrating how methods are added to the prototype. Explain the benefits of using OOP principles (like encapsulation and inheritance) for code organization and reusability. Discuss the implications of JavaScript being a prototype-based language, even with the `class` syntax.
