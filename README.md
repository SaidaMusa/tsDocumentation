# tsDocumentation

Type script is type safety.It is like while writing a code you can know it . A lot of people think that ts is a new programming language but honestly it is not 100%.It is static vhecking language such as JAVA , GOLANG.Which means 
it is checked by IDE's.Not js is like that whatever you write it is ok for js or maybe sometimes you can only know from browser or terminal hah and that's wrong and ts is just development tool.

### 27:40


### Types

number,string,boolean,underfined,null,void,object,array,tuple and any,never, unknown and so on.

### syntax

let variableName : type = value

36:31

### Primitive types

String,number and boolean

###Number
There is no int float thing in ts just like js.Because JS doesnt have special runtime value for integers.It is for saving memory and whatever you write it just callbacks number maybe it is 5.5 or 4

43:31


###Annotations



let count: number; - here number is annotation




### compile error

let counter: number;
counter = 'Hello'; // compile error 


### array type annotations


let arrayName: type[];


### string array

let names: string[] = ['John', 'Jane', 'Peter', 'David', 'Mary'];



### objects

let person: {
  name: string;
  age: number;
};

person = {
  name: 'John',
  age: 25,
}; 



### Function arguments & return types


let greeting : (name: string) => string;


greeting = function (name: string) {
    return `Hi ${name}`;
};




### type inference

let counter = 0;

It is equivalent to the following statement:

let counter: number = 0;


### function

function increment(counter: number) {
    return counter++;
}


It is the same as:

function increment(counter: number) : number {
    return counter++;
}



### Number

we have only numbers.if we have big integers we count them as a bigInt number.


### decimal numbers

let counter: number = 0;
let x: number = 100, 
    y: number = 200;


### binary numbers

The binary number uses a leading zero followed by a lowercase or uppercase letter  0b or 0B :


let bin = 0b100;
let anotherBin: number = 0B010;



### Octal numbers

let octal: number = 0o10;


### Big Integers
The big integers represent the whole numbers larger than 253 – 1. A Big integer literal has the n character at the end of an integer literal like this:

let big: bigint = 9007199254740991n;




### String

## With using backtick you can extra line your string.

let description = `This TypeScript string can 
span multiple 
lines
`;


### Boolean

&& - AND
|| - OR
!- NOT


## functions
function changeStatus(status: boolean): boolean {
   //...
}


### Object

# Option 1:
let employee: {
    firstName: string;
    lastName: string;
    age: number;
    jobTitle: string;
};


employee = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25,
    jobTitle: 'Web Developer'
};


# Option 2:

let employee: {
    firstName: string;
    lastName: string;
    age: number;
    jobTitle: string;
} = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25,
    jobTitle: 'Web Developer'
};

### Object vs object

The object type represents all non-primitive values while the Object type describes the functionality of all objects.

# object
let user = { name: "Ali" }; // object
let list = [1, 2, 3];        // object


## Object

let obj = new Object(); // Object konstruktori
console.log(Object.keys({a: 1})); // Object funksionalligi




### Empty type obj

The empty type {} describes an object that has no property on its own. If you try to access a property on such an object, TypeScript will issue a compile-time error:

let vacant: {};
vacant.firstName = 'John';

OUTPUT: error TS2339: Property 'firstName' does not exist on type '{}'.

But you can access all properties and methods declared on the Object type:

let vacant: {} = {};
console.log(vacant.toString()); 
OUTPUT: [object Object]




### Array

let arrayName: type[];

## Array of strings

let str : String[] = []


## 2 array of strings

let skills: string[];
skills = ['Problem Sovling','Software Design','Programming'];

##Storing values of mixed types

let scores : (string | number)[];
scores = ['Programming', 5, 'Software Design', 4]; 



### Tuple

A tuple works like an array with some additional considerations:

1.The number of elements in the tuple is fixed.
2.The types of elements are known, and need not be the same.



let skill: [string, number];
skill = ['Programming', 5];

But here it's value must be in order instead you will get an error.


let skill: [string, number];
skill = [5, 'Programming'];

error:

error TS2322: Type 'string' is not assignable to type 'number'.



## rgb color

For example, you can use a tuple to define an RGB color that always comes in a three-number pattern:

(r,g,b)


For example: 

let color: [number, number, number] = [255, 0, 0];

The color[0], color[1], and color[2] would be logically mapped to Red, Green and Blue color values.




let bgColor, headerColor: [number, number, number, number?];
bgColor = [0, 255, 255, 0.5];
headerColor = [0, 255, 255];



### Enum

Enum is a box of consts

1.First, use the enum keyword followed by the name of the enum.
2.Then, define constant values for the enum.


The following shows the syntax for defining an enum:

enum name {constant1, constant2, ...};



## Enum months of the year

enum Month {
    Jan,
    Feb,
    Mar,
    Apr,
    May,
    Jun,
    Jul,
    Aug,
    Sep,
    Oct,
    Nov,
    Dec
};


Named Month is enum and type of the month is constants.



## enum example with switch

function isItSummer(month: Month) {
  let isSummer: boolean;
  switch (month) {
    case Month.Jun:
    case Month.Jul:
    case Month.Aug:
      isSummer = true;
      break;
    default:
      isSummer = false;
      break;
  }
  return isSummer;
}


And you can call it like so:

console.log(isItSummer(Month.Jun)); // true



### Month of numbers

var Month;
(function (Month) {
    Month[Month["Jan"] = 0] = "Jan";
    Month[Month["Feb"] = 1] = "Feb";
    Month[Month["Mar"] = 2] = "Mar";
    Month[Month["Apr"] = 3] = "Apr";
    Month[Month["May"] = 4] = "May";
    Month[Month["Jun"] = 5] = "Jun";
    Month[Month["Jul"] = 6] = "Jul";
    Month[Month["Aug"] = 7] = "Aug";
    Month[Month["Sep"] = 8] = "Sep";
    Month[Month["Oct"] = 9] = "Oct";
    Month[Month["Nov"] = 10] = "Nov";
    Month[Month["Dec"] = 11] = "Dec";
})(Month || (Month = {}));



Output:
{
  '0': 'Jan', 
  '1': 'Feb', 
  '2': 'Mar', 
  '3': 'Apr', 
  '4': 'May', 
  '5': 'Jun', 
  '6': 'Jul', 
  '7': 'Aug', 
  '8': 'Sep', 
  '9': 'Oct', 
  '10': 'Nov',
  '11': 'Dec',
  Jan: 0,     
  Feb: 1,     
  Mar: 2,     
  Apr: 3,     
  May: 4,
  Jun: 5,
  Jul: 6,
  Aug: 7,
  Sep: 8,
  Oct: 9,
  Nov: 10,
  Dec: 11
}


### TypeScript any Type

The TypeScript any type allows you to store a value of any type. It instructs the compiler to skip type-checking.
Use the any type to store a value that you don’t know its type at the compile-time or when you migrate a JavaScript project over to a TypeScript project.

### Unknown type


let result: unknown;

result = 1;
result = 'hello';
result = false;
result = Symbol();
result = { name: 'John' };
result = [1, 2, 3];



Feature	any	unknown
Type Safety	No type-safety	Enforces type safety
Operations	Operations can be performed without checks	Operations cannot be performed without type assertion (narrowing type)
Use cases	Useful for dynamic values but unsafe.	Useful for dynamic values and safe because it requires validation before use.
Type Checking	TypeScript compiler does not perform a type checking on an any variable.	TypeScript compiler enforces a type checking on an unknown variable.
Common Scenarios	Used for migrating JavaScript codebase to TypeScript.	Used when handling data from external sources (API calls, databases, ..) where type validation is necessary.



### For


## first look
let i = 0;
for (; ;) {
    console.log(i);
    i++;
    if (i > 9) break;
}

### second look

for (let i = 0; i < 10; i++) {
    console.log(i);
}



### while

let counter = 0;

while (counter < 5) {
    console.log(counter);
    counter++;
}


### do while

let i = 0;

do {
    console.log(i);
    i++
} while (i < 10);

