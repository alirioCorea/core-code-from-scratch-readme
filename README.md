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
```
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

###MIPS
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
