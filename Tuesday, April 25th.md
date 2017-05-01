# Tuesday, April 25th - Javascript Fundamentals

This week we are focusing on JavaScript fundamentals, as well as some more language-agnostic ideas that will apply elsewhere.

* Standup
* Improv
* Show off your Meteor sketches!
* What is JavaScript?
  * Basic history, from NetScape to now.
  * Dynamically Typed, Weakly Typed
    * How this differs from other languages.
  * What are variables?
  * What are objects?
    * Creating objects
      * Object Literals, and Object Constructors
    * Arrays
  * Conditionals
    * If, Else, Else If
    * Switch Statements
  * Comparisons


## JavaScript History

First of all, don't mistake JavaScript with Java. JavaScript, originally called "Mocha", is a scripting language created in 1995 by Brendan Eich, at NetScape.

The original goal was to create a language that could work within the NetScape browser (it was notoriously rushed, taking Eich 10 days to write). As time passed, Microsoft and other companies became interested, and eventually, the ECMAScript specification was created, to allow different, but similar implementations of scripting languages. ECMAScript is a standard, not a language of it's own.

JavaScript was initially seen as an alternative to programming Java applets, and was therefore seen as a language for more unskilled programmers. Over time, obviously, this has changed. It's important to remember the core technologies of the time. HTML, CSS, and JavaScript ruled the landscape, along with PHP, ASP.NET, and others. It was only meant to fill the role of programming on the browser, and until recently, that's how it has stayed.

### Weak, Dynamically Typed

You might hear of JavaScript being weak, dynamically typed. Let's break that down.

A dynamically typed language only cares about the type of information that is being used, during runtime. In a statically typed language, the type of information will be checked *at compile time*, while a dynamically typed language will check the type *at runtime*. In JavaScript, you don't specify the type of every variable, the language will try to figure that out for you *while it is running*.

A weakly typed language is a vague term, but really it just refers to how strict it is (which, as you can guess now, JavaScript is pretty forgiving). If you are adding a number to a string, JavaScript will do it's best to do what it thinks you *want to do*, but this can sometimes cause issues. Other languages, like C, will not run at all if you try to add a number to a string, without specifically telling it how those types should be converted.

## Variables

This brings me to variables. Variables, put simply, are named containers for data. JavaScript deals in only a few types of information:

* Numbers
* Strings
* Booleans
* NULL, or undefined

Since JavaScript is both dynamic, and particularly forgiving, you don't have to constantly think of these types, but there are times that it will be required to know of their underlying purpose.

In JavaScript, variables are simply created using the `var` keyword.

Variables can be one piece of information, or they can refer to a collection of other variables, which brings us to arrays and objects.

### Objects

Most things in JavaScript are technically objects. Objects are really just `name:value` pairs that allow the storage of multiple pieces of information. Objects have members, and members can be new variables (member properties), or even other functions (member methods).

Objects can be created in a few different ways in JavaScript. First, we can create objects using *object literals*.

```
var SomeThing = {
  myProperty: 'some value',
  myOtherProperty: 'some other value'
}
```

And objects can also be created using an *Object Constructor*

```
function SomeThing(){
  this.myProperty = 'some value';
  this.myOtherProperty = 'some other value';

  this.myMethod = function(){
    return true;
  }
}

var myObj = new SomeThing();
```

These are equivalent.

//go over more about prototypes

### Arrays

Arrays are actually objects, with their own set of methods (push(), splice(), etc), but the information is *ordered*. We use *indices* in arrays to point to information at a certain location, but these are numerically ordered collections of information.

```
//initialized an array
var myArray = [];

myArray.push("Hello");// [0]
myArray.push("Everyone");// [1]
myArray.push("My");// [2]
myArray.push("Name");// [3]
myArray.push("Is");// [4]
myArray.push("Austin");// [5]

// myArray = ["Hello", "Everyone", "My", "Name", "Is", "Austin"];
```


### Numbers and Precision

I feel like many people assume that the math done within a language is just going to be *perfect*. This is absolutely not true, and it comes down to the different ways that we interact with numbers. In other languages, there are a few different kinds of numbers.

* Integer
* Float
* Double

Integers are your whole numbers, floats are your decimal point numbers, and then doubles are floating point numbers that are *twice as precise as floats*. In JavaScript, every number is technically a 64 bit floating point number. This means the numbers are accurate to up to 15 digits. Past that, we begin rounding numbers. If you are dealing with incredible precision, you will want to use special, large decimal point data types, but for the most part, just be aware of the fact that there is rounding at a certain point, and the math will not be *perfect* in some circumstances.

## Conditionals

In programming, we constantly have to check if some kind of condition has been met before something else can happen. You are already familiar with if statements, but there are a few ways to play with conditionals past that.

A conditional in it's most basic form is this:

```
if(condition){
  then execute code
}
```

But we can chain together some of these conditionals:

```
if(condition){
  then execute code
}else{
  execute other code
}
```

And finally, we can reinsert new if statements in the chain:

```
if(condition){
  then do this
}else if(other condition){
  if it fails the first conditional, but passes the second.
}else{
  if all else fails
}
```

There are also *Switch Statements*, which can be useful in certain situations:

```
switch(value to test) {
  //if the value we are testing is "This"...
  case "This":
    code
    break;
  //Otherwise, if the value we are testing is "That"...
  case "That":
    code
    break;
  //and if it fulfills none of the conditions, we will do this:
  default:
    code
}
```

## Comparisons

Obviously, when you are defining conditions, you are checking a value against another, comparing them. Comparison operators allow us to do this, and they return either true or false.

```
//if the values are equal
value1 == value2

//if the values are equal, both in content and in type
value1 === value2

//if the values aren't equal
value1 != value2

//if the values aren't equal, or if the types aren't equal
value1 !== value2

//greater than
value1 > value2

//greater than or equal to
value1 >= value2

//same goes for less than
```

We can also string some conditionals together:

```
//&& - AND
if(value1 > value2 && value1 < value3){

}

//|| - OR
if(value1 > value2 || value1 < value3){

}

//and we can also just check if something is not fulfilling a condition, using !:
if(!(value1 > value2)){

}
```
