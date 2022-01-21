## Thursday activity

### 1. Exclamation marks series #2. 
Remove all exclamation marks from the end of sentence.

Examples:
```
remove("Hi!") === "Hi"
remove("Hi!!!") === "Hi"
remove("!Hi") === "!Hi"
remove("!Hi!") === "!Hi"
remove("Hi! Hi!") === "Hi! Hi"
remove("Hi") === "Hi"
```

#### Solution
```javascript
function remove (string) {  
  let s = string;
  while (s && s.slice(-1) == '!') s = s.slice(0,-1);
  return s;
}
```
--------
### 2. Vowel remover. 
Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples:
```
"hello"     -->  "hll"
"codewars"  -->  "cdwrs"
"goodbye"   -->  "gdby"
"HELLO"     -->  "HELLO"
```

#### Solution
```javascript
function shortcut (string) {
  let s = string;
  let al = [ 'a', 'e', 'i', 'o', 'u'];
  let result = "";
    
  for(let i = 0; i < s.length; i++) {
    if (!al.includes(s[i])) result += s[i];
  }
  return result;
}
```

### 3. Rock Paper Scissors! 
Let's play! You have to return which player won! In case of a draw return Draw!.

Examples:
```
rps('scissors','paper') // Player 1 won!
rps('scissors','rock') // Player 2 won!
rps('paper','paper') // Draw!
```

#### Solution
```javascript
const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!';
  if (p1 === 'rock' && p2 === 'scissors') return 'Player 1 won!';
  if (p1 === 'paper' && p2 === 'rock') return 'Player 1 won!';
  if (p1 === 'scissors' && p2 === 'paper') return 'Player 1 won!';
  return 'Player 2 won!';
}
```

### 4. Persistent Bugger.
Write a function that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

For example (Input --> Output):
```
39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit)
999 --> 4 (because 9*9*9 = 729, 7*2*9 = 126, 1*2*6 = 12, and finally 1*2 = 2)
4 --> 0 (because 4 is already a one-digit number)
```

#### Solution
```javascript
function persistence(num) {
  let s = num.toString();
  let c = 0;
  if (s.length === 1) return 0;
  
  while(s.length > 1) {
    let r = 1
    
    for(let i = 0; i < s.length; i++) {
      r = r * s[i];
    }
    
    s = r.toString().split('');
    c = c + 1;
  }
  return c;
}
```

------------
### 5. Complete your 1st Core Challenge.
- [Mission Statement](challenge)


-------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*
