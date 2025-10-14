# Strict equality in javascript

### 🧠 **1️⃣ What Is Equality in JavaScript?**

In JavaScript, there are **two ways** to compare values for equality:

| Type | Operator | Checks | Example |
| --- | --- | --- | --- |
| **Loose Equality** | `==` | Only checks **value** (not type) | `"5" == 5` ✅ |
| **Strict Equality** | `===` | Checks **value + type** | `"5" === 5` ❌ |

💬 So basically:

- `==` says “Eh, close enough!” 😅
- `===` says “Nope, it must be *exactly* the same — both type and value!” 💪

---

### 💡 **2️⃣ Loose Equality (`==`) Example**

```jsx
console.log(5 == "5");   // true
console.log(0 == false); // true
console.log(null == undefined); // true

```

😬 These are **true** because `==` automatically converts data types before comparing — this is called **type coercion**.

---

### ⚙️ **3️⃣ Strict Equality (`===`) Example**

```jsx
console.log(5 === "5");   // false
console.log(0 === false); // false
console.log(null === undefined); // false

```

🧠 Here, strict equality checks both:

1. The **value**
2. The **data type**

So `"5"` (a string) and `5` (a number) are *not the same* ❌

---

### 🧩 **4️⃣ Strict Inequality (`!==`)**

The opposite of strict equality.

It checks if **value or type** is *not the same*.

```jsx
console.log(5 !== "5");  // true
console.log(10 !== 10);  // false

```

---

### 💬 **5️⃣ Real-World Example**

Imagine you’re checking a user’s PIN code 🔒

```jsx
let pinFromUser = "1234";
let actualPin = 1234;

if (pinFromUser === actualPin) {
  console.log("✅ Access granted!");
} else {
  console.log("❌ Incorrect PIN!");
}

```

🧩 Output:

```
❌ Incorrect PIN!

```

Why? Because `"1234"` is a **string**, not a **number** — and `===` checks both.

---

### 🎯 **6️⃣ When Should You Use Which?**

✅ Always use `===` and `!==` in modern JavaScript —

They’re **safer**, **predictable**, and **avoid weird bugs**.

❌ Avoid `==` and `!=` unless you *really* understand type coercion (which most devs avoid anyway 😅).

---

### 🔍 **7️⃣ Quick Type Coercion Examples**

```jsx
console.log(true == 1);   // true
console.log(false == 0);  // true
console.log("0" == false); // true
console.log("0" === false); // false

```

💡 `==` tries to *convert* both sides to a similar type before comparing —

`===` does *no conversion* at all.

```jsx
// = assignment operator
//== comparison operator 
//=== strict equality operators (compares if value adn datypes are equal)
//!= inequality operator 
//!== strich inequality operator 

const PI = 3.14;
if(PI == "3.14"){// comparison operators only compare the value not te data type 
    console.log("it is a pi");
}
else{
    console.log("This is not an PI");
}// it is pi 

//stict equality operator 
const PI = 3.14;
if(PI === "3.14"){// strictequality  operators checks both the value and datatype 
    console.log("it is a pi");
}
else{
    console.log("This is not an PI");
}// this is not a PI

//inequality operator 
const PI = 3.14;
if(PI != 3.13){// not equal to operator 
    console.log("this is not pi");
}
else{
    console.log("this is pi");
}// this is pi 

//stictly ineuality operators
const PI = 3.14;
if(PI !== 3.13){// this checks the value and data type both 
    console.log("this is not pi");
}
else{
    console.log("this is pi");
}// this is not pi
```