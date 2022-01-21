## Thursday activity

### 1. Remove all exclamation marks from the end of sentence. [codewars link](https://www.codewars.com/kata/57faece99610ced690000165)
```javascript
function remove (string) {  
  let s = string;
  while (s && s.slice(-1) == '!') s = s.slice(0,-1);
  return s;
}
```
</pre>

### 2. Vowel remover. [codewars link](https://www.codewars.com/kata/5547929140907378f9000039)
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

### 3. Rock Paper Scissors! [codewars link](https://www.codewars.com/kata/5672a98bdbdd995fad00000f)
```javascript
const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!';
  if (p1 === 'rock' && p2 === 'scissors') return 'Player 1 won!';
  if (p1 === 'paper' && p2 === 'rock') return 'Player 1 won!';
  if (p1 === 'scissors' && p2 === 'paper') return 'Player 1 won!';
  return 'Player 2 won!';
}
```

### 4. Persistent Bugger. [codewars link](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec)
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
### 5. Complete your 1st Core Challenge. s
- [Mission Statement](challenge)

#### You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)
