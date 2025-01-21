# MongoDB $inc operator error with string value
This example demonstrates an incorrect usage of the MongoDB $inc operator, where a string is provided instead of a number.  The $inc operator is used to increment a numeric field by a specified value. Attempting to increment with a string will result in an error.  The solution shows the correct way to use the $inc operator, providing a numeric value to ensure successful operation.

## Bug
The following code snippet will result in an error:
```javascript
//Incorrect usage of $inc operator
db.collection.updateOne({name: "John"}, {$inc: {age: '1'}});
```
## Solution
To avoid the error, provide a numeric value to the $inc operator:
```javascript
//Correct usage of $inc operator
db.collection.updateOne({name: "John"}, {$inc: {age: 1}});
```