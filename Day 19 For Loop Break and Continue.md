# For loop in javascript

### 🧠 **1️⃣ What Is a For Loop?**

A **for loop** is used when you know **exactly how many times** you want to repeat a block of code.

💬 Think of it like:

> “Do this action X number of times.”
> 

---

### ⚙️ **2️⃣ Syntax**

```jsx
for (initialization; condition; increment/decrement) {
  // code to repeat
}

```

💡 Here’s what each part does:

1. **Initialization** → sets a starting point (e.g. `let i = 1`)
2. **Condition** → loop runs while this is `true`
3. **Increment/Decrement** → changes the variable each time (e.g. `i++`)

---

### 💡 **3️⃣ Example – Counting Numbers**

```jsx
for (let i = 1; i <= 5; i++) {
  console.log(`Count: ${i}`);
}

```

🧩 Output:

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5

```

---

### ⚡ **4️⃣ Counting Backward**

```jsx
for (let i = 5; i > 0; i--) {
  console.log(`Countdown: ${i}`);
}
console.log("🎉 Blast off!");

```

🧩 Output:

```
Countdown: 5
Countdown: 4
Countdown: 3
Countdown: 2
Countdown: 1
🎉 Blast off!

```

---

### 🧩 **5️⃣ Looping Through a String**

```jsx
let name = "Pratham";

for (let i = 0; i < name.length; i++) {
  console.log(name[i]);
}

```

🧩 Output:

```
P
r
a
t
h
a
m

```

---

## 💥 **Break Statement**

### 💡 What It Does:

Stops the loop **immediately** ⛔ when a certain condition is met.

---

### ⚙️ Example – Stop at 3

```jsx
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    break;
  }
  console.log(i);
}

```

🧩 Output:

```
1
2

```

💬 As soon as `i === 3`, the loop **breaks** and stops running.

---

## ⚡ **Continue Statement**

### 💡 What It Does:

**Skips** one iteration and moves to the next loop cycle ⏩

---

### ⚙️ Example – Skip 3

```jsx
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    continue;
  }
  console.log(i);
}

```

🧩 Output:

```
1
2
4
5

```

💬 The loop **skipped** `3`, but continued with the rest.

---

## 🔄 **6️⃣ Combining Break and Continue**

```jsx
for (let i = 1; i <= 10; i++) {
  if (i === 5) {
    console.log("Skipping 5...");
    continue; // skip this one
  }
  if (i === 8) {
    console.log("Stopping at 8!");
    break; // stop completely
  }
  console.log(i);
}

```

🧩 Output:

```
1
2
3
4
Skipping 5...
6
7
Stopping at 8!

```

---

### 

## For loop will repeat the code limited amount of times

```jsx
// for loop 
for(let i =0; i<=2 ; i++){
    console.log("hello");
    console.log(i);// output 0 1 2 
}// output hello three times 

for(let i = 1; i<=20; i++){
    if(i== 13){
        continue
    }
    else{
        console.log(i);
    }// here it will show all number between 1 to 20 except the 13 number 
}

for( let i= 1;  i<=20; i++){
    if(i==13){
        break;
    }
    else{
        console.log(i);// it will break at 12 and exit the loop 
        
}
}
```