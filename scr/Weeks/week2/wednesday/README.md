## Wednesday activity

### 1. How many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday. [codewars link](https://www.codewars.com/kata/57e92e91b63b6cbac20001e5)
<pre>
function dutyFree(normPrice, discount, hol){ 
  let num;
  let desc; 
  let redondeo; 
  num = hol / normPrice; 
  desc = num / discount; 
  redondeo = Math.floor(desc* 100); 
  return redondeo; 
} 
</pre>

### 2. Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old). [codewars link](https://www.codewars.com/kata/5b853229cfde412a470000d0)
<pre>
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let op;
  op = Math.abs(dadYearsOld - (sonYearsOld * 2));
  return op
</pre>

### 3. Your task is to write a function which checks if a string has valid spacing. The function should return either True or False. [codewars link](https://www.codewars.com/kata/5f77d62851f6bc0033616bd8)
<pre>
function validSpacing(s) {
  let a = s;
  
  if(a.trim() != s){
    return false;
  }
  if(s.search('  ') != -1){
      return false;
  }
  return true;
}
</pre>

### 4. Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string. [codewars link](https://www.codewars.com/kata/57eae65a4321032ce000002d)
<pre>
function fakeBin(x){
     let a = "";
 for (let i = 0; i < x.length; i++) {
    
    if (Number(x[i]) <= 4) {
        a += "0";
    } 
   else if (Number(x[i]) >= 5) {
        a += "1";
    }
  }
return a;
}
</pre>


#### You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)