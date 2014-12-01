#JavaScript Cheatsheet

**Variables**
```javascript

// number
var num1 = 5;
num1; //returns 5

// boolean
var hasCar = false;
hasCar; //returns false

// string
var myName = 'Joe';
myName; // returns 'Joe'
```
**Arrays**
```javascript

// array
var names = ['Adam', 'Sam', 'Joe'];
names; //returns ['Adam', 'Sam', 'Joe']

// returns 3
names.length;

// returns 'Adam'
names[0]; 

// changes 'Adam' to 'Billy'
names[0] = Billy;

// returns 'Sam'
names[1];

// returns 'Joe' 
names[2]; 

```
**Functions**
```javascript

// defining and storing the function into a variable:

var returnVolumeBox = function(length, width, height){
	var area = length * width * height;
	return area;
};

// calling the function:
// returns 40

returnVolumeBox(4, 5, 2); 
```
**Hash:  {key:value} pairs**
```javascript
var car = {
  brand: 'Honda',
  milesPerGallon: 30,
  'license plate': 'DB22MG',
  dimensions: {
  	length: 20,
  	width: 10,
  	height: 5
  },
  passengers: [
  	{
  		firstName: 'Joe',
  		lastName: 'Smith',
  		age: 30
  	},{
  		firstName: 'Jane',
  		lastName: 'Smith',
  		age: 29
  	},{
  		firstName: 'Brad',
  		lastName: 'Cooper',
  		age: 16
  	},{
  		firstName: 'Sarah',
  		lastName: 'Smith',
  		age: 15
  	}
  ],
  numPassengers: function(){
  	return this.passengers.length;
  },
  remainingRange: function(currentGallonsOfGas){
  	var range = this.milesPerGallon * currentGallonsOfGas;
  	return range;
  }
};

```
**Accessing, Editing, and Adding Values**
```javascript

// adds a new {key:value pair} :

car.color = 'black';

// you cannot add keys without first creating the parent keys first:

// doesn't work
car.model.designation = 'RSX'; 

// works
car.model = {};
car.model.designation = 'RSX';

// returns 'Honda' in dot notation and square bracket notation
car.brand;
car['brand'];

// changes 'Honda' to 'Ford'
car.brand = 'Ford';
car['brand'] = 'Ford';

// returns 'DB22MG'
car['license plate'];

// returns 20
car.dimensions.length;
car['dimensions']['length'];
car['dimensions'].length

// square bracket notation can evaluate code
var xyz = 'length';
car.dimensions[xyz];

// returns 'Cooper'
car.passengers[2].lastName;

// returns 4
car.numPassengers();

// returns 300
car.remainingRange(10);

// returns 60
var myGallons = 2;
car.remainingRange(myGallons);

var litersToGallons = function(liters){
	var gallons = liters * 0.26417;
	return gallons;
};

// returns 79.251
car.remainingRange( litersToGallons(10) );

// returns 1000
returnVolumeBox(car.dimensions.length, car.dimensions.width, car.dimensions.height);
```
**Loops**
```javascript
var names = ['Adam', 'Sam', 'Joe'];

// console logs 
// 'Adam' 
// 'Sam' 
// 'Joe'

for(var i = 0; i < names.length; i++){
  console.log(names[i]);
};

// console logs 
// 'Adam' 
// 'Sam' 
// 'Joe'

var i = 0;
while(i < names.length){
  console.log(names[i]);
  i++;
};

// console logs 
// 'Adam' 
// 'Sam' 
// 'Joe'

var i = 0;
do {
  console.log(names[i]);
  i++;
} while (i < names.length);

```
**Using loops in functions**
```javascript
var moreNames = ['Zack', 'Zoey', 'Zakeria'];
var consoleArrayItems = function(array){
	for(var i = 0; i < names.length; i++){
	  console.log(names[i]);
	};
};
// console logs 
// 'Zack' 
// 'Zoey' 
// 'Zakeria'
consoleArrayItems(moreNames);

```
**For-In Loops for Arrays**
```javascript
var moreNames = ['Zack', 'Zoey', 'Zakeria'];

// console logs 
// 'Zack' 
// 'Zoey' 
// 'Zakeria'
for(index in moreNames){
  console.log(moreNames[index]);
};

var consoleLogNames = function(array){
	for(index in array){
	  console.log(array[index]);
	};
};

// console logs 
// 'Zack' 
// 'Zoey' 
// 'Zakeria'
consoleLogNames(moreNames);

```
**For-In Loops for Hashes**
```javascript

var car = {
  brand: 'Honda',
  milesPerGallon: 30,
  color: 'black'
};
 
// console logs
// brand is Honda
// milesPerGallon is 30
// color is black
 
for(key in car){
  console.log(key + " is " + car[key])
};

var consoleHash = function(myHash){
	for(prop in myHash){
	  console.log(prop + " is " + myHash[prop])
	};
};

// console logs
// brand is Honda
// milesPerGallon is 30
// color is black

consoleHash(car);

```
