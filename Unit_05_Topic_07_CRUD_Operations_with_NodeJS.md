---
title: "Unit V: Implementation of CRUD Operations with Node.js"
id: unit5-topic7-crud-operations
tags:
  - unit-5
  - nodejs
  - crud
  - mongodb
  - mongoose
  - api
aliases:
  - "Node.js CRUD"
links:
  - "[[UITx/Unit_05_Topic_06_Connecting_to_NoSQL_Database.md|Connecting to NoSQL Database]]"
  - "[[UITx/Unit_05_Quiz.md|Unit 05 Quiz]]"
---

# Unit V, Topic 7: Implementation of CRUD Operations with Node.js

> [!quote] A database connection is only the first step; the true power of a data-driven application lies in its ability to manipulate that data. CRUD—Create, Read, Update, and Delete—are the four fundamental operations of persistent storage. Mastering their implementation in Node.js is essential for building any dynamic web service or API.

## 1. What are CRUD Operations?

**CRUD** is an acronym that stands for the four basic functions of persistent storage:

-   **Create:** Add new data to the database.
-   **Read:** Retrieve data from the database.
-   **Update:** Modify existing data in the database.
-   **Delete:** Remove data from the database.

These four operations are the foundation of most applications that interact with a database. In the context of a web API, they often map directly to HTTP methods:

-   `POST` -> **Create**
-   `GET` -> **Read**
-   `PUT` / `PATCH` -> **Update**
-   `DELETE` -> **Delete**

For our examples, we will use **Mongoose**, as its high-level methods make implementing CRUD operations clean and intuitive. We will assume we have already connected to MongoDB and have a `User` model defined as in the previous topic.

```javascript
// Prerequisite: Mongoose connection and User model
const mongoose = require('mongoose');

// Define the Schema
const userSchema = new mongoose.Schema({
    name: { type: String, required: true },
    email: { type: String, required: true, unique: true },
    age: Number
});

// Compile the Model
const User = mongoose.model('User', userSchema);
```

## 2. Create (Adding New Data)

The **Create** operation involves creating a new instance of a model and saving it to the database.

### `new Model()` and `.save()`
You can create a new document using the model constructor and then call the `.save()` method on the instance.

```javascript
async function createUser(userData) {
    try {
        const newUser = new User({
            name: userData.name,
            email: userData.email,
            age: userData.age
        });

        const savedUser = await newUser.save();
        console.log("User created successfully:", savedUser);
        return savedUser;
    } catch (error) {
        console.error("Error creating user:", error);
    }
}

// Usage:
// createUser({ name: "John Doe", email: "john.doe@example.com", age: 30 });
```

### `Model.create()`
A convenient shorthand for creating and saving one or more documents.

```javascript
async function createAnotherUser(userData) {
    try {
        const createdUser = await User.create(userData);
        console.log("User created with .create():", createdUser);
        return createdUser;
    } catch (error) {
        console.error("Error creating user:", error);
    }
}

// Usage:
// createAnotherUser({ name: "Jane Smith", email: "jane.smith@example.com", age: 25 });
```

## 3. Read (Retrieving Data)

The **Read** operation involves querying the database to find documents.

### `Model.find()`
Finds all documents matching a query object. If the query object is empty, it returns all documents in the collection.

```javascript
async function getAllUsers() {
    try {
        const users = await User.find({}); // Empty query finds all
        console.log("All users:", users);
        return users;
    } catch (error) {
        console.error("Error fetching users:", error);
    }
}
```

### `Model.findById()`
A convenient method for finding a single document by its unique `_id`.

```javascript
async function getUserById(id) {
    try {
        const user = await User.findById(id);
        console.log("Found user:", user);
        return user;
    } catch (error) {
        console.error("Error finding user:", error);
    }
}
```

### `Model.findOne()`
Finds the first document that matches a query object.

```javascript
async function findUserByEmail(email) {
    try {
        const user = await User.findOne({ email: email });
        console.log("Found user by email:", user);
        return user;
    } catch (error) {
        console.error("Error finding user:", error);
    }
}
```

## 4. Update (Modifying Data)

The **Update** operation modifies existing documents.

### `Model.updateOne()` or `Model.updateMany()`
Updates the first document (or multiple documents) that matches a query.

```javascript
async function updateUserAge(email, newAge) {
    try {
        const result = await User.updateOne(
            { email: email },         // Find a user with this email
            { $set: { age: newAge } } // Update their age
        );
        console.log("Update result:", result);
        // result contains info like { matchedCount: 1, modifiedCount: 1 }
    } catch (error) {
        console.error("Error updating user:", error);
    }
}

// Usage:
// updateUserAge("john.doe@example.com", 31);
```
-   `$set`: This is a MongoDB update operator that sets the value of a field.

### `Model.findByIdAndUpdate()`
Finds a document by its ID and updates it. This is very common and useful as it can also return the updated document.

```javascript
async function findAndUpdatUser(id, updateData) {
    try {
        const updatedUser = await User.findByIdAndUpdate(
            id,
            updateData,
            { new: true } // This option returns the document after the update
        );
        console.log("Updated user:", updatedUser);
        return updatedUser;
    } catch (error) {
        console.error("Error updating user:", error);
    }
}
```

## 5. Delete (Removing Data)

The **Delete** operation removes documents from the database.

### `Model.deleteOne()` or `Model.deleteMany()`
Deletes the first document (or multiple documents) that matches a query.

```javascript
async function deleteUserByEmail(email) {
    try {
        const result = await User.deleteOne({ email: email });
        console.log("Delete result:", result);
        // result contains info like { deletedCount: 1 }
    } catch (error) {
        console.error("Error deleting user:", error);
    }
}
```

### `Model.findByIdAndDelete()`
Finds a document by its ID and deletes it, returning the deleted document.

```javascript
async function findAndRemoveUser(id) {
    try {
        const deletedUser = await User.findByIdAndDelete(id);
        console.log("Deleted user:", deletedUser);
        return deletedUser;
    } catch (error) {
        console.error("Error deleting user:", error);
    }
}
```

## 6. Exam-Oriented Insights

CRUD operations are the practical application of database knowledge.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What does the acronym CRUD stand for?**
>     *Answer:* Create, Read, Update, Delete.
> 2.  **In Mongoose, which method is used to add a new document to the database?**
>     *Answer:* The `.save()` method on a new model instance, or the static `Model.create()` method.
> 3.  **How would you find all documents in a Mongoose collection named `Product`?**
>     *Answer:* By using the `find()` method with an empty query object: `Product.find({})`.
> 4.  **What is the purpose of the `{ new: true }` option in `findByIdAndUpdate()`?**
>     *Answer:* It ensures that the method returns the document *after* the update has been applied, rather than the original document before the update.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a set of `async` functions that implement all four CRUD operations for a given Mongoose model. Explain the difference between `updateOne()` and `findByIdAndUpdate()`. Discuss how these CRUD operations map to a RESTful API's HTTP methods (e.g., `POST` for Create, `GET` for Read, etc.).
