# JavaScript Objects in Detail
-------------------------------

## Own and Inherited Properties

Objects have inherited properties and own properties. The own properties are properties that were defined on the object, while the inherited properties were inherited from the object’s Prototype object.

To find out if a property exists on an object (either as an inherited or an own property), you use the in operator:
```javascript
// Create a new school object with a property name schoolName​
​var school = { 
  schoolName:"MIT" 
 };
​
​// Prints true because schoolName is an own property on the school object​
console.log("schoolName" in school);  // true​
​
​// Prints false because we did not define a schoolType property on the school object, 
// and neither did the object inherit a schoolType property from its prototype object Object.prototype.​
console.log("schoolType" in school);  // false​
 
​// Prints true because the school object inherited the toString method from Object.prototype. ​
console.log("toString" in school);  // true
```

## hasOwnProperty
To find out if an object has a specific property as one of its own property, you use the hasOwnProperty method. This method is very useful because from time to time you need to enumerate an object and you want only the own properties, not the inherited ones.
```javascript
// Create a new school object with a property name schoolName​
​var school = {
  schoolName:"MIT"
};
​
​// Prints true because schoolName is an own property on the school object​
console.log(school.hasOwnProperty ("schoolName"));  // true​
 
​// Prints false because the school object inherited the toString method from Object.prototype, 
// therefore toString is not an own property of the school object.​
console.log(school.hasOwnProperty ("toString"));  // false 
```
