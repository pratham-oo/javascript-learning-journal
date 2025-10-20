# While loop in javascript

### 🧠 **1️⃣ What Is a Loop?**

A loop lets you **repeat a block of code** multiple times until a certain condition becomes `false`.

It helps you **avoid writing the same line again and again** 🌀

There are two main loops you learned today:

- **`while` loop**
- **`do...while` loop**

---

## 🔹 **While Loop**

### 💡 **How It Works**

The **while loop** checks the condition **first**, then runs the code **only if** it’s true.

### ⚙️ **Syntax**

```jsx
while (condition) {
  // code to repeat
}

```

---

### 🧩 **Example 1 – Counting Up**

```jsx
let count = 1;

while (count <= 5) {
  console.log(`Count: ${count}`);
  count++;
}

```

🧠 **Explanation:**

- Starts with `count = 1`
- Checks the condition `count <= 5`
- If true → runs code → then increases `count`
- Stops when `count` becomes `6`

🧩 Output:

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5

```

---

### ⚠️ **Infinite Loop Warning**

If you forget to update your variable (`count++`), the loop will never end 😵‍💫

Always make sure something changes inside the loop!

---

## 🔹 **Do...While Loop**

### 💡 **How It Works**

The **do...while** loop runs the code **at least once**, *even if the condition is false* 🤯

Why?

Because it checks the condition **after** running the code once.

---

### ⚙️ **Syntax**

```jsx
do {
  // code to repeat
} while (condition);

```

---

### 🧩 **Example 2 – Counting Down**

```jsx
let number = 5;

do {
  console.log(`Number: ${number}`);
  number--;
} while (number > 0);

```

🧩 Output:

```
Number: 5
Number: 4
Number: 3
Number: 2
Number: 1

```

✅ Works like a while loop, but runs **once first** before checking the condition.

---

### 💡 **Example 3 – User Input**

This one shows the real difference between the two:

### Using `while`

```jsx
let name = "";

while (name === "") {
  name = prompt("Enter your name: ");
}
console.log(`Welcome, ${name}!`);

```

### Using `do...while`

```jsx
let name;

do {
  name = prompt("Enter your name: ");
} while (name === "");

console.log(`Welcome, ${name}!`);

```

💬 Even if `name` starts as `undefined`, the `do...while` loop will **run once**, then check if it should repeat.

---

## ⚔️ **While vs Do...While**

| Feature | `while` | `do...while` |
| --- | --- | --- |
| Checks condition | Before running code | After running code |
| Runs at least once? | ❌ No | ✅ Yes |
| Common use case | When you might *not* want it to run at all | When you want it to run *at least once* |

While loop means repeating some code while some condiition is true 

```jsx

//while loop 
// a program wihtout using the while loop 
 let username = "";
 if(username === ""){
     console.log(`enter your username `);
}
 else{
     console.log(`hello ${username}`);
 }// output is enter your username and the loop ends 
//soo if we want to continous thing then we will use the while loop 
let username = "";
while(username === ""){
    console.log(`enter your username `);
}
// here it will continously print the message inside the while loop without breaking 
   console.log(`hello ${username}`);
   
   
   
   
   let username = "";
while(username === ""){
    username = window.prompt("enter your name");
// alert window will not be  gone until you enter your username 
// if you cancel the alert window and then you will get hello null as an output 
}
   console.log(`hello ${username}`);// output is hello brocode 
   
   
   
   let username = "";
while(username === "" || username === null){// using or operator will make you right the username and it will not be gone 
    username = window.prompt("enter your username");
}
console.log(`hello ${username}`);// output hello pratham 
   

```

## Do while loop

```jsx
let username; // while using the do while loop you can keep the varibale undefined 
// if you do this while using the while loop then your while loop will never execute
do{
    username = window.prompt(`enter your username`);
}while(username === ""|| username === null  )// it will do the code first then it will check the condition 
    console.log(`hello ${username}`);
    
    

```

```jsx
let loggedin = false;
let username;
let password;
while(!loggedin){// while no logged in do all these other wise skip everthing 
    username = window.prompt("enter your username");
    password = window.prompt("enter your password ");
    if(username ==="myusername" && password === "mypasword"){

        loggedin= true;
        console.log(`welcome ${username} login succes`);
    }
    else{
        console.log(`loggin unsuccesful invalid credential`);
    }
}

```