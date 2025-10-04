# Accept user inuput in javascript

### 🧩 1️⃣ What does “accepting input” mean?

Up until now, your code just *outputs* stuff (e.g., `console.log("Hello!")`).

But what if you want the **user** to *enter* something — like their name, age, or a number — and then use it in your code? 🤔

That’s where **input methods** come in.

## How to accept  the user input in javascript

1. Easy way  = window prompt 
2. Professional way = HTML textbox 

## Window prompt

- This pops up a small dialog box asking the user to type something.
- Whatever the user types is **always returned as a string** (text).

```jsx
// in this method you will see the input on the page as alert button 
let username ; // declaring the variablle first 
username = window.prompt("what is your user name ?") // the assigning the value next 
console.log(username); // output in terminal pratham shinde 
let username = window.prompt("what is your username ??"); // in this we have declare and assiginign at the same level 
console.log(username); // output in the terminal pratham shinde

```

## Professional method  by creating HTML textbox

```jsx
// this is the html code 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1 id="myh1">welcome </h1>
    <label for="">username</label>
    <input type="text" id="mytext"><br><br>
    <label for="">age</label>
    <input type="number" id="myage"> <br><br>
    <button id="mysubmit">submit</button>s
    
    <script  src="index.js"></script>
    
</body>
</html>

```

```jsx
t//this is the javascript code 

let username;
let age;
// the varible should be declared outside of the function assign inside the funtion s

document.getElementById("mysubmit").onclick = function(){ //everything we will right in this in this function will happening after we click on the button 

    username = document.getElementById("mytext").value;
    age = document.getElementById("myage").value;
    document.getElementById("myh1").textContent = ` welcome ${username } , your age is ${age}`;// this assigning is to change the heading to welcome for welocme pratham your age is 18 
    console.log(username);
    console.log(age);
}

```