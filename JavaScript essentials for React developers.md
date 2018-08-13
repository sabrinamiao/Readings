# JavaScript essentials for React developers

## Variable Declaration

### var - Used to declare variables but the scope of variables is function block. if declared globally, scope is global

### let - Used to declare variables but variables are block scoped

### const - Used to declare variables but variable can't be reassigned. Declared variables are immutable. const variables are also block scoped

## Classes

### function keyword is not used to declare functions. We don't need to have the word function for declaring methods

### We can't assign properties as we do in methods. We initialize them using constructor method

### constructor method is special method which is called on creation of objects and used to initialization

### this is always point to current object

## Inheritance

### Inheritance is the mechanism of creating a new class(child class) from another class(parent class)

### super() method is mandatory to call if we have declared custom constructor for Child Class, else not required

### super is used to call Parent Class methods inside Child Class

### Child Class will have access to all parent class methods

### this will always point to current object

## Arrow functions

### this in arrow functions always inherits this object from the context in which code is defined. We don't need to do ```that = this``` or ```self = this``` or ```.bind(this)```

### this always points to current objects in arrow functions

## Array.map()

### This method doesn't modify original array, it returns a new array

## Template Literals

## Multi-line Strings

## Object Destructuring

## Spread Operator

### Spread operator is used to extract all array items or object properties. To create objects we use {...} and to create arrays we use [...]

## Modules

### We use export keyword before class and variables to make them available for other modules. import keyword is used to import variables or classes from other modules
