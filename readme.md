#Arrays and objects in Javascript

##Arrays in JavaScript:
An array is a data structure used to store a collection of elements. In JavaScript, arrays can hold elements of any data type, and they can dynamically grow or shrink in size. Arrays in JavaScript are zero-indexed, which means the first element is accessed with index 0, the second with index 1, and so on.

Here's how you can create an array in JavaScript:

```javascript
// Creating an array with square brackets
let fruits = ['apple', 'orange', 'banana'];
```

Common Array Methods in JavaScript:

1. `push`: Adds one or more elements to the end of an array and returns the new length of the array.

```javascript
fruits.push('mango');
// fruits will now be ['apple', 'orange', 'banana', 'mango']
```

2. `pop`: Removes the last element from an array and returns that element.

```javascript
let lastFruit = fruits.pop();
// lastFruit will be 'mango', and fruits will be ['apple', 'orange', 'banana']
```

3. `shift`: Removes the first element from an array and returns that element. This method also shifts the remaining elements one position down.

```javascript
let firstFruit = fruits.shift();
// firstFruit will be 'apple', and fruits will be ['orange', 'banana']
```

4. `unshift`: Adds one or more elements to the beginning of an array and returns the new length of the array.

```javascript
fruits.unshift('kiwi', 'pear');
// fruits will now be ['kiwi', 'pear', 'orange', 'banana']
```

5. `indexOf`: Returns the first index at which a given element can be found in the array, or -1 if it is not present.

```javascript
let indexOrange = fruits.indexOf('orange');
// indexOrange will be 2
```

6. `splice`: Changes the content of an array by removing existing elements and/or adding new elements.

```javascript
fruits.splice(1, 2, 'grape', 'watermelon');
// fruits will now be ['kiwi', 'grape', 'watermelon', 'banana']
```

7. `slice`: Returns a shallow copy of a portion of an array selected from start to end (end not included). The original array is not modified.

```javascript
let slicedFruits = fruits.slice(1, 3);
// slicedFruits will be ['grape', 'watermelon'], and fruits remains unchanged
```

8. `concat`: Returns a new array that concatenates two or more arrays.

```javascript
let moreFruits = ['pineapple', 'cherry'];
let allFruits = fruits.concat(moreFruits);
// allFruits will be ['kiwi', 'grape', 'watermelon', 'banana', 'pineapple', 'cherry']
```

##Now let's move on to Objects in JavaScript:

Objects in JavaScript:
An object is another fundamental data structure in JavaScript. Unlike arrays, which use numerical indices, objects use key-value pairs to store and retrieve data. Objects represent real-world entities and are commonly used to model complex data structures.

Here's how you can create an object in JavaScript:

```javascript
// Creating an object with curly braces
let person = {
  name: 'John Doe',
  age: 30,
  occupation: 'Software Engineer'
};
```

In this example, the object `person` has three properties: `name`, `age`, and `occupation`.

Accessing Object Properties:
You can access the properties of an object using dot notation or square brackets.

```javascript
let personName = person.name; // Using dot notation
let personAge = person['age']; // Using square brackets
```

You can also dynamically access properties using variables:

```javascript
let propertyName = 'occupation';
let personOccupation = person[propertyName];
```

Adding and Modifying Properties:
You can add new properties or modify existing ones in an object:

```javascript
person.email = 'john@example.com'; // Adding a new property
person.age = 31; // Modifying an existing property
```

Deleting Properties:
You can remove properties from an object using the `delete` keyword:

```javascript
delete person.email;
```

Iterating over Object Properties:
To iterate over the properties of an object, you can use `for...in` loop or `Object.keys()`.

```javascript
for (let key in person) {
  console.log(key, person[key]);
}

// Using Object.keys()
let keys = Object.keys(person);
for (let key of keys) {
  console.log(key, person[key]);
}
```

Object Methods:
In addition to properties, objects can also contain methods, which are functions stored as object properties.

```javascript
let calculator = {
  add: function(a, b) {
    return a + b;
  },
  subtract: function(a, b) {
    return a - b;
  }
};

let sum = calculator.add(5, 3); // sum will be 8
let difference = calculator.subtract(7, 2); // difference will be 5
```

