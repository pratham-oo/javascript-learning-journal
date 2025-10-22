# Temperature converter program

## HTML CODE:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>temperature converter </title>
</head>
<body>
    <form action="">
        <h1>Temperature converter:</h1>
        <input type="number"  id="textbox" value="0"><br>
        <input type="radio" name="unit" id="tofahereneit">
        <label for="tofahereneit">celcius ➡️ fahereneit</label><br>
        <input type="radio" name="unit" id="tocelsius">
        <label for="tocelsius">fahereneit ➡️ celsisus</label><br>
        <button type="button" onclick="convert()">submit </button>
        <p id="myp1"></p>
        <button type="button" id="reset"">reset </button>
    </form>
    <script src="index.js"></script>
</body>
</html>
```

## CSS CODE:

```jsx

```

```
body{
    font-family: Arial, Helvetica, sans-serifs;
    background-color: hsl(0, 14%, 91%);
}
h1{
    color: blue;
}
form{
    text-align: center;
    background-color: aliceblue;
    max-width: 400px;
    margin: auto;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 5px 5px 15px hsla(0, 0%, 0%, 0.30);
}

#textbox{
    width: 50%;
    text-align: center;
    font-size: 2em;
    border: 2px solid rgba(0, 0, 0, 0.607);
    border-radius: 5px ;
    margin-bottom: 20px;
}
label{
    font-size: 1.5em;
    font-weight: bold;
}
button{
    margin-top: 15px;
    background-color: rgba(159, 45, 45, 0.801);
    font-size: 1.5em;
    border-radius: 5px;
    padding:10px 15px;
    color: aliceblue;
    cursor: pointer;
    transition: background-color 0.25s;
}
button:hover{
    background-color: rgb(225, 24, 24);
}
#myp1{
    font-size: 1.75em;
    font-weight: bold;
}
```

## JAVASCRIPT CODE :

```jsx
const tofahereneit = document.getElementById("tofahereneit");
const tocelsius = document.getElementById("tocelsius");
const myp1 = document.getElementById("myp1");
const reset = document.getElementById("reset");
let temp;

function convert(){
    if(tofahereneit.checked){
        temp = Number(textbox.value);
        temp = temp * 9/5 + 32;
        myp1.textContent = temp.toFixed(1) + `F`;
    }
    else if(tocelsius.checked){
        temp = Number(textbox.value);
        temp = (temp - 32) * (5/9);
        myp1.textContent = temp.toFixed(1) + `C`;
    }
    else{
        myp1.textContent =` select  a unit `;
    }
    if ( myp1 < 15) {
        document.body.style.backgroundColor = "#66ccff"; // cold - blue
      } 
      else if (myp1 >= 15 && myp1 < 30) {
        document.body.style.backgroundColor = "#ffff99"; // warm - yellow
      } 
      else {
        document.body.style.backgroundColor = "#ff6666"; // hot - red
      }

}
reset.onclick = function(){
    textbox.value ="0";
    myp1.textContent ="";
          document.body.style.backgroundColor = "#f4f4f4"; // reset background

}

```