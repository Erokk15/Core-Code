## Tuesday activity

---------
### 1. Your order, please
```javascript
function order(words) {
  let result = [];
  let w = words.split(' ');
  
  for (let i = 1; i <= w.length; i++) {
    result.push(w.find((w) => w.includes(i)));
  }

  return result.join(' ');
}
```
--------
### 2. Counting Duplicates
Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

Example
"abcde" -> 0 # no characters repeats more than once
"aabbcde" -> 2 # 'a' and 'b'
"aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
"indivisibility" -> 1 # 'i' occurs six times
"Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
"aA11" -> 2 # 'a' and '1'
"ABBA" -> 2 # 'A' and 'B' each occur twice

#### Solution
```javascript
function duplicateCount (who) {
  let lower = who.toLowerCase();
  let Arr = Array.from(String(lower));
  let obj = [];
  let sum = 0;
  
  for (let i = 0; i<Arr.length;i++) {
    let change = Arr[i];
    if(obj[change] >=1) obj[change] = obj[change] + 1;
    else obj[change] = 1;
    
    if (obj[change] === 2 ) sum = sum + 1;
  }
  return(sum);
  }
}
```
-----
### 3. Simple Pig Latin
Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

Examples:

```

pigIt('Pig latin is cool'); // igPay atinlay siay oolcay
pigIt('Hello world !');     // elloHay orldway !
```

#### Solution
```javascript
function pigIt(str) {
  let arr = str.split(' ')
  return arr
    .map((word) => {
      return word.match(/[A-z]/i)
        ? `${word.substr(1)}${word.substr(0, 1)}ay`
        : word
    })
    .join(' ')
}

```
----------


------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*
