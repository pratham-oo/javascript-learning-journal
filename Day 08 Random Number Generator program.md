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
```