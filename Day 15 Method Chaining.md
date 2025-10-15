# Method chaining in javascript

### 🧠 **1️⃣ What Is Method Chaining?**

**Method chaining** means calling **multiple methods in one line**, one after another, instead of writing them separately.

Each method *returns a value* that the next method can act on.
  
💬 Think of it like a pipeline — data goes through multiple transformations, one after the other 🚀
// it is very important in js
---

### 💡 **2️⃣ Example Without Chaining**

```jsx
let username = "   pratham shinde   ";
username = username.trim();
username = username.toUpperCase();
username = username.replace("PRATHAM", "PRATHAM S.");
console.log(username);

```

🧩 Output:

```
PRATHAM S. SHINDE

```

---

### ⚙️ **3️⃣ Example With Method Chaining**

Now let’s make that same thing **cleaner and cooler 😎**

```jsx
let username = "   pratham shinde   ";

let result = username
  .trim()
  .toUpperCase()
  .replace("PRATHAM", "PRATHAM S.");

console.log(result);

```

🧩 Output:

```
PRATHAM S. SHINDE

```

💬 Both do the same thing — but the chained version is:

✅ Shorter

✅ Cleaner

✅ Easier to read

---

### ⚡ **4️⃣ How Does It Work?**

Each method (like `.trim()`, `.toUpperCase()`, `.replace()`) returns a **new string**.

So you can immediately call another method on that result.

⚠️ Important: Not all methods return something you can chain!

For chaining to work, the method must return the same type of object (like a string).

Example — this won’t work 👇

```jsx
let name = "Pratham";
console.log(name.length.trim()); // ❌ Error: .trim is not a function

```

Because `.length` returns a number, not a string — so you can’t chain string methods after it.

---

### 🧩 **5️⃣ Another Example – Formatting Input**

```jsx
let email = "   PRATHAM.SHINDE@GMAIL.COM   ";

let cleanEmail = email
  .trim()
  .toLowerCase()
  .replace("gmail", "outlook");

console.log(cleanEmail);

```

🧩 Output:

```
pratham.shinde@outlook.com

```

💡 Nice and simple — three clean operations chained together.

---

### 🎯 **6️⃣ Real-Life Example – Username Formatter**

Let’s say you’re creating a signup form and want to clean the username properly 👇

```jsx
let rawUsername = "   PrAthAm_Shinde   ";

let formatted = rawUsername
  .trim()
  .toLowerCase()
  .replace("_", " ");

console.log(formatted);

```

🧩 Output:

```
pratham shinde

```

🔥 Boom! Perfectly formatted username in one chain!

## Method chaining = method chaining is a programic technique use to call one method after another in one continous line of code

## Program using no method chaining

```jsx
let username = window.prompt("enter the user name");
username = username.trim();
let letter = username.charAt(0);
letter = letter.toUpperCase();
let extraletter = username.slice(1);
extraletter = extraletter.toLocaleLowerCase();
username = letter + extraletter;
console.log(username);
// output pratham 
```

## Program using method chaining

```jsx
let username = window.prompt("enter the name ");
username = username.trim().charAt(0).toLocaleUpperCase() + username.trim().slice(1).toLocaleLowerCase();// we have use 
// plus sign for sting catination 
console.log(username);
```