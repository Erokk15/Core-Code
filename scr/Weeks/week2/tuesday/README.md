## Tuesday activity

### 0. Watch [this](https://www.youtube.com/watch?v=cEBkvm0-rg0) video 
- Done
---------
### 1. Multiply. 
```javascript
function multiply(a, b) {
  let c = a * b;
  return c;
}
```
--------
### 2. ASCII Total.
You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:

uniTotal("a") == 97 uniTotal("aaa") == 291

#### Solution
```javascript
function uniTotal (string) {
  let l = string.length;
  let sum = 0; 
  let a = 0;
  
    for(let i = 0; i < l; i++){
     a = string.charCodeAt(i);
     sum = sum + a; 
    }
  return sum;
}
```
-----
### 3. Get character from ASCII Value.
Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value.

Example:
```
get_char(65)
```
should return:
```
'A'
```

#### Solutiom
```javascript
function getChar(c) {
  let a = String.fromCharCode(c);
  return a;
}
```
----------

### 4. Binary Addition. 
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

Examples:(Input1, Input2 --> Output (explanation)))
```

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)
```
#### Solution
```javascript
function addBinary(a,b) {
  let sum = a + b;
  let bi = sum.toString(2);
  return bi;

}
```

### 5. Student's Final Grade.
Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);

This function should return a number (final grade). There are four types of final grades:

100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
0, in other cases
Examples(Inputs-->Output):

```
100, 12 --> 100
99, 0 --> 100
10, 15 --> 100

85, 5 --> 90

55, 3 --> 75

55, 0 --> 0
20, 2 --> 0
```
#### Solution
```javascript
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10) return 100;
  if(exam > 75 && projects >= 5) return 90;
  if(exam > 50 && projects >= 2) return 75;
  return 0;
}
```
------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*
