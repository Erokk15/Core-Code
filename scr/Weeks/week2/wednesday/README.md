## Wednesday activity

### 1. Holiday VIII - Duty Free. [codewars link](https://www.codewars.com/kata/57e92e91b63b6cbac20001e5)
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

### 2. Twice as old. [codewars link](https://www.codewars.com/kata/5b853229cfde412a470000d0)
<pre>
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let op;
  op = Math.abs(dadYearsOld - (sonYearsOld * 2));
  return op
}
</pre>

### 3. Valid Spacing [codewars link](https://www.codewars.com/kata/5f77d62851f6bc0033616bd8)
<pre>
function validSpacing(s) {
  let a = s;  
  if(a.trim() != s) return false;  
  if(s.search('  ') != -1) return false;
    return true;
}

</pre>

### 4. Fake Binary. [codewars link](https://www.codewars.com/kata/57eae65a4321032ce000002d)
<pre>
function fakeBin(x){
  let a = "";
  for (let i = 0; i < x.length; i++) {
    if (Number(x[i]) <= 4) a += "0"; 
    if (Number(x[i]) >= 5) a += "1";
  }
return a;
}
</pre>


#### You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)