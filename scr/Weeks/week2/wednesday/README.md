## Wednesday activity

### 1. Holiday VIII - Duty Free. 
The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.

#### Solution
```javascript
function dutyFree(normPrice, discount, hol){ 
  let num;
  let desc; 
  let redondeo; 
  num = hol / normPrice; 
  desc = num / discount; 
  redondeo = Math.floor(desc* 100); 
  return redondeo; 
```
----------
### 2. Twice as old.
Your function takes two arguments:

current father's age (years)
current age of his son (years)
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).

#### Solution
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let op;
  op = Math.abs(dadYearsOld - (sonYearsOld * 2));
  return op
}
```
------------
### 3. Valid Spacing.
Your task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either True or False.

For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Below are some examples of what the function should return.
```
'Hello world' = true
' Hello world' = false
'Hello world  ' = false
'Hello  world' = false
'Hello' = true
// Even though there are no spaces, it is still valid because none are needed
'Helloworld' = true 
// true because we are not checking for the validity of words.
'Helloworld ' = false
' ' = false
'' = true
```
Note - there will be no punctuation or digits in the input string, only letters.

#### Solution
```javascript
function validSpacing(s) {
  let a = s;  
  if(a.trim() != s) return false;  
  if(s.search('  ') != -1) return false;
    return true;
}

```
----------
### 4. Fake Binary.
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

#### Solution
```javascript
function fakeBin(x){
  let a = "";
  for (let i = 0; i < x.length; i++) {
    if (Number(x[i]) <= 4) a += "0"; 
    if (Number(x[i]) >= 5) a += "1";
  }
return a;
}
```

-----
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*