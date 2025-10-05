# Const variable in javascript

## 🧠 1️⃣ What is `const`?

`const` stands for **constant**.

It’s used to declare variables **whose value should never change** after being assigned.

Example: 

```jsx
const pi = 3.14159;
console.log(pi); // 3.14159
//If you try to change it later:
pi = 3.14; // ❌ Error: Assignment to constant variable
//So basically, const means “lock this value” 🔒

```

## const = a variable that cannot be change

```jsx
//To understand const lets calculate the circumference of a circle 
// lets calculate the circumference of circle to understand it 
// first we will calculate it by using let variable 
// the forumula is circumference = 2*pi*r
let pi = 3.1459;
let radius = Number(window.prompt("enter the radius"));
let circumference = 2 * pi * radius;
console.log(circumference);// output 62.918000000000006
// why to use the const varible you may accidently or someone delibrately change the value of let varible
// the output will differ 

//by using const 
const PI = 3.1459;// by using the const variable here no can change it by reassing it and for good practice you
// should always make the lettter capital on the const variable when it is number and not done for stings 
let radius = Number(window.prompt("enter the radius"));
let circumference = 2 * pi * radius;
PI = 40.234
console.log(circumference);// you wil get an error because const varible once assign then you cannot change it 
```

## 💡 2️⃣ Difference between `let` and `const`

| Feature | `let` | `const` |
| --- | --- | --- |
| Reassign value | ✅ Allowed | ❌ Not allowed |
| Redeclare (in same scope) | ❌ Not allowed | ❌ Not allowed |
| Must be initialized immediately | ❌ No | ✅ Yes |
| Block scope | ✅ Yes | ✅ Yes |

example :

```jsx
let name = "Pratham";
name = "Shinde";  // ✅ works fine

const age = 21;
age = 22;         // ❌ error

```

## ⚙️ 3️⃣ You *must* initialize a `const` when you declare it

This will cause an error:

```jsx
const score;
score = 100;  // ❌ Error
const score = 100;// correct 

```

## Short practice to calculate circumference fo circle using const function

```jsx
//html cocde 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
        <h1 id="myh1">the circumference of circle is :</h1>
    <label for="">radius</label>
    <input type="text" id="mytext"><br><br>
    <button id="mysubmit">calulate circumference</button>
    
    <script  src="index.js"></script>
    
</body>
</html>
```

```jsx
//javascript code 
const PI = 3.1459;// by using the const variable here no can change it by reassing it and for good practice you
// should always make the lettter capital on the const variable when it is number and not done for stings 
let radius ;
let circumference ;
document.getElementById("mysubmit").onclick = function(){
    radius=document.getElementById("mytext").value; // this line is use to get the value from the text and it is assgined to the radius 
    radius = Number(radius);
    circumference = 2 * PI* radius;
    document.getElementById("myh1").textContent = `the cirumference of cicle is ${circumference}cm`;
    console.log(circumference);
    console.log(PI);    
    console.log(radius);
}
```