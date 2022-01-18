# FIRST WEEK ACTIVITY

## Tuesday activity

  ### 1. Watch [this](https://www.youtube.com/watch?v=JNMy969SjyU) video about compilation and interpretation
   - Done
     
  ### 2. Java languaje is compiled or interpreted?
   - R: Java can be considered both a compiled and an interpreted language because its source code is first compiled into a binary byte-code. 
    This byte-code runs on the Java Virtual Machine (JVM), which is usually a software-based interpreter
    
  ### 3. Create an algorithm to calculate the equivalent of your local currencty to USD
   - Find the conversion rate of the local currency
   - Divide the local currency by the amount that you want
   - Calculate how much money you will have after the change

  ### 4. Read about Pseudocode [here](https://www.freecodecamp.org/news/what-is-pseudocode-in-programming/)
   - Done
 
  ### 5. Why is pseudocode helpful?
   - R: Pseudocode is usefull to getting started with software programming because you can learn the logic without the strict syntax rules and its easy to understand with other people
 
  ### 6. Create a pseudocode to calculate the aproximated age of a user base on the year they born
   - Start
   - Y: 2022; --- *año actual*
   - Year_birth: input; --- *solicitamos el año de nacimiento del usuario*
   - Age: Y-Year_birth; --- *restamos el año actual con el año de nacimiento del usuario*
   - print(Age); --- *Mostramos en pantalla la edad del usuario*
   - End
 
  ### 7. Read about flowcharts [here](https://www.lucidchart.com/pages/es/que-es-un-diagrama-de-flujo)
   - Done
  
  ### 8. Why are flowcharts important to us as developers?
   - R: With flowcharts we can determine the operation of a project and better define its development
  
  ### 9. Search about High-level languages and Low-level languages, you can start with [this](https://www.youtube.com/watch?v=1vRPOp5p-qs) video
   - Done

## Wednesday activity

  ### 1. Learn about binary, decimal and hexadecimal numbers
   - Done
   
  ### 2. Translate the year you where born to binary, decimal and hexadecimal
   - Decimal: 2001
   - Hexadecimal: 7D1
   - Binary: 11111010001
 
  ### 3. Translate 51966 into hexadecimal and binary
   - Hexadecimal: CAFE
   - Binary: 1100101011111110
  
  ### 4. Use a Low-level language, for example MIPS aseembler
   - Done
  
  ### 5. Base on the examples and the guide of the low-level language:
   5.1 Create a program to add two numbers given by the user<br></ol>
      
   <pre>
.data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
	result_message: .asciiz "\nEl resultado es: "
.text
	main:
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0
		
		add $t2, $t0, $t1

		li $v0, 4
		la $a0 result_message
		syscall

		li $v0, 1
		move $a0, $t2
		syscall
   </pre>
   
   
   5.2 Create a program that display your name
   <pre>
.data
	texto: .asciiz "\nCual es mi nombre?: "
	nombre: .asciiz "Mi nombre es: "
	v: .space 20
.text
	main:
		li $v0, 4
		la $a0, texto
		syscall

		li $v0, 8
		la $a0, v
		li $a1, 20
		syscall 

		li $v0, 4
		la $a0, nombre
		syscall

		li $v0, 4
		la $a0, v
		syscall
		
   </pre>

## Thursday activity
  ### 1. Search for real word applications of Javascript
   - Flying Robots
   - Smartwatch Applications
   - Mobile Applications
   - Video Games
   - Web Servers
   - Web Applications
   
  ### 2. Watch [this](https://www.youtube.com/watch?v=LW6vQNE2jgc&t=1962s) video
   - Done
   
  ### 3. Watch [this](https://www.youtube.com/watch?v=KXkQJBASUOg) video
   - Done
  
  ### 4. Follow the github course
   - Done