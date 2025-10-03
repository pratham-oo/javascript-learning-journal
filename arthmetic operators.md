# Arthmetic operators in javascript

### 1️⃣ What are Arithmetic Operators?

They’re symbols we use to do math with numbers. Think of them like your calculator 🧮, but inside code.

Arthemtics operators = operands (values , variables , etc..)

                                              operators (+, -, *, /)

                                              ex 11 = x +5;

### 2️⃣ The main operators

| Operator | Example | Meaning | Result |
| --- | --- | --- | --- |
| `+` | `5 + 3` | Addition | `8` |
| `-` | `5 - 3` | Subtraction | `2` |
| `*` | `5 * 3` | Multiplication | `15` |
| `/` | `10 / 2` | Division | `5` |
| `%` | `10 % 3` | Modulus → remainder | `1` |
| `**` | `2 ** 3` | Exponent → power | `8` |

code :

```jsx
let students = 60;
students = students + 4; // this is how you can reassign the varible for any arhtmetic operation 
console.log(students);// 64
students = students * 5; //multiplication 
console.log(students);// output 320 
students = students/4;// division 
console.log(students);//output 80
students =  students - 5;// subtraction 
console.log(students);// output 75
students = students**2;// exponential 
console.log(students);// output 5625
let extrastudents = students % 2; // modulus operator it gives you the remainder of any division  and 
// it is recommended that while using the modulus operator we use a new variable to get the accurate answer 
console.log(extrastudents); // output 1
```

## Augmented assignment operators

👉 With **augmented operators**, you can write it shorter:

| Operator | Long way | Short way (Augmented) | Result |
| --- | --- | --- | --- |
| `+=` | `x = x + 5;` | `x += 5;` | Adds and stores |
| `-=` | `x = x - 3;` | `x -= 3;` | Subtracts and stores |
| `*=` | `x = x * 2;` | `x *= 2;` | Multiplies and stores |
| `/=` | `x = x / 4;` | `x /= 4;` | Divides and stores |
| `%=` | `x = x % 2;` | `x %= 2;` | Stores remainder |
| `**=` | `x = x ** 3;` | `x **= 3;` | Power and store |

```jsx
let students = 30;
 students += 2;
 console.log(students);
 students -= 2;
 console.log(students);
 students *= 2;
 console.log(students);
 students /= 2;
 console.log(students);
 students **= 2;
 console.log(students);
 students %= 2;// modulus operator can be used to determine whihc number is even or odd like now we have 
 // number 30 the ouput is 0 so it is the even number 
 // when we make the number to 31 the output becomes 1 so it is odd number 
 console.log(students);

```

## Increment operator

`++` → adds 1 to a number.

```jsx
let students =  30;
students ++;// this is increment operator which will increment the value by one 
console.log(students);// output 31 

```

## Decrement operator

 `--` → subtracts 1 from a number.

```jsx
let students = 30 ; 
students --; // this is decrement operator whih will decrement the value by one 
console.log(students);// output 29

```

⚠️ There’s also a difference between:

- **Post-increment (`num++`)** → increases after using the value.
- **Pre-increment (`++num`)** → increases before using the value

```jsx
let x = 5;
console.log(x++); // prints 5, then x becomes 6
console.log(++x); // x becomes 7, then prints 7
// outut 5 
// 7 
let a = 5;

console.log(a++); // prints 5, then a becomes 6
console.log(a);   // prints 6 (after increment)

let b = 5;
console.log(++b); // b becomes 6 first, then prints 6
console.log(b);   // still 6
```

## Operators precendence

1. Parenthesis ()
2. exponents 
3. multiplication & division & modulo 
4. addition & subtraction 

```jsx
// operator precedence 
let result = 1 + 2 *3 + 4 **2 + 2 / 2; // by usig operator precendence 
console.log(result);// output 24 
let results = 12 % 5 + 8 / 4; 
console.log(results); // output 4
let result =  6 / 2 ** (2 +5);
 console.log(result);// output  0.046875

```

## Basic excercise

```jsx
let fullname = "pratham shinde";
let age = 20; 
let score = 10; 
let isstudent = true;
document.getElementById("p1").textContent = ` my name is ${fullname}`;
document.getElementById("p2").textContent = ` my age is ${age}`;
document.getElementById("p3").textContent = `my score is ${score}`;
document.getElementById("p4").textContent = `enrolled in college : ${isstudent}`;
score += 5 ;
document.getElementById("p5").textContent = ` the score of pratham after adding 5 : ${score}`;
score -= 5;
document.getElementById("p6").textContent = ` the score of pratham after subtracting 5: ${score}`;

let number = 5;
number++;
number;
document.getElementById("p7").textContent = `the number shows 5 and then become 6: ${number}`
++number;
number;
document.getElementById("p8").textContent = ` the number add first then shows 7 : ${number}`

```