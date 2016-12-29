# JavaScript Objects in Detail
--------------------------------

## Reference Data Type and Primitive Data Types
One of the main differences between reference data type and primitive data types is reference data type’s value is stored as a reference, it is not stored directly on the variable, as a value, as the primitive data types are. For example:

```javascript
// The primitive data type String is stored as a value​
​var person = "Kobe";  
​var anotherPerson = person; // anotherPerson = the value of person​
person = "Bryant"; // value of person changed​
console.log(anotherPerson); // Kobe​
console.log(person); // Bryant
```

It is worth noting that even though we changed person to “Bryant,” the anotherPerson variable still retains the value that person had.

```javascript
var person = {name: "Kobe"};
​var anotherPerson = person;
person.name = "Bryant";
​
console.log(anotherPerson.name); // Bryant​
console.log(person.name); // Bryant
```
In this example, we copied the person object to anotherPerson, but because the value in person was stored as a reference and not an actual value, when we changed the person.name property to “Bryant” the anotherPerson reflected the change because it never stored an actual copy of it’s own value of the person’s properties, it only had a reference to it.
