# If statements in javascript

### 🧠 **What Are If Statements?**

`if` statements let your program **make decisions**.

They check a **condition**, and if it’s true ✅ — the code inside runs.

If not ❌ — it’s skipped.

## if statemens = if the condition is true execute the code if not do something else

```jsx
let age = 12;
if(age >= 18){// in the parethesis you can wirte the condition you want to set and then insdie the curly bracket 
    // you can write the code or anything you want to dislplay 
    console.log("your are old enough for voting");
}
else {// this is used when the first staement is not true and you want to display something else 
        console.log("your are not eligible for voting")
}
// output is your are not eligible for voting 

 let time = 17; // time should be in military hours 
 if (time < 12){
    console.log("good morning")
 }
 else{
    console.log("good night")
 }
 //output is good night 
 
 // bolean example 
 let isstudent = true;
if(isstudent){
    console.log("your are student")

}
else {
    console.log("you are not a student ")
}
// ouput is you are not a student 

```

## nested if statements

```jsx
let age = 20;
let haslicense =false;
if(age >= 18){// if thi condition is true and then it will execute the next if statement othere wise it will skip everything and move onto else 
    console.log("you are eligble to drive a car ");
    if(haslicense){// if this condition is true and then it will execute this statem otherewise the next one 
        console.log("you have license");
    
    }
    else{
        console.log("you do not have license");
    }
}
else{// if the main if condition is false then only this statement will be executed 
    console.log("you are not eligble to drive a car");
}
// output you are eligible to drive a car 
// you do not have license 
```

## else if statements

```jsx
let age = 10;
if(age >= 18){
    console.log(" you are eligible to drive");// when is age is above 18 
}
else if(age >=16){
    console.log("you can drive any ev vehicle ");// when age is above 16
}
else {
    console.log("you are not eligible to drive "); // when age is below 16 
}//ouput you are not eligibel to drive 

let age = 71;
 if(age >= 70){
    console.log("you are advised to not to drive a car at this after this age ")// when your age is above 70 
}
else if(age >= 18){
    console.log(" you are eligible to drive");// when is age is above 18 
}
else if(age >=16){
    console.log("you can drive any ev vehicle ");// when age is above 16
}

else {
    console.log("you are not eligible drive "); // when age is below 16 
}// output you are advised to not to drive a car at this after this age 
```

### ⚡  **Comparison Operators Recap**

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` | Equal to | `5 == "5"` → ✅ true (type not checked) |
| `===` | Strict equal (checks type too) | `5 === "5"` → ❌ false |
| `!=` | Not equal | `10 != 5` → true |
| `!==` | Strict not equal | `10 !== "10"` → true |
| `>` | Greater than | `8 > 6` → true |
| `<` | Less than | `3 < 5` → true |
| `>=` | Greater than or equal to | `10 >= 10` → true |
| `<=` | Less than or equal to | `4 <= 7` → true |

### 💥  **Logical Operators**

| Operator | Meaning | Example |
| --- | --- | --- |
| `&&` | AND (both must be true) | `(age > 18 && age < 60)` |
| ` |  | ` |
| `!` | NOT (reverses) | `!(true)` → false |

## small excercise

html code: 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <h1 id="myh1">enter your age to knwo the eligibilty for driving the vehicle </h1>
    <label id="mylabel">enter the age:</label>
    <input id="mytext"><br><br>
    <button id="mysubmit">submit</button>
    <p id="myp"></p>
    <script  src="index.js"></script>
    
</body>
</html>
```

javascript code :

```jsx

const mytext = document.getElementById("mytext");
const mysubmit = document.getElementById("mysubmit");
const myp = document.getElementById("myp");
const muh1 = document.getElementById("myh1");
let age;
mysubmit.onclick = function(){
    age = mytext.value;
    age = Number(age);
    if(age >= 70){
    myp.textContent = `you are advised no to drive a car after this age`;
    myh1.textContent = `your age is ${age} please dont drive `;
}
else if(age >= 18){
    myp.textContent = `you are eligible to drive`;
    myh1.textContent = `your age is ${age} you can drive but get the license first if you have not`;
}
else if(age >=16){
    myp.textContent = `you can drive any ev vehicle`;
    myh1.textContent = `your age is ${age} you can drive ev but not any other vehicel`;

}

else {
    myp.textContent =` you are not eligble to drive `;
    myh1.textContent = ` your age is ${age} please drive cycle`;

}

}

```