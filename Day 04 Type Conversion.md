# Type conversion in javascript

## 🧠 1️⃣ What is Type Conversion?

Type conversion means **changing one data type into another**.

Example:

You get input from a user as a **string** (like `"42"`) but you want to use it as a **number** for calculations → so you **convert** it.

There are two types:

- 🧩 **Implicit Conversion** → done automatically by JS
- ⚙️ **Explicit Conversion** → done manually by you

## 💡 2️⃣ Implicit Conversion (a.k.a. Type Coercion)

JavaScript is a *smart* (and sometimes sneaky 😅) language — it converts data types behind the scenes when it needs to.

Example:

```jsx
console.log("5" + 2); // "52"  -> JS turns 2 into a string
console.log("5" - 2); // 3    -> JS turns "5" into a number
console.log("5" * "2"); // 10 -> both get converted to numbers

```

📌 **Rule of thumb:**

- `+` tries to make things **strings**
- -,* , `/`, `%` try to make things **numbers**

## 🧩 3️⃣ Explicit Conversion (You do it manually)

Here’s how you take control 💪

## Type conversion =  change the datatype of a value to another

## ( number - boolean - strings )

                                                          

```jsx
let age ;
age = window.prompt(" how old are you??");// here we are accepting the user input as string 
age +=1; 
console.log(age);// output 181 not 19 because it is string which is not converted into number so sting catination happens
// type conversion 
let age = window.prompt("how old are you ");
age = Number(age);// reassingning the varible with type conversion like form string to number 
age +=1;
console.log(age, typeof age);// output now  the output is 19 when enter 18 and number 

let x = "pratham ";
let y = " pratam";
let z = "pratham";

x = Number(x);// this convert data type into number 
y = String(y);// this convert data type into string 
z = Boolean(z);// this convert the data type into boolean 
console.log(x , typeof x);// output NaN 'number'
console.log(y , typeof y);// output  pratam string
console.log(z , typeof z);// output true 'boolean'

console.log(Boolean(1));    // true
console.log(Boolean(0));    // false
console.log(Boolean("hi")); // true (non-empty string)
console.log(Boolean(""));   // false (empty string)

```

📌 Truthy = values JS treats as true (

```
1
```

,

```
"text"
```

,

```
true
```

, etc.)

📌 Falsy = values JS treats as false (

```
0
```

,

```
""
```

,

```
null
```

,

```
undefined
```

,

```
NaN
```

,

```
false
```

)