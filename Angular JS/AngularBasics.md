

## Javascript Enumerables
http://zduck.com/2013/non-enumerable-properties-in-javascript/

The For In loop allows you to loop through each property in an object. The code below will display the property name.

```javascript
var dog ={
  name: 'Ghost',
  color: 'White'
}
 
for (var propertyName in dog){
    console.log(propertyName + ':' + dog[propertyName])
}
```

Now lets make enumerable false on the name  property.
Now even though we are looping over all the properties in our Object , the name property is not returned in the loop.

```javascript
var dog ={
  name: 'Ghost',
  color: 'White'
}
 
Object.defineProperty(dog, 'name' , {enumerable:false})
for (var propertyName in dog){
    console.log(propertyName + ':' + dog[propertyName])
}
```
Setting enumerable to false also makes it so that the object will not appear in the Object Keys.
Setting enumerable to false affects json serialization as the property will not appear in the json.

```javascript
'use strict'
 
var dog ={
  name: {first : 'Ghost', last : 'Snow'},
  color: 'White'
}
 
Object.defineProperty(dog, 'name',{enumerable : true});
for (var propertyName in dog){
  display(propertyName + ':' + dog[propertyName]);
}
 
console.log(Object.keys(dog))
console.log(JSON.stringify(dog)
```
