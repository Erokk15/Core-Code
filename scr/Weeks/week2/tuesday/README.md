## Tuesday activity

### 0. Watch [this](https://www.youtube.com/watch?v=cEBkvm0-rg0) video 
- Done

### 1. Multiply. [codewars link](https://www.codewars.com/kata/50654ddff44f800200000004)
<pre>
function multiply(a, b){
  let c = a * b;
  return c;
}
</pre>

### 2. You'll be given a string, and have to return the sum of all characters as an int. [codewars link](https://www.codewars.com/kata/572b6b2772a38bc1e700007a)
<pre>
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
</pre>

### 3. Write a function which takes a number and returns the corresponding ASCII char for that value. [codewars link](https://www.codewars.com/kata/55ad04714f0b468e8200001c)
<pre>
function getChar(c){
  let a = String.fromCharCode(c);
  return a;
}
</pre>

### 4. Implement a function that adds two numbers together and returns their sum in binary. [codewars link](https://www.codewars.com/kata/551f37452ff852b7bd000139)
<pre>
function addBinary(a,b) {
  let sum = a + b;
  let bi = sum.toString(2);
  return bi;

}
</pre>

### 5. Create a function, which calculates the final grade of a student depending on two parameters. [codewars link](https://www.codewars.com/kata/5ad0d8356165e63c140014d4) 
<pre>
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10){
    return 100
  }
  else if(exam > 75 && projects >= 5){
    return 90;
  }
  else if(exam > 50 && projects >= 2){
    return 75;
  }
  else{
    return 0;
  }
}
</pre>

#### You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)