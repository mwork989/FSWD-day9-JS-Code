Looping statements in JS
----------------------------

JavaScript provides several looping statements that allow you to repeatedly execute a block of code. Here are the main looping statements in JavaScript:


1.for Loop:
The for loop is used to iterate over a sequence of values, such as numbers. It consists of three parts: initialization, condition, and increment/decrement.

//ES5
for(var i=0;i<5;i++){
  console.log(i);
}

// Es6 

for(let i=0;i<5;i++){
  console.log(i);
}


2. while Loop:
The while loop repeatedly executes a block of code as long as a specified condition is true.

let i = 0;
while (i < 5) {

    console.log(i);
    i++;
}


3.do...while Loop:
Similar to the while loop, the do...while loop executes a block of code as long as a specified condition is true. The difference is that the do...while loop always executes the block of code at least once, even if the condition is false.


let i = 0;
do {
    // code to be executed in each iteration
    console.log(i);
    i++;
} while (i < 5);



4. for...in Loop:
The for...in loop is used to iterate over the properties of an object. It ellobrates and provides the properties(keys) of an object

const emp ={
    name:"david",
    age:32,
    designation:"software engineer"
}

5.for...of Loop:
The for...of loop is used to iterate over the values of an iterable object, such as arrays or strings.


const arr = [1, 2, 3];
for (let value of arr) {
   
    console.log(value);
}


for (let value of Object.keys(emp)) {
   
    console.log(value);
}


when to use which loop
--------------------

The choice between using a for loop and a while loop in JavaScript often depends on the specific situation and the requirements of your code.

when Definite Number of Iterations, Loop through Arrays, Object properties - for loop
If you know the exact number of iterations beforehand, a for loop is a concise and expressive way to handle the iteration.

when we dont know the exact number of iterations and iterations based on condition - while loop
when If you don't know the exact number of iterations and the loop should continue until a certain condition is met, a while loop is more appropriate.


Operators
------------------------

JavaScript supports a variety of operators that are used to perform operations on variables and values.

Arithmetic Operators
----------------------
+ Addition        : e.g. let result = 5 + 3; // output 8
- Subtraction     : e.g. let result = 5 - 3; // output 2
* Multiplication  : e.g. let result = 5 * 3; // output 15
/ Division        : e.g. let result = 6 / 2; // output 3
% Modulus (Remainder)  : 6%4  e.g let result = 6 % 4; //output


Assignment Operators
---------------------

= Assignment  e.g. let x =5;
+= Addition Assignment e.g. x+=3  // equivalent to x = x + 3;
-= Subtraction  Assignment e.g. x-=3  // equivalent to x = x - 3;
*= Multiplication   Assignment e.g. x*=3  // equivalent to x = x * 3;
/= Division   Assignment e.g. x/=3  // equivalent to x = x / 3;


Comparison Operators
--------------------------
Equal to (==):  console.log(5 == '5'); // true (loose equality)
Strict Equal to (===): console.log(5 === '5'); // false (strict equality)
Not Equal to (!=): console.log(5 != '5'); // false (loose inequality)
Strict Not Equal to (!==): console.log(5 !== '5'); // true (strict inequality)
Greater Than (>), Less Than (<): console.log(5 > 3); // true  console.log(5 < 3); // false
Greater Than or Equal to (>=), Less Than or Equal to (<=): console.log(5 >= 5); // true
console.log(5 <= 3); // false


Logical Operators:
------------------------
Logical AND (&&)   
Logical OR (||)
Logical NOT (!)

if (x > 0 && x < 10) {
    // code executes if x is greater than 0 and less than 10
}
if (x === 0 || y === 0) {
    // code executes if x is 0 or y is 0
}
if (!flag) {
    // code executes if flag is false
}


Other Operators: based on JS behaviour
----------------------------
Concatenation (+): let string = 'Hello, ' + 'world!' -->// str is 'Hello, world!'

Typeof Operator (typeof): console.log(typeof x); // prints the data type of x

Conditional (Ternary) Operator (condition ? expr1 : expr2):

e.g. let result = (x > 0) ? 'Positive' : 'Negative';

Increment (++), Decrement (--):

let x = 5;
x++; // Increment x by 1

let x = 5;
x--; // Decrement x by 1


These are the fundamental types of operators in JavaScript. They enable you to perform various operations and comparisons in your code.


Important notes
--------------------

Type coercion in JavaScript refers to the automatic conversion of values from one data type to another when they are used together in an operation or expression.

 JavaScript is a loosely typed or dynamically typed language, which means that variables can hold values of any data type, and the interpreter attempts to interpret the operations accordingly.  Type coercion can occur implicitly or explicitly.


 Implicit Type Coercion
 

 let x = 5;
let y = '10';

let result = x + y; // JavaScript converts x to a string and performs string concatenation
console.log(result); // '510'


In the above example, the + operator is used for both addition and string concatenation. Since one of the operands is a string (y), JavaScript implicitly converts the numeric value x to a string and performs concatenation


Explicit Type Coercion

Explicit type coercion, also known as type casting, occurs when a developer intentionally converts a value from one type to another using functions or methods. Examples include using Number(), String(), and Boolean() functions

let x1 = '5';
let y1 = '10';

let result = Number(x1) + Number(y1); // Explicitly converting x and y to numbers
console.log(result); // 15


Conditional statements
----------------------------

Conditional statements in JavaScript allow you to execute different code blocks based on whether a specified condition evaluates to true or false.

if Statement:
The if statement is the most basic type of conditional statement. It executes a block of code if the specified condition is true.

let x = 5;

if (x > 0) {
    console.log('x is positive');
}


if...else Statement:
The if...else statement extends the if statement by providing an alternative block of code to execute when the condition is false.

let x = -3;

if (x > 0) {
    console.log('x is positive');
} else {
    console.log('x is not positive');
}

if...else if...else Statement:
The if...else if...else statement allows you to check multiple conditions in sequence. It executes the block associated with the first true condition.

let x = 0;

if (x > 0) {
    console.log('x is positive');
} else if (x < 0) {
    console.log('x is negative');
} else {
    console.log('x is zero');
}


switch Statement:
The switch statement provides a way to handle multiple conditions more efficiently than a series of if...else if statements. It compares a value against multiple possible case values.

let day = '';

switch (day) {
    case 'Monday':
        console.log('It\'s the start of the week');
        break;
    case 'Friday':
        console.log('Weekend is near');
        break;
    default:
        console.log('It\'s a regular day');
}


In JavaScript, break and continue are control flow statements that are used within loops (like for, while, and do...while) to alter the normal flow of the loop.

1. break Statement:
The break statement is used to exit a loop prematurely, before the loop condition is false. It is often used when a certain condition is met, and you want to terminate the loop immediately.


for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // exit the loop when i is equal to 5
    }
    console.log(i);
}


2. continue Statement:
The continue statement is used to skip the rest of the code inside a loop for the current iteration and move on to the next iteration.


for (let i = 0; i < 5; i++) {
    if (i === 2) {
        continue; // skip the rest of the loop body for i = 2
    }
    console.log(i);
}

It's important to use them judiciously to control the flow of your loops effectively. Misuse of these statements can lead to code that is harder to read and maintain, so it's generally recommended to use them with caution


when we are learning JS we have to categorize Objects
----------------------------------------------
1. Globally available Objects
2. user defined objects


 Globally available Objects
--------------------------

In JavaScript, several global objects are available by default. These objects provide functionality that is accessible throughout your entire script.


Global Object (window in browsers, global in Node.js):
---------------------------
a)In browsers, the global object is window. It represents the global context for the JavaScript code running in the browser.
b)In Node.js, the global object is global. It represents the global context for the JavaScript code running in Node.js.


+-------------------+----------------------------+
| Global Object     | Environment                |
+-------------------+----------------------------+
| window (browser)  | Browser                    |
| global (Node.js)  | Node.js                    |
| Math              | Universal                  |
| JSON              | Universal                  |
| console           | Universal                  |
| Date              | Universal                  |
| setTimeout        | Universal                  |
| setInterval       | Universal                  |
| Object            | Universal                  |
| Array             | Universal                  |
| String            | Universal                  |
| RegExp            | Universal                  |
| Error             | Universal                  |
+-------------------+----------------------------+

These global objects provide a variety of functionalities, from handling mathematical operations and dates to managing asynchronous operations and working with different data types. 

These global objects provide a foundation for building JavaScript applications and are available throughout the entire runtime of a script. It's important to note that when running JavaScript in different environments (e.g., browsers, Node.js), some objects may have slight variations or additional functionalities specific to that environment.