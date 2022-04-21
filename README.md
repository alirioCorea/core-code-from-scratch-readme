# Week 1 : Introduction to programming & Javascript 
## Week challenges (Tuesday)
### What is a compiled languages.
A compiled language is a programming language where a computer convert directly into machine code  the program and it can execute it. That also makes them faster and more efficient.
### What is a interpreted languages.
An interpreted language is a programming language where a program called interpreter runs the code. The program is not read by the target machine but instead read and executed by some other program.
### Is Java compiled or interpreted, or both?
Java is a particular language because it is compiled into an intermediate language called bytecode, which is then interpreted. So what we can see is that Java is a special lenguage because use both ways to arrive at the final step.
### Pseudocode currency converter.
`Algorithm`
```javascript
Start
#cantidad<-- GET ;
#bitcoin_dolar<--GET From (https://coinmarketcap.com/es/currencies/bitcoin/);
#total <-- #cantidad * #bitcoin_dolar;
PRINT #total;
End

```
## Week challenges (Wednesday) 
Your team has just seen the movie "Matrix" and you have been asked, how the number of your year of birth would be written in binary. You must learn how to translate your date of birth into binary and show your team. (Do not use a webpage or a tool to convert your date of birth)
### Your date of birth in the matrix?
My birthday: 2000.

![This is an Image](https://raw.githubusercontent.com/alirioCorea/core-code-from-scratch-readme/main/Screenshot%202022-04-07%20192307.png)

My birthday in binary: 1111101000.

### MIPS
Based on the [guide](htthttps://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e2/descp:// "guide") and the examples of the low-level language, create the following

1. Create a program that adds any two given numbers provided by the user
2. Create a program that displays your name

`A program that adds any two numbers`

```
 .data
	      number1: .asciiz "\nIngrese el primer numero: "
	      number2: .asciiz "\nIngrese el segundo numero: "
	      result: .asciiz "\nLa suma es : "
  .text
	      main
	      #Mensaje para ingresar el primer numero
              li $v0, 4
              la $a0, number1
              syscall
              
              #Entrada del primer numero
              li $v0, 5
              syscall
              
              #Guardo la variable
              move $t0, $v0
              
              ##Mensaje para ingresar el segundo numero
              li $v0, 4
              la $a0, number2
              syscall
              
              #Entrada del segundo numero
              li $v0, 5
              syscall
              
              #Guardo la variable
              move $t1, $v0
              
              #Hago la suma      
              add $t2, $t0, $t1
              
              #Imprimo el resultado             
              li $v0, 4
              la $a0, result
              syscall

              li $v0, 1
              move $a0, $t2
              syscall
```

`A program that displays your name`

```
  .data
	      name: .asciiz "\nNombre: Josue Alirio Corea"
  .text
	      main:
              li $v0, 4
              la $a0, name
              syscall
```

## Week challenges (Thursday)
### Print special numbers
#### Description
In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise

`Even numbers in the range of numbers from 0 to 100`
```javascript
for(let i=0;i<=100;i++){
    if(i%2===0){
        console.log(i);
    }
}
```
### Bad code
#### Description
The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code
```javascript
var cond = false;

if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```
`My solution`
```javascript
var cond = false;

if (cond) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

### Bad code 2
#### Description
You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly

```javascript
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}
```

`My solution`

```javascript
var n = 10;

if (n === 100) {
  console.log('This is a special number!');
}
else if (n < 1000 && n % 10 == 0) {
    console.log('This number is almost special');
} else {
  console.log('Just a regular number')
}

```
# Week 2 : Javascript
## Week challenges (Monday) 
- [x] Follow the github course, you can find it here
- [x] Create an account in Codewars, follow this instructions
- [x] Read about: if...else
- [x] Read about: for
- [x] Read about: while
- [x] Read about: functions

## Week challenges (Tuesday) 
### 1. Multiply exercise
This code does not execute properly. Try to figure out why.
```javascript
function multiply(a, b){
	a * b
}
```
`My solution`
```javascript
function multiply(a, b){
	let c = a * b;
	return c;
}
```

### 2. ASCII Total exercise
You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.
```javascript
function uniTotal (string) {
    let total=0;
    for(let i=0;i<string.length;i++){
        total+=string[i].charCodeAt();
    }
    return total;
}
```

### 3. Char From ASCII Value exercise
Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value.

```javascript
function getChar(c){
    let chart=String.fromCharCode(c);
    return chart;
  }
```
### 4.Binary Addition exercise
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.
The binary number returned should be a string.

```javascript
function addBinary(a,b) {
    let total=a+b;
    return total.toString(2);
}
```

### 5.Student's Final Grade exercise
Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

```javascript
function finalGrade (exam, projects) { 
    let notaFinal=0;
    if(exam>90 || projects>10){
        notaFinal=100;
    }
    else if(exam > 75 && projects >= 5){
        notaFinal=90;
    }
    else if(exam > 50 && projects >= 2){
        notaFinal=75;
    }
    return notaFinal;
  }

```
