
## About

The purpose of this page is to quickly go through Javascript properties.
https://plnkr.co/edit/Lt6qmkHTBYM8BHSrsd8I

## Writeable

If we set writable to true then the value of that property can be written over.

```javascript
var dog ={
  name: 'Ghost',
  color: 'White'
}
 
Object.defineProperty(dog,'name', {writable: true})
console.log('Original Name: ' + dog.name);
dog.name = "Summer";
console.log("Changed Name: " + dog.name)
console.log(Object.getOwnPropertyDescriptor(dog,'name'));
```
If we set writable to false and try to change it, it will break.
 ```javascript
var dog ={
  name: 'Ghost',
  color: 'White'
}
 
Object.defineProperty(dog,'name', {writable: false})
console.log('Original Name: ' + dog.name);
// code will break at this point.
dog.name = "Summer";
console.log("Changed Name: " + dog.name)
console.log(Object.getOwnPropertyDescriptor(dog,'name'));*/
```
If we set writable to false on the parent but try to change the property on the child, we can. 
This makes sense because the writable is not actually set to the value of the child but the pointer of the parent.
```javascript
var dog ={
  name: {first : 'Ghost', last : 'Snow'},
  color: 'White'
}
 
Object.defineProperty(dog,'name', {writable: false})
console.log("Original First Name: " + dog.name.first);
dog.first = "Summer";
console.log("Changed First name: " +dog.first);
console.log(Object.getOwnPropertyDescriptor(dog,'first'));
```

## Configurable
doesn't allow you to change configurable or enumerable to true after false, cannot delete properties after this is set to false

```javascript
Object.defineProperty(dog2, 'name',{configurable : false});
// this will not happen
Object.defineProperty(dog2, 'name',{configurable : true});
// this will not happen
Object.defineProperty(dog2, 'name',{enumerable: false});
// this will happen
Object.defineProperty(dog2, 'name',{writeable: false});
```

## Getters and Setters
https://www.youtube.com/watch?v=IbqCWoFO410

```javascript
var dog ={
  name: {first : 'Ghost', last : 'Snow'},
  color: 'White'
}
 
Object.defineProperty(dog, 'fullName'
,{
  get  : function() {
    return this.name.first + ' ' + this.name.last
  },
   set  : function(value) {
   var nameParts = value.split(' ')
   this.name.first = nameParts[0]
   this.name.last = nameParts[1]
  }
});
 
console.log(dog.fullName);
dog.fullName = "Summer Time"
console.log(dog.fullName);
console.log(dog.name.first);
console.log(dog.name.last)
```
