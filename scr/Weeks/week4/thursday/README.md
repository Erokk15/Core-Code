## Thursday activity

### 1. Detect Pangram

A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.

#### Solution
```typescript
export const isPangram = (phrase: string): boolean => {
  let s = phrase.toLowerCase();
  let letters = "abcdefghijklmnopqrstuvwxyz";
    for (let i = 0; i < 26; i++){
        if (s.indexOf(letters.charAt(i)) == -1)
    return false;
    }
    return true;
}
```
-------

### 2. Find the missing letter
Write a method that takes an array of consecutive (increasing) letters as input and that returns the missing letter in the array.

You will always get an valid array. And it will be always exactly one letter be missing. The length of the array will always be at least 2.
The array will always contain letters in only one case.

Example:
```
['a','b','c','d','f'] -> 'e' ['O','Q','R','S'] -> 'P'

["a","b","c","d","f"] -> "e"
["O","Q","R","S"] -> "P"
```
#### Solution
```typescript
export function findMissingLetter(array:string[]):string {
   let newArr = array.map(function(letter) {
        return letter.toLowerCase()
    })
    let alphabet = 'abcdefghijklmnopqrstuvwxyz';
    let letter = newArr[0];
    let indexLetter = alphabet.indexOf(letter);
    alphabet = alphabet.slice(indexLetter, alphabet.length);
    const missingLetter = alphabet.split('').filter(letter => !newArr.includes(letter))[0];
    return array[0] === letter.toUpperCase() ? missingLetter.toUpperCase() : missingLetter.toLowerCase();
}
```
-------

### 3. Find the unique number
There is an array with some numbers. All numbers are equal except for one. Try to find it!

```
findUniq([ 1, 1, 1, 2, 1, 1 ]) === 2
findUniq([ 0, 0, 0.55, 0, 0 ]) === 0.55
```
#### Solution
```typescript
export function findUniq(arr: number[]): number {
  return arr.filter((n) => arr.indexOf(n) === arr.lastIndexOf(n))[0];
}
```
-------

### 4. Reverse or rotate?
The input is a string str of digits. Cut the string into chunks (a chunk here is a substring of the initial string) of size sz (ignore the last chunk if its size is less than sz).

If a chunk represents an integer such as the sum of the cubes of its digits is divisible by 2, reverse that chunk; otherwise rotate it to the left by one position. Put together these modified chunks and return the result as a string.

If

- sz is <= 0 or if str is empty return ""
- sz is greater (>) than the length of str it is impossible to take a chunk of size sz hence return "".

Examples:
```
revrot("123456987654", 6) --> "234561876549"
revrot("123456987653", 6) --> "234561356789"
revrot("66443875", 4) --> "44668753"
revrot("66443875", 8) --> "64438756"
revrot("664438769", 8) --> "67834466"
revrot("123456779", 8) --> "23456771"
revrot("", 8) --> ""
revrot("123456779", 0) --> "" 
revrot("563000655734469485", 4) --> "0365065073456944"
```
Example of a string rotated to the left by one position:
```
s = "123456" gives "234561".
```
#### Solution
```typescript

```
-------

### 5. What's Your Poison?
You receive an array of integers (0 to 9), each of them is the number of a rat which died after tasting the wine bottles. Return the number of the bottle (1..1000) which is poisoned.

#### Solution
```javascript
function find(rats) {
  return rats.reduce((a,b) => a + Math.pow(2, b), 0);
}
```
-------
*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*