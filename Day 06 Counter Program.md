# Counter program using javascript

## Increasing and decreasing by one and increasing and decreasng by two both thing

## HTML CODE :

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>counnter program</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>counter program</h1>
    <label id="countlabel">0</label><br><br>
    <div id="buttoncontainer">
        <button id="decreasebtn" class="button">decrease</button>
        <button id="resetbtn" class="button">reset</button>
        <button id="increasebtn" class="button">increase</button>
    </div>

    <h1 >counter program increasing decreasin with two </h1>

    <label id="clabel">0</label><br><br>
    <div id="btncontainer">
        <button id="decrease" class="btn"> decrease</button>
        <button id="reset" class="btn" >reset</button>
        <button id="increase" class="btn">increase</button>

    </div>
    
<script src="index.js"></script>
</body>
</html>
```

## CSS CODE :

```jsx
#countlabel{
    display: block;
    text-align: center;
    font-size: 10em;
    font-family: Helvetica;

}
h1{
    text-align: center;
    border: 2px solid black;
    background-color: aqua;
    cursor: pointer;
    transition: background-color 0.25s;
    
}
h1:hover{
    background-color: rgb(48, 196, 196);
}
#buttoncontainer{
    text-align: center;
    
}
.button{
    font-size: 1.5em;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: hsl(180, 100%, 50%);
    cursor: pointer;
    transition: background-color 0.25s;
}
.button:hover{
      background-color: hsl(180, 96%, 20%);
}

#clabel{
    display: block;
    text-align: center;
    font-size: 10em;
    font-family: Helvetica;
}
#btncontainer{
    text-align: center;
}
.btn{
    font-size: 1.5em;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: hsl(180, 100%, 50%);
    transition: background-color 0.25s;
    cursor: pointer;

}
.btn:hover{
      background-color: hsl(180, 96%, 20%);
}
```

## JAVASCRIPT CODE :

```jsx
const increasebutton = document.getElementById("increasebtn");
const decreasebutton = document.getElementById("decreasebtn");
const resetbtn = document.getElementById("resetbtn");
let count =0;
increasebutton.onclick = function(){
    count ++;
    countlabel.textContent = count;
}
decreasebutton.onclick = function(){
    count--;
    countlabel.textContent = count;
}
resetbtn.onclick = function(){
    count = 0;
    countlabel.textContent = count;
}
const dbutton = document.getElementById("decrease");
const ibutton = document.getElementById("increase");
const rbutton = document.getElementById("reset");
let counter = 0 ;
dbutton.onclick = function(){
    counter -= 2;
    clabel.textContent = counter;
}
ibutton.onclick = function(){
    counter +=2;
    clabel.textContent = counter;
}
rbutton.onclick = function(){
    counter =0;
    clabel.textContent = counter;
}t
```