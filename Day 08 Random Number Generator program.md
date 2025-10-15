# Random generator program in javascript

## 🧠 1️⃣ What Is It?

A **Random Number Generator (RNG)** is a program that gives you a random number every time you click a button or refresh the page.

You can use it to simulate things like:

- Dice rolls 🎲
- Lottery numbers 🎯
- Random passwords 🔐
- Lucky draws 🍀

```jsx
let random = Math.random();// this generates the random number 
console.log(random);
// generating the number between 1 and 6 
let random = Math.floor(Math.random()*6 +1);// now this will genearte the number between 1 to 6 
console.log(random);// output 1 not 0 because we have +1 
// generating the random number between a certain range 100 - 50 
const max = 100;
const min = 50;
let random = Math.floor(Math.random() * max) + min;// if we do like then then what is happenig is 
// the math.random is multiplyin withe the max which is 100 
// and it then getting add with the min which is 50  then the the total wil be 150 
console.log(random); // output 139 an so onn...
// update version to do it 
const max = 100;
const min = 50;
let random = Math.floor(Math.random()* (max - min)) + min; // now here due to operator preccedence we can se how things will be happening 
console.log(random);// output number between 50 - 100 

```

## 💡 2️⃣ The Core Logic (Just 1 Line!)

The magic line that makes it all work:

```jsx
Math.floor(Math.random() * max) + min;

```

💬 Example: Random number between 1 and 6 (like dice):

```jsx
let randomNum = Math.floor(Math.random() * 6) + 1;

```

👉 Here’s what’s happening:

- `Math.random()` → gives a decimal between **0 and 1**
- `6` → scales it between **0 and 5.999...**
- `Math.floor()` → removes decimals
- `+ 1` → shifts range to **1–6**

Rolling one dice program 

html code:

```jsx
// rolling one dice program 
//html code 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>random number</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>rolling a six side dice </h1>
    <button id="mybutton"> roll</button><br>
    <label id="mylabel"> 0</label>
    <script src="index.js"></script>
    
</body>
</html>
```

css code :

```jsx
body{
    font-family: Verdana ;
    text-align: center;
}
#mybutton{
    font-size: 3em;
    padding: 10px 20px;
    border-radius: 10px;
    background-color: hsl(180, 100%, 50%);
    cursor: pointer;
    transition: background-color 0.25s;
}
#mybutton:hover{
    background-color: hsl(0, 17%, 63%);
}
#mylabel{
    font-size: 3em;
}

```

javascript code :

```jsx
const mybutton = document.getElementById("mybutton");
const mylabel = document.getElementById("mylabel");
const max = 6;
const min = 1;
let randomnum;
mybutton.onclick = function(){
    randomnum = Math.floor(Math.random() * max) + min;
    mylabel.textContent = randomnum;
    console.log(randomnum);
    
}
```

Rolling three dice program :

html code :

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>random number</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>rolling a six side dice </h1>
    <button id="mybutton"> roll</button><br>
    <label id="mylabel1" class="mylabel"> 0</label>
    <label id="mylabel2" class="mylabel"> 0</label>
    <label id="mylabel3" class="mylabel"> 0</label>
    <script src="index.js"></script>
    
</body>
</html>
```

css code :

```jsx
body{
    font-family: Verdana ;
    text-align: center;
}
#mybutton{
    font-size: 3em;
    padding: 10px 20px;
    border-radius: 10px;
    background-color: hsl(180, 100%, 50%);
    cursor: pointer;
    transition: background-color 0.25s;
}
#mybutton:hover{
    background-color: hsl(0, 17%, 63%);
}
.mylabel{
    font-size: 3em;
    padding: 10PX 10PX;
}

```

javascript code :

```jsx
const mybutton = document.getElementById("mybutton");
const mylabel1 = document.getElementById("mylabel1");
const mylabel2 = document.getElementById("mylabel2");
const mylabel3 = document.getElementById("mylabel3");
const max = 6;
const min = 1;
let randomnum1;
let randomnum2;
let randomnum3;
mybutton.onclick = function(){
    randomnum1 = Math.floor(Math.random() * max) + min;
    randomnum2 = Math.floor(Math.random() * max) + min;
    randomnum3 = Math.floor(Math.random() * max) + min;
    mylabel1.textContent = randomnum1;
    mylabel2.textContent = randomnum2;
    mylabel3.textContent = randomnum3;
    
}

const mylabel1 = document.getElementById("mylabel1");
const mybutton = document.getElementById("mybutton");
const x = Number(window.prompt("enter the  number:"));
const y = Number(window.prompt("enter the  number:"));
const s1 = document.getElementById("s1");
const s2 = document.getElementById("s2");
let myh1;
// const max = Math.max (x , y);
// const min = Math.min (x , y);
let max;
let min;
let random;
if(x >y){
    max=x;
    min = y;

}
else{
    max =y;
    min = x;
}
mybutton.onclick = function(){
    random = Math.floor(Math.random() * (max - min +1)) +min;
    mylabel1.textContent = random;
    myh1 = document.getElementById("myh1").textContent = `number is ${random}`;
    myh1 = document.getElementById("myh1").textContent = `number is ${random}`;
    s1.textContent = `the maxium number is ${max}`;
    s2.textContent= `the minimun nnumber is ${min}`;
    
    
}
// The main confusion is thinking the number 6 is a maximum value. It's not. The number 6 is the COUNT of how many numbers we want to choose from.

// ## The Box of Chocolates Analogy 🍫
// Imagine you have a box of chocolates. The chocolates are numbered 10, 11, 12, 13, 14, and 15.

// Question: How many chocolates are in the box?
// Answer: There are 6 chocolates.

// The code does the exact same thing in two steps:

// Step 1: Count the Items
// First, the code calculates (15 - 10 + 1), which equals 6.

// The computer now knows it needs to choose one out of 6 possible items. It completely forgets about the numbers 10 and 15 for a moment.

// Step 2: Pick an Item by its Position
// Now, the computer needs to pick one of those 6 items. Computers start counting from 0, so it labels their positions like this:

// The 1st item is at position 0.

// The 2nd item is at position 1.

// The 3rd item is at position 2.

// The 4th item is at position 3.

// The 5th item is at position 4.

// The 6th (and last) item is at position 5.

// The code Math.floor(Math.random() * 6) generates a random position, which will be a number from 0 to 5. It will never generate a 6, because there is no 7th item at position 6.

// Step 3: Find the Real Number
// Finally, the computer takes the random position it picked and adds your starting number (min) to it.

// If it picked position 0, it does 0 + 10 = 10.

// If it picked position 5, it does 5 + 10 = 15.

// So, the range is never 0 to 16. The calculation is always:
// (A random number from 0 to 5) + 10 = (A final number from 10 to 15)

// Computer's Random Position (0-5)	The Shift (+ min)	Final Number (10-15)
// 0	+ 10	10
// 1	+ 10	11
// 2	+ 10	12
// 3	+ 10	13
// 4	+ 10	14
// 5	+ 10	15

// Export to Sheets









```