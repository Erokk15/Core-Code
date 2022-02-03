## Monday activity

### 1. Who likes it?
You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

```
[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
```
Note: For 4 or more names, the number in "and 2 others" simply increases.

#### Solution
```javascript
function likes (names) {
  if (names.length === 0) return 'no one likes this';
  if (names.length === 1) return `${names[0]} likes this`;
  if (names.length === 2) return `${names[0]} and ${names[1]} like this`;
  if (names.length === 3) return `${names[0]}, ${names[1]} and ${names[2]} like this`;
  if (names.length > 3) return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
  }
```

-----
### 2. Bit Counting
Write a function that takes an integer as input, and returns the number of bits that are equal to one in the binary representation of that number. You can guarantee that input is non-negative.

Example: The binary representation of 1234 is 10011010010, so the function should return 5 in this case.

#### Solution
```javascript
var countBits = function(n) {
let l = n.toString(2);
let r = 0;

  for (let i = 0; i < l.length; i++) {
    if(l[i]=='1'){
    r = r + 1;
  }
 }
  return r;
}
```

------
### 3. Decode the Morse code
Your task is to implement a function that would take the morse code as input and return a decoded human-readable string.

For example:

```
decodeMorse('.... . -.--   .--- ..- -.. .')
//should return "HEY JUDE"
```
#### Solution
```javascript
const decodeLetter = letter => {
  return MORSE_CODE[letter];
}

const decodeWord = word => {
  return word.split(' ').map(decodeLetter).join('');
}

const decodeMorse = morseCode => {
  return morseCode.trim().split('   ').map(decodeWord).join(' ');
}
```
------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*