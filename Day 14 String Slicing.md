# String slicing in javascript

### 🧠 **1️⃣ What Is String Slicing?**

**Slicing** means taking a *portion* of a string — kind of like saying:

> “Hey, I just want characters from here 👈 to there 👉.”
> 

In JavaScript, we do that using:

- `slice(start, end)`
- `substring(start, end)`
- `substr(start, length)` (⚠️ older, not commonly used anymore)

---

### 💡 **2️⃣ The `.slice()` Method**

Syntax:

```jsx
string.slice(startIndex, endIndex)

```

🧩 **How it works:**

- It starts **at** `startIndex` (included)
- Stops **before** `endIndex` (excluded)

Example:

```jsx
let name = "Pratham";
let sliced = name.slice(0, 3);
console.log(sliced); // "Pra"

```

💬 Explanation:

- Starts at index 0 (P)
- Stops before index 3 (t → excluded)

---

### ⚙️ **3️⃣ Omitting the End Index**

If you only give a **start index**, JavaScript slices *till the end*.

```jsx
let city = "PuneCity";
console.log(city.slice(4)); // "City"

```

---

### 🌀 **4️⃣ Using Negative Indexes**

Negative values count from the **end** of the string 😎

```jsx
let word = "JavaScript";
console.log(word.slice(-6));   // "Script"
console.log(word.slice(-10, -6)); // "Java"

```

💬 So useful when you don’t know the exact length of a string but want the *last few characters*.

---

### 💥 **5️⃣ `.substring()` vs `.slice()`**

Both seem similar, but there’s a small difference 👇

| Method | Negative Values | Swap Index Order |
| --- | --- | --- |
| `slice()` | ✅ Works with negative | ❌ Doesn’t swap |
| `substring()` | ❌ Treats negatives as 0 | ✅ Swaps if start > end |

Example:

```jsx
let name = "Pratham";

console.log(name.slice(2, 6));      // "atha"
console.log(name.substring(6, 2));  // "atha" (swapped automatically)

```

So — most developers prefer **`slice()`** for clarity 🧠

---

### 🧩 **6️⃣ `.substr()` (Old School)**

```jsx
let text = "JavaScript";
console.log(text.substr(4, 6)); // "Script"

```

⚠️ It uses **(start, length)** instead of **(start, end)**.

It’s outdated now but good to know in case you see it in old code.

---

### 🎯 **7️⃣ Real Example – Extracting a Username from Email**

```jsx
let email = "pratham.shinde@example.com";
let username = email.slice(0, email.indexOf("@"));
console.log(username); // "pratham.shinde"

```

🔥 Smart way to use `slice()` + `indexOf()` together.

## String slicing = creating a substring from a portion of another string            string.slice(start , end )

```jsx
const fullname = "partham shinde";
let firstname = fullname.slice(0,8);
let lastname = fullname.slice(8, 15);
let firschar = fullname.slice(0,1);// for the first character 
let lastchar = fullname.slice(-1);// we use the negative index for getting the last character 

console.log(firstname);
console.log(lastname);
console.log(firschar);
console.log(lastchar);

const fullname = "pratham shinde";
let firstname = fullname.slice(0, fullname.indexOf(" "));// we can use that when we dont want to count the index manually 
let lastname = fullname.slice( fullname.indexOf(" ") + 1);// here adding plus 1 means star after the space 
console.log(firstname);
console.log(lastname);

const email = "prathamshinde@gmail.com";
let username = email.slice(0, email.indexOf("@"));
let extension = email.slice(email.indexOf("@") +1);
console.log(username);// output prathamshinde
console.log(extension);//output gmail.com

```