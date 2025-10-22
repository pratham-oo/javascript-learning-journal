# Variable scope in javascript

### 🧠 **1️⃣ What Is “Scope”?**

**Scope** decides *where* in your code a variable can be used or accessed.

💬 Think of it like this:

> Some variables live in the whole city (global),
> 
> 
> while others live only inside a *house* (local).
> 

---

### 🗺️ **2️⃣ Types of Scope**

JavaScript mainly has **two** types of scope:

1. 🌍 **Global Scope**
2. 🏠 **Local Scope (Function or Block Scope)**

---

### 🌍 **3️⃣ Global Scope**

A variable declared *outside* of any function or block can be used **anywhere** in your code.

```jsx
let city = "Pune";

function showCity() {
  console.log(city); // accessible here
}

showCity();
console.log(city); // also accessible here

```

🧩 Output:

```
Pune
Pune

```

✅ Since `city` is global, both inside and outside code can access it.

---

### 🏠 **4️⃣ Local (Function) Scope**

Variables declared *inside a function* exist **only** inside that function.

```jsx
function greet() {
  let name = "Pratham";
  console.log(`Hello, ${name}`);
}

greet();
console.log(name); // ❌ ERROR - name is not defined

```

💬 The variable `name` only exists *inside* the function —

once the function ends, it’s gone!

---

### 🧩 **5️⃣ Block Scope (`let` and `const`)**

Variables declared with `let` or `const` inside `{}` (like if/else or loops)

are **block-scoped**, meaning they only exist inside those curly braces.

```jsx
{
  let x = 10;
  console.log(x); // ✅ Works
}
console.log(x); // ❌ Error - x is not defined

```

---

### ⚠️ **6️⃣ `var` is Function-Scoped (Not Block-Scoped)**

Unlike `let` and `const`, variables declared with `var` **ignore** block scope.

```jsx
{
  var num = 100;
}
console.log(num); // ✅ Works - because var is not block-scoped

```

⚠️ This is why modern JavaScript developers prefer using `let` and `const`.

---

### 🧠 **7️⃣ Summary Table**

| Type | Declared Using | Scope Type | Accessible Outside Block | Redeclarable |
| --- | --- | --- | --- | --- |
| `var` | var | Function Scope | ✅ Yes | ✅ Yes |
| `let` | let | Block Scope | ❌ No | ❌ No |
| `const` | const | Block Scope | ❌ No | ❌ No |

---

### 💻 **8️⃣ Example Combining All**

```jsx
let a = 10; // global

function testScope() {
  let b = 20; // local
  if (true) {
    let c = 30; // block
    var d = 40; // function scoped (not block scoped)
    console.log(a, b, c, d); // ✅ all accessible here
  }
  console.log(a, b, d); // ✅ c is not accessible here
}

testScope();
console.log(a); // ✅
console.log(b); // ❌ Error

```

## Variable scop means where variable is recognised and accessible (local vs global)

```jsx
function1();// any varibale declared inside of an function has a local scope 
function function1(){// function cannot see what is ther inside the other function because they local scope 
    let x = 1;
    console.log(x);
}
// you can declare variable with the same if ther are inside the curly brackets 
// so inside a function or curly bracketes you declared the variable with same name and 
// that will not a cause name conflict 
function function2(){
    let x = 2;
    console.log(x);
}

// global scope 

let x = 3; // declared variable outside the function so that it becomes 
// global and can accessed by any function 
function1();
function function1(){
    console.log(x);
}
// so here if i call any one function it will give me the value 3 becase i have declared it globally
// which means it is available globally 
function function2(){
    console.log(x);
}// in large and complex program it is recommended that you use local varible rather then 
// global because global willl caue name conflict 

if we have two variable with same name and it is called but both are differntly scoped 
then the varibale with local scop will execute first !!
```