# Checked property in javascript

## checked = This is he property that determines the check status of and html checkbox or radio element

### 🧠 **1️⃣ What Is a “Property” in JavaScript?**

Every **object** in JavaScript has **properties** — they’re basically *key–value pairs* inside curly braces `{}`.

Example:

```jsx
const person = {
  name: "Pratham",
  age: 21,
  isStudent: true
};

```

Here:

- `name`, `age`, and `isStudent` → are **properties (keys)**
- `"Pratham"`, `21`, and `true` → are **their values**

---

### 💡 **2️⃣ Why Check for a Property?**

Sometimes, you’re not sure if a property **exists** in an object.

If you try to use a property that doesn’t exist → you’ll get `undefined`, which can cause bugs 🐛

### Program for checked property

html code :

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
    <h1 id="myh1">payement and subscription checking program </h1>
    <input type="checkbox"  id="mycheckbox">
    <label for="mycheckbox"> Subscribe </label><br><br>
<input type="radio" name="pratham" id="vistabtn">
<label for="vistabtn">vista</label><br>
<input type="radio" name="pratham" id="mastercardbtn">
<label for="mastercardbtn">mastercard</label><br>
<input type="radio" name="pratham" id="paypalbtn">
<label for="paypalbtn">paypal</label><br><br>
<button id="mysubmit">submit</button><br>
<p id="s1"></p>
<p id="s2"></p>
<script src="index.js"></script>
    
</body>
</html>
```

css code :

```jsx
#mysubmit{
    font-size: 1.5em;
    border-radius: 5px;
    background-color: hsl(180, 100%, 50%);
    cursor: pointer;
    transition: background-color 0.25s;
}
#mysubmit:hover{
    background-color: hsl(180, 87%, 44%);
}
```

javascript code :

```
const myh1 = document.getElementById("myh1");
const mycheckbox = document.getElementById("mycheckbox");
const vistabtn = document.getElementById("vistabtn");
const mastercardbtn = document.getElementById("mastercardbtn");
const paypalbtn = document.getElementById("paypalbtn");
const mysubmit = document.getElementById("mysubmit");
const s1 = document.getElementById("s1");
const s2 = document.getElementById("s2");
mysubmit.onclick = function(){
    if(mycheckbox.checked){
        s1.textContent = `you are subscribbed`;

    }
    else{
        s1.textContent = ` you are not subscribed`;
    }
    if(vistabtn.checked){
        s2.textContent = `you are paying wiht visa`;
    }
    else if(mastercardbtn.checked){
        s2.textContent =`you are paying with mastercard`;
    }
    else if(paypalbtn.checked){
        s2.textContent = `you are paying with paypal`;
    }
    else{
        s2.textContent = ` you have not selected the payment method`
    }
   
}
```