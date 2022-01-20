## Tuesday activity

### 0. Watch [this](https://www.youtube.com/watch?v=cEBkvm0-rg0) video 
- Done

### 1. Multiply. [codewars link](https://www.codewars.com/kata/50654ddff44f800200000004)
```javascript
function multiply(a, b) {
  let c = a * b;
  return c;
}
```

### 2. ASCII Total. [codewars link](https://www.codewars.com/kata/572b6b2772a38bc1e700007a)
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

### 3. Get character from ASCII Value. [codewars link](https://www.codewars.com/kata/55ad04714f0b468e8200001c)
```javascript
function getChar(c) {
  let a = String.fromCharCode(c);
  return a;
}
```

### 4. Binary Addition. [codewars link](https://www.codewars.com/kata/551f37452ff852b7bd000139)
```javascript
function addBinary(a,b) {
  let sum = a + b;
  let bi = sum.toString(2);
  return bi;

}
```

### 5. Student's Final Grade. [codewars link](https://www.codewars.com/kata/5ad0d8356165e63c140014d4) 
```javascript
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10) return 100;
  if(exam > 75 && projects >= 5) return 90;
  if(exam > 50 && projects >= 2) return 75;
  return 0;
}
```

#### You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)
