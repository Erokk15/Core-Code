## Wednesday activity

### 1. Valid Parentheses
Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid. The function should return true if the string is valid, and false if it's invalid.

```

Examples:
"()"              =>  true
")(()))"          =>  false
"("               =>  false
"(())((()())())"  =>  true
```

#### Solution
```javascript
function validParentheses(parens){
  let n = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] == '(') n++;
    if (parens[i] == ')') n--;
    if (n < 0) return false;
  }
  
  return n == 0;
}
```
----------
### 2. Convert string to camel case
Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized only if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case).

#### Solution
```javascript
function toCamelCase(str){
 return str.split(/-|_/g).map((w, i) => (
   i > 0 ? 
   w.charAt(0).toUpperCase() 
   : w.charAt(0)) + w.slice(1)).join('');
}
```
------------
### 3. Unique In Order
Implement the function unique_in_order which takes as argument a sequence and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.

For example:

```
uniqueInOrder('AAAABBBCCDAABBB') == ['A', 'B', 'C', 'D', 'A', 'B']
uniqueInOrder('ABBCcAD')         == ['A', 'B', 'C', 'c', 'A', 'D']
uniqueInOrder([1,2,2,3,3])       == [1,2,3]
```

#### Solution
```javascript
var uniqueInOrder=function(iterable){
  let result = [];
  let w = iterable;
  
  for(let i = 0, length = w.length; i < length; i++){
    if(w[i] !== w[i + 1]) result.push(w[i]);
  }
  
  return result
}
```

-----
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*