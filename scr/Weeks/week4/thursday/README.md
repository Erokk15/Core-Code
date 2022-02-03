## Thursday activity

### 1. Fold an array
In this kata you have to write a method that folds a given array of integers by the middle x-times.

An example says more than thousand words:

```
Fold 1-times:
[1,2,3,4,5] -> [6,6,3]

A little visualization (NOT for the algorithm but for the idea of folding):

 Step 1         Step 2        Step 3       Step 4       Step5
                     5/           5|         5\          
                    4/            4|          4\      
1 2 3 4 5      1 2 3/         1 2 3|       1 2 3\       6 6 3
----*----      ----*          ----*        ----*        ----*


Fold 2-times:
[1,2,3,4,5] -> [9,6]

```

#### Solution
```javascript
function foldArray(array, runs) {
  let arrayToFold = Array.from(array);
    while (runs > 0) {
      let resultArray = [];
      while (arrayToFold.length > 1) {
        let firstElement = arrayToFold.shift();
        let lastElement = arrayToFold.pop();
        resultArray.push(firstElement + lastElement);
      }
      arrayToFold = [...resultArray, ...arrayToFold];
      runs--;
    }
    return arrayToFold;
}
```
--------
### 2. Encrypt this!
You want to create secret messages which can be deciphered by the Decipher this! kata. Here are the conditions:

1. Your message is a string containing space separated words.
2. You need to encrypt each word in the message using the following rules:
- The first letter must be converted to its ASCII code.
- The second letter must be switched with the last letter
3. Keepin' it simple: There are no special characters in the input.

Examples:

```
encryptThis("Hello") === "72olle"
encryptThis("good") === "103doo"
encryptThis("hello world") === "104olle 119drlo"
```

#### Solution
```javascript
var encryptThis = function(text) {
 return text.split(' ').map( e => {
  if (e.length===1) return e.charCodeAt(0)
  if (e.length===2) return `${e[0].charCodeAt(0)}${e[1]}`
  if (e.length===3) return `${e[0].charCodeAt(0)}${e.slice(-1)}${e[1]}`
  if (e.length > 3) return `${e[0].charCodeAt(0)}${e.slice(-1)}${e.slice(2,-1)}${e[1]}`  
  }).join(' ');
}
```

### 3. Format a string of names like 'Bart, Lisa & Maggie'. 
Given: an array containing hashes of names

Return: a string formatted as a list of names separated by commas except for the last two names, which should be separated by an ampersand.

Example:


```
list([ {name: 'Bart'}, {name: 'Lisa'}, {name: 'Maggie'} ])
// returns 'Bart, Lisa & Maggie'

list([ {name: 'Bart'}, {name: 'Lisa'} ])
// returns 'Bart & Lisa'

list([ {name: 'Bart'} ])
// returns 'Bart'

list([])
// returns ''
```

#### Solution
```javascript
function list(names){
  return names.reduce(function(prev, current, index){
    if (index === 0) return current.name;
    if (index === names.length - 1) return ${prev} & ${current.name}
    return ${prev}, ${current.name};
  }, '');
 }
```


-------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*
