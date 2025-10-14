# Logical operators in javascript

### 🧠 **1️⃣ What Are Logical Operators?**

Logical operators are used to **combine or compare multiple conditions** (like in `if` statements).

There are **three main logical operators** in JavaScript 👇

| Operator | Symbol | Meaning | Example |
| --- | --- | --- | --- |
| AND | `&&` | True if **both** conditions are true | `a > 0 && b > 0` |
| OR | ` |  | ` |
| NOT | `!` | **Reverses** the condition (true → false, false → true) | `!(a > 0)` |

---

### 💡 **2️⃣ Example: AND Operator (`&&`)**

Both sides must be **true** for the result to be true ✅

```jsx
let age = 20;
let hasLicense = true;

if (age >= 18 && hasLicense) {
  console.log("✅ You can drive!");
} else {
  console.log("❌ You cannot drive yet.");
}

```

🧩 Output:

```
✅ You can drive!

```

If either one is false (say `age = 16`), the condition fails.

---

### 💡 **3️⃣ Example: OR Operator (`||`)**

At least **one** condition must be true ✅

```jsx
let day = "Sunday";

if (day === "Saturday" || day === "Sunday") {
  console.log("🎉 It’s the weekend!");
} else {
  console.log("💼 It’s a weekday.");
}

```

🧩 Output:

```
🎉 It’s the weekend!

```

---

### 💡 **4️⃣ Example: NOT Operator (`!`)**

It **flips** the condition’s truth value.

```jsx
let isRaining = false;

if (!isRaining) {
  console.log("☀️ Let’s go outside!");
} else {
  console.log("🌧️ Stay inside!");
}

```

🧩 Output:

```
☀️ Let’s go outside!

```

---

### ⚙️ **5️⃣ Combine Them All!**

You can use multiple logical operators together 👇

```jsx
let temperature = 25;
let isSunny = true;

if (temperature > 20 && isSunny || temperature > 30) {
  console.log("🌞 Perfect day for a picnic!");
} else {
  console.log("🥶 Maybe stay in today.");
}

```

🧩 Output:

```
🌞 Perfect day for a picnic!

```

---

### 🧠 **6️⃣ Truthy and Falsy Values**

Logical operators also work with **truthy** and **falsy** values (not just `true`/`false`).

In JavaScript, these are considered **falsy**:

```
false, 0, "", null, undefined, NaN

```

Everything else is **truthy**.

Example:

```jsx
if ("hello" && 5) console.log("✅ This is truthy!");

```

🧩 Output:

```
✅ This is truthy!

```

## logical operators = They are used to manipulate boolean value

## There are three logical operators

1. And= &&
2. or = ||
3. Not = !

```jsx
const temp = 200;// temp in celcius 
if(temp >0){
    console.log("temperature is good");
}
else if(temp>30){
    console.log("temperature is good");
}
else {
    consle.log("the weathe is bad ");
}// if i am putting here 200 still i am getting the oouput is the temp is good 

// usiing the logical operator 
const temp = 200;
if(temp >0 && temp<=30){
    console.log("weather is good")
}
else {
    console.log("weather is bad ")
}// weather is bad 

// using or operators 
const temp = 100;
if(temp <=0 || temp>=30){
    console.log("weather is bad")// in this it checks either one conditon is true S
}
else {
    console.log("weather is good ")
}// weather is bad 

// using not operator 
const issunny = true;
if (!issunny){
    console.log("it is cloudy");// it changes from true to false 

}
else {
    console.log("it is sunny");
}

```