# Switch  and break statement in javascript

---

### 🧠 **1️⃣ What Is a Switch Statement?**

A `switch` statement is used when you have **multiple possible values** for a single variable or expression.

Instead of writing a bunch of `if...else if` statements, you can use `switch` for better readability 👇

---

### 💡 **2️⃣ Basic Syntax**

```jsx
switch (expression) {
  case value1:
    // code if expression === value1
    break;
  case value2:
    // code if expression === value2
    break;
  default:
    // code if no match found
}

```

### 💥  **The Role of `break`**

- The `break` statement **stops** the switch from continuing to other cases.
- Without it, **execution “falls through”** to the next case (even if it doesn’t match 😅).

Example 👇

```jsx
let fruit = "apple";

switch (fruit) {
  case "apple":
    console.log("Apples are red 🍎");
  case "banana":
    console.log("Bananas are yellow 🍌");
  default:
    console.log("Unknown fruit 🥭");
}

```

🧩 Output (without `break`):

```
Apples are red 🍎
Bananas are yellow 🍌
Unknown fruit 🥭

```

👉 See what happened? It didn’t stop!

That’s why we use **`break`** to exit once the right case runs ✅

---

### ⚙️  **Example with `break` (Correct Way)**

```jsx
let fruit = "apple";

switch (fruit) {
  case "apple":
    console.log("Apples are red 🍎");
    break;
  case "banana":
    console.log("Bananas are yellow 🍌");
    break;
  default:
    console.log("Unknown fruit 🥭");
}

```

🧩 Output:

```
Apples are red 🍎

```

---

### 🎯  **Example with `default` Case**

The `default` block runs **when none of the cases match**.

Think of it like the **else** in an if-statement.

```jsx
let color = "purple";

switch (color) {
  case "red":
    console.log("Color of passion ❤️");
    break;
  case "blue":
    console.log("Color of calm 💙");
    break;
  default:
    console.log("Unknown color 🎨");
}

```

🧩 Output:

```
Unknown color 🎨

```

---

### 🧩  **Grouping Multiple Cases**

You can **combine multiple cases** that share the same outcome 👇

```jsx
let month = 2;

switch (month) {
  case 1:
  case 2:
  case 12:
    console.log("It’s winter ❄️");
    break;
  case 3:
  case 4:
  case 5:
    console.log("It’s spring 🌸");
    break;
  default:
    console.log("Invalid month");
}

```

🧩 Output:

```
It’s winter ❄️

```

## Switch = switch can be efficient replacement of to many else if statements

```jsx
// a program without using switch statements 
let day = 3;
if (day ==1){
    console.log(`it is monday`);
}
else if(day==2){
    console.log(`its tuesday`);
}
else if(day==3){
        console.log(`its wednesday`);

}
else if(day==4){
        console.log(`its thursday`);

}
else if(day==5){
        console.log(`its friday`);

}
else if(day==6){
        console.log(`its saturday`);

}
else if(day==7){
        console.log(`its sunday`);

}
else {
        console.log(`${day} it is not a day `);

}//output its wednesday 
```

## Program using the swith statement

```jsx
let day = 2;
switch(day){// within the parenthesis we have to put the value or variable we are examing 
    case 1:
        console.log(`its monday`);
        break;// reason to use the break is to execute the code and then break and start from the first otherwise it will execute the all cases after the value 
    case 2:
        console.log(`its tuesday`);
        break;
    case 3:
        console.log(`its wednesday`);
        break;
    case 4:
        console.log(`its thurday`);
        break;
    case 5:
        console.log(`its friday`);
        break;
    case 6:
        console.log(`its saturday`)
        break;
    case 7:
        console.log(`its sunday`)
        break;
    default:// incase there are no matching you can add default case there to get the output 
        console.log(`${day} it is not a day`)    
    
    
}
//ouput it is tuesday  
```

## a program to for grading system using switch method

```jsx
let testscore = 35;
let grade;
switch(true){// this is the another way of using the switch statement 
    case testscore >= 90:
        grade = 'A';
        break;
    case testscore >= 80:
        grade = 'B';
        break;
    case testscore >= 70:
        grade = 'C';
        break;
    case testscore >= 60:
        grade = 'D';
        break;
    case testscore >= 50:
        grade = 'E';
        break;
    case testscore >=35:
        grade = 'F';
        break;
    case testscore < 35:
        grade ='FAIL';
        break;
    
}
console.log(`your marks is ${testscore}  and so you got ${grade}`);
```