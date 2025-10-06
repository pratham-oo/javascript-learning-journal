# Math object in javascript

## Math object is a built in object that provides a collection of properties and methods

## 🧠 1️⃣ What is the Math Object?

The **`Math` object** in JavaScript gives you built-in methods and constants for performing mathematical operations.

Think of it as your calculator 🧮 inside JS!

👉 Important:

You don’t have to create it (like `new Math()`); it’s already available globally.

## 💡 2️⃣ Common Math Methods

Here are the most useful ones (and you’ll use them a LOT later 👇):

| Method | Description | Example |
| --- | --- | --- |
| `Math.round(x)` | Rounds to nearest integer | `Math.round(4.6)` → `5` |
| `Math.floor(x)` | Rounds *down* | `Math.floor(4.9)` → `4` |
| `Math.ceil(x)` | Rounds *up* | `Math.ceil(4.1)` → `5` |
| `Math.trunc(x)` | Removes decimals (no rounding) | `Math.trunc(4.9)` → `4` |
| `Math.pow(x, y)` | Raises `x` to power `y` | `Math.pow(2, 3)` → `8` |
| `Math.sqrt(x)` | Square root | `Math.sqrt(25)` → `5` |
| `Math.abs(x)` | Absolute value | `Math.abs(-7)` → `7` |
| `Math.max(a, b, c...)` | Largest number | `Math.max(3, 8, 1)` → `8` |
| `Math.min(a, b, c...)` | Smallest number | `Math.min(3, 8, 1)` → `1` |
| `Math.random()` | Random number between 0–1 | `Math.random()` → `0.63` (example) |

```jsx
Math.PI
console.log(Math.PI);// this is the math object and output is 3.141592653589793
console.log(Math.E);// euluers number and output is 2.718281828459045
// round off
let x = 3.12;
let y = 4;
let z;
z = Math.round(x);// this will round of the value of x 
console.log(z);// output is 3 
// flooring 
let x = 3.99;
let y = 4;
let z;
z = Math.floor(x);// this is will always round downn the value of x 
console.log(z);// output is 3
// ceiling 
let x = 3.21;
let y = 4;
let z;
z = Math.ceil(x);// opposite of floor
console.log(z);// output is 4 
// truncate 
let x =  3.123;
let y = 4;
let z;
z = Math.trunc(x);// this is done for truncation 
console.log(z); // output is 3
// power 
let x = 3;
let y = 2;
let z;
z = Math.pow( x , y);// for powering it 
console.log(z);// output 9 
// squrare root 
let x = 9;
let y = 2;
let z;
z = Math.sqrt(x);// for squaring it 
console.log(z);// output 3
// logaritm 
let x = 10;
let y = 2;
let z;
z = Math.log(x);// for finding natural logarithm 
console.log(z);// output 2.302585092994046
//trignomertrc 
let x = 45;
let y = 2;
let z;
z = Math.sin(x);// for finding trigno metric function 
console.log(z);// output 0.8509035245341184
//abosulte value 
let x = -3.123;
let y = 2;
let z;
z = Math.abs(x);// for finding absoulte value 
console.log(z);// output 3.123 basically give the same value but in positive 
// to finding the sign of an number 
let x = -3.123;
let y = 2;
let z;
z = Math.sign(x);// for finding the sing of an variable  
console.log(z);// output -1 
// finding maximun and minimun value 
let x = -3.123;
let y = 2;
let z = 4;
let max= Math.max(x, y , z);// for finding the maximmun value 
console.log(max);// output 4
// findin the minimun value 
let x = -3.123;
let y = 2;
let z = 4;
let min= Math.min(x, y , z);// for finding the minimum value 
console.log(min);// output -3.123

```

## 💥  Math Constants

| Constant | Description | Example |
| --- | --- | --- |
| `Math.PI` | π (3.14159…) | Circle calculations |
| `Math.E` | Euler’s number (~2.718) | Exponential growth |
| `Math.SQRT2` | √2 | Square root of 2 |
| `Math.LN2` | ln(2) | Natural log of 2 |