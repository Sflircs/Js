# JavaScript Objects in Detail
--------------------------------

## What is an Object
An object is an unordered list of primitive data types (and sometimes reference data types) that is stored as a series of name-value pairs. Each item in the list is called a property (functions are called methods).

** var myFirstObject = { firstName: "Richard", favoriteAuthor: "Conrad" }; **

Property names can be a string or a number, but if the property name is a number, it has to be accessed with the bracket notation.
** var ageGroup = {30: "Children", 100:"Very Old"};
console.log(ageGroup.30) // This will throw an error​
​// This is how you will access the value of the property 30, to get value "Children"​
console.log(ageGroup["30"]); // Children​ **