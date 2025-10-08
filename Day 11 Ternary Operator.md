# Ternary operator in javascript

## Ternary = A shortcut to if{} and else{} statements helps to assign varible based on condition

## condition ? codeifTrue : codeifFalse;

### 🧠 **1️⃣ What Is the Ternary Operator?**

The **ternary operator** is a **one-line “if...else”** statement.

It’s called *ternary* because it has **three parts**:

```jsx
condition ? expressionIfTrue : expressionIfFalse

```

It checks the condition:

- ✅ If it’s true → runs the first expression
- ❌ If it’s false → runs the second expression

```jsx
// ternary operator 
let age = 10;
let message = age >=18 ? "you are eligible to drive " : "you are not eligible to drive";// in this we have use ternary operator 
// the ternary operator is "?" and the first part is if it is true and he second part is if it is false 
console.log(`your age is ${age} and ${message}`);
//ouput your age is 10 and you are not eligible to drive
 let time = 16;
let msg = time>=12 ? "good afternoon": "good morning";
console.log(`time is ${time} so ${msg}`);//output time is 16 so good afternoon
 let isstudent = true;
let enrolled = isstudent ? "you are a student ": "you are not a student";
console.log(enrolled);//output you are a student
let amount = 10;
let purchase = amount >= 100 ? "you wil get an 10% discount": "your purchase amount should be atleast more than 100 for the discount";
console.log(`your purchase amount is ${amount} so ${purchase}`)// output your purchase amount is 10 so your purchase amount should be atleast more than 100 for the discount
```

### 🧩  **Nested Ternary (Advanced)**

You can chain multiple ternary operators — but be careful ⚠️ (too many makes it confusing).

```jsx
let score = 85;

let grade = (score >= 90) ? "A+" :
             (score >= 75) ? "A" :
             (score >= 60) ? "B" :
             "C";

console.log(`Your grade is ${grade}`);

```

🧩 Output:

```
Your grade is A

```

## BY using ternary operator calculating discount

### General Formula

The fundamental formula to calculate a price after a discount is:

Final Price=Original Amount−(Original Amount×Dicount Percentage/100)

```jsx
let amount = 125;
let purchase = amount >= 100 ? 10:0;
console.log(`your total with the 10% discout  is $${amount - amount *(purchase/100)}`);
//output your total with the 10% discout  is $112.5
```

### 💥 **Using with Template Literals**

You can use ternary operators *directly inside strings*, which makes UI logic easy 👇

```jsx
let isLoggedIn = true;
console.log(`Welcome ${isLoggedIn ? "back" : "guest"}!`);

```

🧩 Output:

```
Welcome back!

```