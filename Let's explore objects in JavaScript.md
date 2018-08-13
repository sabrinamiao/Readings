# Let's explore objects in JavaScript

## Objects are dynamic collections of properties, with a "hidden" property to the object's prototype

## A property has a key and a value

## Property key

### The property key is a unique string

### There are 2 ways to access properties: dot notation adn bracket notation

### When the dot notation is used, the property key must be a valid identifier

### When the bracket notation is used, the property key does not have to be a valid identifier - it can have any value

### When a non string is used as the property key, it will be converted to a string (via the ```toString()``` method, when available)

## Property value

### The property value can be a primitive, object, or function

### Objects can be nested inside other objects

### When a function is used as a value for a property, it usually becomes a method. Inside methods, the ```this``` keyword is used to refer to the current object

### ```this```, however, can have many values depends on how the function was invoked

## Dynamic nature

### Objects are dynamic by nature. Properties can be added or deleted at any time

## Map

### Accessing a key doesn't require you to scan through all the properties. It's an 0(1) access time

## Prototype

### Objects have a "hidden" link ```__proto__``` to a prototype object, from which they inherit properties

### Empty Object

### The empty object ```{}``` is not really empty as it contains a link to the ```Object.prototype```. To create a true empty object, we can use ```Object.create(null)```

### Prototype chain

### The prototype object has a prototype of its own. When a property is accessed and the object does not contain it, JavaScript will look down the prototype objects until it either finds the requested property, or until it reaches null

## Primitives and Object Wrappers

### JavaScript treats primitives like objects in the sense that it allows access to properties. Primitives, of course, are not objects

### Numbers, strings and booleans have object equivalent wrappers. These are the ```Number```, ```String```, and ```Boolean``` functions

### ```null``` and ```undefined``` primitives have no corresponding wrapper objects and provide no methods


## Built-in Prototypes

### Numbers inherit from ```Number.prototype```, which inherits from ```Object.prototype```

### Strings inherit from ```String.prototype```

### Booleans inherit from ```Boolean.prototype```

### Arrays inherit from ```Array.prototype```

### Functions are objects and inherit from ```Function.prototype```. They have methods like ```bind()```, ```apply()``` and ```call()```

### All objects, functions, and primitives (except ```null``` and ```undefined```) inherit properties from ```Object.prototype```. All of them have the ```toString()``` method

## Augmenting built-in objects with polyfills

### A polyfill is piece of code that implements a feature in browsers that don't support that feature

### Utilities

### the polyfill for ```Object.assign()``` adds a new function on ```Object``` if it's not available

### the polyfill for ```Array.from()``` adds a new function on ```Array``` if it's not available

### Prototypes

### New methods can be added on prototypes

### ```String.prototype.trim()``` polyfill makes the ```trim()``` method available on all strings

### ```Array.prototype.find()``` makes the ```find()``` methods available on all arrays, same as ```Array.prototype.findIndex()```

## Single Inheritance

### ```Object.create()``` creates a new object with a specified prototype object. It is used for single inheritance

```javascript
let bookPrototype = {
  title: undefined,
  author: undefined,
  getFullTitle: function () {
    return this.title + " by " + this.author
  }
}

let book = Object.create(bookPrototype)
book.title = "JavaScript: The Good Parts"
book.author = "Douglas Crockford"
book.getFullTitle() // JavaScript: The Good Parts by Douglas Crockford
```

## Multiple Inheritance

### ```Object.assign()``` copies properties from one or more objects to a target object. It can be used for multiple inheritance

```javascript
let authorDataService = {
  getAuthors: functon () {}
}
let bookDataService = {
  getBooks: function () {}
}
let userDataService = {
  getUsers: function () {}
}

let dataService = Object.assign({},
authorDataService,
bookDataService,
userDataService)

dataService.getAuthors()
dataService.getBooks()
dataService.getUsers()
```

## Immutable Objects

### ```Object.freeze()``` freezes an object. Properties can't be added, deleted or changed

## Clone

### ```Object.assign()``` can be used to clone objects

## Object literal

### Object literal offers a simple, elegant way of creating objects, but has a few drawbacks. All properties are public, methods can be redefined, and we can't use the same methods for new instances

## Function Constructor

### All functions can be used as function constructors. A function constructor is called with ```new```. The new object will have the prototype set to FunctionConstructor.prototype

## Class

### The object built with class has the prototype set to ClassName.prototype. The ```new``` operator must be used when creating an object with a class

### The class syntax doesn't freeze the prototype, so we need to do that after

## Prototype-based inheritance

### The prototype inheritance has the benefit of memory conservation. The prototype is created once and used by all instances

### No Encapsulation

### The prototype-based inheritance patterns have no privacy. All object's properties are public

### The pretended privacy pattern involves marking private properties with ```_```, so that others will avoid using them

## Factory Functions

### JavaScript offers a new way of creating encapsulated objects using factory functions
