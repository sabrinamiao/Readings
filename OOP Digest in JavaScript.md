# OOP Digest in JavaScript

## Basics - Refreshed

### Objects in JavaScript are free-form and mostly don't follow any structure. Their structure can be best compared to being similar Map objects in Java, consisting of key-value pairs

## The "new" keyword - a constructor function

### JavaScript has a new keyword that allows for objects to be created using constructor functions which are different to normal functions. They act similarly to the constructors in Java

### Calling a function designed to be invoked as a constructor function does not return an object, instead it sets properties on it's parent/enclosing object. The this keyword in a constructor function refers to the object it will return. When invoked normally, it will refer to the object that the function is a property of

## Using "call" to fix which "this" is this

### By using call, we can bind an object to a function, supplanting the parent/enclosing object, so that the this keyword refers to our bound object

## Prototypes

### JavaScript doesn't have the comparable class structures as traditional OOP languages such as Java. Behaviors (methods/functions etc) in JavaScript do not belong to a class, so much as they do in the likes of Java. JavaScript objects are a collection of properties, of which a function is simply assigned to a property

### The prototype is essentially a reference to another object it inherits from. Constructor function prototypes have a two-way reference to itself

### Prototypes (and Prototype chains) are JavaScript's implementation of Object inheritance

### Where it differs with typical OOP in languages such as Java is that the prototype object is accessible to objects created before and after any changes to the prototype

### It is really important to note that __proto__ is controversial and it's use directly is generally discouraged. You can use the Object.getPropertyOf(obj) instead. Changing an object's prototype is considered a slow operation that should be avoided

## Class

### MDN defines it as syntactical sugar over JavaScript's existing prototype-based inheritance

### The "new" requirement

#### Class objects require definition using the new keyword. By default, classes are given empty constructors if none are defined. If you try to set an object without using the constructor function, you will receive an error

### Named/Unnamed expression

### Strict mode

#### Classes use strict mode

### Getters and Setters

#### You can use the property name when accessing on the object rather than executing the function

### Functions-only

#### Classes cannot contain instance properties. All properties must defined using functions. Instance properties can be returned via functions
