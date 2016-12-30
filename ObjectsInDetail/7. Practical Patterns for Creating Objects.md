# JavaScript Objects in Detail
---------------------------------

Here are two common patterns for creating objects. If you have done the Learn JavaScript Properly course, you would have seen the lessons in the Code Academy used this first pattern frequently:

**I recomended that you should use the first pattern.**

### 1. Constructor Pattern for Creating Objects (Recomended)
```javascript
function Fruit (theColor, theSweetness, theFruitName, theNativeToLand) {​
    this.color = theColor;
    this.sweetness = theSweetness;
    this.fruitName = theFruitName;
    this.nativeToLand = theNativeToLand;
    this.showName = function () {
        console.log("This is a " + this.fruitName);
    }
    this.nativeTo = function () {
    this.nativeToLand.forEach(function (eachCountry)  {
          console.log("Grown in:" + eachCountry);
        });
    }
}
```
### 2. Prototype Pattern for Creating Objects (Unrecomended)
```javascript
function Fruit () {
}
​
Fruit.prototype.color = "Yellow";
Fruit.prototype.sweetness = 7;
Fruit.prototype.fruitName = "Generic Fruit";
Fruit.prototype.nativeToLand = "USA";
​
Fruit.prototype.showName = function () {
  console.log("This is a " + this.fruitName);
}
​
Fruit.prototype.nativeTo = function () {
  console.log("Grown in:" + this.nativeToLand);
}
```
