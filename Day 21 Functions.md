# Function in javascript

### 🧠 **1️⃣ What Is a Function?**

A **function** is like a mini-program inside your program —

it’s a reusable block of code that performs a specific task whenever you *call* it. 🔁

💬 Think of it like a vending machine:

- You press a button (call the function)
- It performs some steps (code)
- It gives you an output (result)

---

### ⚙️ **2️⃣ Syntax**

```jsx
function functionName() {
  // code to execute
}

```

You create a function once and use (or “call”) it as many times as you want.

---

### 💡 **3️⃣ Example – Simple Function**

```jsx
function sayHello() {
  console.log("Hello, Pratham!");
}

sayHello(); // calling the function

```

🧩 Output:

```
Hello, Pratham!

```

---

### 💬 **4️⃣ Parameters & Arguments**

Parameters are like **placeholders** — they’re the inputs your function can take.

Arguments are the **actual values** you pass when calling it.

```jsx
function greet(name) {  // 'name' is a parameter
  console.log(`Hello, ${name}!`);
}

greet("Pratham");  // 'Pratham' is an argument
greet("Aman");

```

🧩 Output:

```
Hello, Pratham!
Hello, Aman!

```

---

### 💡 **5️⃣ Multiple Parameters**

You can pass multiple values into a function.

```jsx
function addNumbers(a, b) {
  console.log(a + b);
}

addNumbers(5, 10);

```

🧩 Output:

```
15

```

---

### 🔁 **6️⃣ The `return` Keyword**

The `return` keyword lets your function send back a value instead of just printing it.

It’s like giving back a result you can store or reuse.

```jsx
function multiply(x, y) {
  return x * y;
}

let result = multiply(4, 3);
console.log(result);

```

🧩 Output:

```
12

```

💬 Without `return`, the function only *prints*.

With `return`, it *gives back* the value for later use.

---

### 💡 **7️⃣ Functions Calling Functions**

You can even call a function **inside** another function.

```jsx
function add(a, b) {
  return a + b;
}

function square(num) {
  return num * num;
}

let sum = add(2, 3);
let squared = square(sum);

console.log(squared);

```

🧩 Output:

```
25

```

## function is a set of reusable code declared once use it whenever you want and call the function to execute that code

```jsx
function happybirthday(){// this is how you declrare any funtion 
    console.log("happy birthday to you ")
    console.log("happy birthday too you")
    console.log ("happ birthdy dear you ")

}
happybirthday();// this is how you call the function  and you can call this function as many times you want to call it 
//ouput happy birthday to you 
//happy birthday too you
//happ birthdy dear you

function happybirthday(username, age){// this is how you set the parameter inside the funtion
    console.log("happy birthday to you ");
    console.log("happy birthday too you");
    console.log (`happy birthday dear ${username}`);
    console.log(`you are ${age} years old`);

}
happybirthday("pratham", 18);// these are the arguments 
// happy birthday to you 
// happy birthday too you
// happy birthday dear pratham
// you are 18 years old

```

## Return keyword

```jsx
// return keyword 
function add(x,y){
    let result = x + y;// or directly return x + y;
    return result;
}
let answer = add(2,3);// tou can either declare the variable and see the result 
console.log(answer);// output is 5

console.log(add(2,3));// or you can directly right inside the console.log and the output is 5
```