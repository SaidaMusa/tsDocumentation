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

