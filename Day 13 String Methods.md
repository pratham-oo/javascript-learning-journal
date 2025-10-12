# String methods in javascript

---

### 🧠 **What Are String Methods?**

👉 A **string method** is basically a **built-in function** that you can use to **manipulate or analyze** text.

Every string in JavaScript comes with these helpful tools.

Example:

```jsx
let name = "Pratham";
console.log(name.length); // 7

```

Here, `.length` is a **property** (not a method), but many others are **methods** (functions that use parentheses like `.toUpperCase()`).

---

### 💡 **2️⃣ Common String Methods**

Let’s go through the most useful ones 👇

---

### ✅ **`toUpperCase()` & `toLowerCase()`**

Convert text to uppercase or lowercase 🆙🔡

```jsx
let city = "pune";
console.log(city.toUpperCase()); // PUNE
console.log(city.toLowerCase()); // pune

```

---

### ✅ **`charAt(index)`**

Gives the character at a certain position (index starts from 0).

```jsx
let name = "Pratham";
console.log(name.charAt(0)); // P
console.log(name.charAt(3)); // t

```

---

### ✅ **`indexOf()` & `lastIndexOf()`**

Find where a substring appears in a string.

```jsx
let message = "I love JavaScript and JavaScript loves me!";
console.log(message.indexOf("JavaScript"));      // 7
console.log(message.lastIndexOf("JavaScript"));  // 22

```

If not found → returns `-1`.

---

### ✅ **`slice(start, end)`**

Extracts part of a string.

```jsx
let fruit = "Mango";
console.log(fruit.slice(0, 3));  // Man
console.log(fruit.slice(1));     // ango

```

⚡ Tip: negative numbers count from the end 👇

```jsx
console.log(fruit.slice(-2)); // go

```

---

### ✅ **`replace(oldValue, newValue)`**

Replace part of a string.

```jsx
let text = "I love cats";
let newText = text.replace("cats", "dogs");
console.log(newText); // I love dogs

```

---

### ✅ **`replaceAll()`**

Replaces *all* occurrences (unlike `replace()` which only changes the first one).

```jsx
let text = "JS is fun. JS is powerful!";
console.log(text.replaceAll("JS", "JavaScript"));

```

🧩 Output:

```
JavaScript is fun. JavaScript is powerful!

```

---

### ✅ **`trim()`**

Removes spaces from **both ends** of a string (super handy for user input).

```jsx
let username = "   pratham   ";
console.log(username.trim()); // "pratham"

```

---

### ✅ **`includes()`**

Checks if a string contains another string → returns `true` or `false`.

```jsx
let email = "pratham@example.com";
console.log(email.includes("@")); // true

```

---

### ✅ **`startsWith()` & `endsWith()`**

Check how a string begins or ends.

```jsx
let filename = "notes.txt";
console.log(filename.startsWith("notes")); // true
console.log(filename.endsWith(".txt"));    // true

```

---

### ✅ **`concat()`**

Joins multiple strings (though `+` is used more often).

```jsx
let firstName = "Pratham";
let lastName = "Shinde";
console.log(firstName.concat(" ", lastName)); // Pratham Shinde

```

---

### ✅ **`split()`**

Turns a string into an **array**, based on a separator.

```jsx
let data = "HTML,CSS,JavaScript";
let arr = data.split(",");
console.log(arr); // ["HTML", "CSS", "JavaScript"]

```

---

### 💥 **3️⃣ Combine Methods Like a Pro**

You can chain multiple methods together 👇

```jsx
let sentence = "   javascript is Awesome!   ";
let result = sentence.trim().toUpperCase().replace("AWESOME", "FUN");
console.log(result); // JAVASCRIPT IS FUN!

```

## String methods = string methods allow you to manipulate with text (strings)

```jsx
// string methods 
// charAt() method 
let username = "         pratham shinde       ";
console.log(username.charAt(2));// charAt()method 
// output a
// indexof() method will return the index of the value 
console.log(username.indexOf("t"));// output is 3 
//lastindeof() method will return the s
// second letters index which is repeated 
console.log(username.lastIndexOf("a"));// output is 5 
// lengt property is used to get the length of the string 
console.log(username.length);// output is 14
// trim method to delete the spaces after or befor the value 
username = username.trim();
console.log(username);// output is pratham shidne withou the space 
console.log(username.toUpperCase());// this is method will upper case the strings 
// output is PRATHAM SHINDE 
console.log(username.toLocaleLowerCase());// this is method will lower case the strings 
// output is pratham shinde 
username = username.repeat(3);// if you want to repeat the string 
console.log(username);// output is pratham shindepratham shindepratham shinde

let username = " pratham"
let result = username.startsWith(" ");// check for wether your user has this or that 
if(result){
    console.log("your user name cannot start with space")
}
else{
    console.log(username);
}//  output is your user name cannot start with space

let username = " pratham "
let result = username.endsWith(" ");// check for wether your user has this or that 
if(result){
    console.log("your user name cannot end with space")
}
else{
    console.log(username);
}//  output is your user name cannot ends with space

let username = " pratham shinde "
let result = username.includes(" ");// check for wether string include this or that 
if(result){
    console.log("your user name cannot include space in between")
}
else{
    console.log(username);
}//  output is your user name cannot include space  in between 

let phonenumber = "123-456-7890";
phonenumber = phonenumber.replaceAll("-" ,"");// this method is used to replace anything inside the stings 
console.log(phonenumber);// output is 1234567890

// pad start method means padding the string with a value unitl the certain value is met 
 let phonenumber = "123-456-7890";
 phonenumber = phonenumber.padStart(15 ,"0");
 console.log(phonenumber);// ouput is 000123-456-7890
 
 
let phonenumber = "123-456-7890";
phonenumber = phonenumber.padEnd(15 ,"0");
console.log(phonenumber);// ouput is 123-456-7890000

```