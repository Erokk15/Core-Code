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
