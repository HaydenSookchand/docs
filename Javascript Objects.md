# Javascript Objects


## About

The purpose of this page is to quickly go through all the ways objects are created in Javascript.

## Literals and Constructors


An object literal is the easiest way to create an object in JavaScript.

It is basically a comma-separated list of name-value pairs wrapped in curly braces.

Object literals are great if you don't require instance methods. Object literals are therefore singletons meaning that a change to the object will affect the entire script.

A constructor is simply a function paired with the new keyword. A constructor makes it possible to have multiple instances of that object.

```javascript
//Object Literal
 
var dog= {name: "Frosty",color:"white"};
console.log(dog)
 
//------------------------------------------------------------------------------
//Constructor Functions
 
function Dog(name,color){
  this.name = name
  this.color = color
}
var dog= new Dog("Dumbo","grey");
console.log(dog)
 
//------------------------------------------------------------------------------
```

## ES6 Objects
```javascript
//------------------------------------------------------------------------------
//ES6 Classes
In ECMA Script 6 some syntactic sugar has been added to create objects using a class structure
 
class Cat {
  constructor(name, color){
    this.name = name
    this.color = color
  }
}
 
var cat = new Cat("Garfield","red");
console.log(cat)
//------------------------------------------------------------------------------
```
## Object.create()

Object.create is what Javascript does "under the hood". When declaring Objects in the ways demonstrated above.

```javascript
//------------------------------------------------------------------------------
// Object.create (underneath the literal and constructor functions)
 
var hippo = Object.create(Object.prototype,{
  name : {
    value: 'Rex',
    enumerable:true,
    writable:true,
    configurable:true
  },
   color : {
    value: 'blue',
    enumerable:true,
    writable:true,
    configurable:true
  }
})
 
console.log(hippo)
//------------------------------------------------------------------------------
```
## Summary
Below is a summary of the various ways that JavaScript Objects can be used.
```javascript
'use strict';
//------------------------------------------------------------------------------
//Object Literal
 
var dog = {
    name: "Frosty",
    color: "white"
};
display(dog);
 
//------------------------------------------------------------------------------
//Object Literal with function
 
var dog2 = {
    name: "Oreo",
    color: "brown-white"
};
 
dog2.speak = function() {
    display('Hello I am Oreo');
}
 
dog2.speak()
//------------------------------------------------------------------------------
//Constructor
 
function Elephant(name, color) {
    this.name = name
    this.color = color
}
var elephant = new Elephant("Dumbo", "grey");
display(elephant);
 
//------------------------------------------------------------------------------
//Constructor with functions
 
function Elephant(name, color) {
    this.name = name
    this.color = color
    this.speak = function() {
        display('I am an elephant');
    }
}
var elephant = new Elephant("Dumbo", "grey");
display(elephant.speak());
 
//------------------------------------------------------------------------------
// Object.create (underneath the literal and constructor functions)
 
var hippo = Object.create(Object.prototype, {
    name: {
        value: 'Rex',
        enumerable: true,
        writable: true,
        configurable: true
    },
    color: {
        value: 'blue',
        enumerable: true,
        writable: true,
        configurable: true
    }
})
 
display(hippo);
//------------------------------------------------------------------------------
//ES6 Classes
 
class Cat {
    constructor(name, color) {
        this.name = name
        this.color = color
    }
}
 
var cat = new Cat("Garfield", "red");
//------------------------------------------------------------------------------
```

## References
https://stackoverflow.com/questions/4597926/what-is-the-difference-between-new-object-and-object-literal-notation

https://stackoverflow.com/questions/4859800/should-i-be-using-object-literals-or-constructor-functions

https://www.internalpointers.com/post/object-literals-vs-constructors-javascript

https://www.youtube.com/watch?v=O3JSPhwKowA
