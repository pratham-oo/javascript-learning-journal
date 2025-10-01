# learn javascript fundamental

- A **programming language** that makes websites *interactive*.
- HTML = structure 🧱
- CSS = style 🎨
- JavaScript = brain 🧠

👉 Example: Clicking a button and something happening → JS at work.

java script is language which handles the logic of an website think of it like the human brain without the brain the your body is useless 

# To print the output in javscript you need to use this stament

console.log(”hello”); 

you can use backtics , single quote and double quote to print any statement in the console 

# To get and alert button in your webpage you can you use

window.alert(”this is an error”);

# By using javascript you can also get the text by not writing it into the index.html by getting the id and class

document.getElementById(’myhw’).textcontent = “hello”

document.getElementByClass(’myh2’).textcontent = “hello”

# VARIABLE

DEFINITION : Variable is a container that stores values and behaves that it were the value of that content 

In JS, you declare a variable using `let` (you’ll also see `var` and `const`, but `let` is modern and preferred).

- **`let`** → modern way to declare a variable (changeable value)
- **`const`** → constant, can’t change value
- **`var`** → old style, avoid for now
1. Declration :  let x ;
2. Assignment : x=100;

```jsx
let x; // this is how we declare the variable 
x =100; // this is how we assign value to the variable 
let x =100; // this is how we do both declration and assignment at the same time 
// when we want the input from user we use the the first method that is declration and assignment differently 
//once the variable is declare we cannot use it again it will throw an error 
let x =100 ; // correct 
let x =120; // wrong  the correct way should be let y = 120; 
console.log(x);// you can use like this to print the the value 
// output ; 100

```

# DATA TYPES IN JAVASCRIPT

1. Number 

```jsx
let age = 25;
console.log(age); // This is the numbe datatype 
// output 25 
// if we want to make a sentence out of it like...
console.log("i am ${age} years old");// this is how you you varible inside an senence using ${}
// outout i am 25 years old 

```

If yoy want to see the the data type fo an variable 

```jsx
let age =12;
console.log(typeof age );// by using typeof keyword we can  get the data type of an variable
// output number 
 
 
```

1. STRING 

 string are the sequence of characters whihc also can include numbet in it but we cannto use that numbers for arthmetic operation 

```jsx
let firstname = "pratham "; //this is how string data type look like 
console.log(firstname);// output pratham 
console.log(typeof firstname);// output string 
console.log(`my name is ${firstname}`);// output my name is pratham 
let email ="pratham123@gmail.com";
console.log(`my email is ${email}`); // output my email is pratham123@gmail.com
```

1. Boolean 

Booleans are either true or false typically they are used flags in your program

```jsx
let online = true; // boolearn datatype 
console.log(typeof online);// output boolean
console.log(`bro is onlnine : ${online}`);
// oouput is bro is online : true 
let forsale =true;
console.log(`is this car for sale: ${forsale}`);// output is this car for sale : true 
```

## Simple program to display your information on website using javascript

```jsx
let fullname = "pratham shinde ";
let age = 20;
let isstudent =true;
document.getElementById("p1").textContent=`my name is ${fullname}`;
document.getElementById("p2").textContent=`my age is ${age}`;
document.getElementById("p3").textContent=`are you student  ${isstudent}`;
// outputmy name is pratham shinde

//my age is 20

//are you student true

```