## Wednesday activity

### 1. Array.diff
Your goal in this kata is to implement a difference function, which subtracts one list from another and returns the result.

It should remove all values from list a, which are present in list b keeping their order.
```
array_diff({1, 2}, 2, {1}, 1, *z) == {2} (z == 1)
```
If a value is present in b, all of its occurrences must be removed from the other:
```
array_diff({1, 2, 2, 2, 3}, 5, {2}, 1, *z) == {1, 3} (z == 2)
```

#### Solution
```javascript
function arrayDiff(a, b) {
  return a.filter(e => !b.includes(e));
}
```
-------

### 2. Create Phone Number
Write a function that accepts an array of 10 integers (between 0 and 9), that returns a string of those numbers in the form of a phone number.

Example
```
createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]) // => returns "(123) 456-7890"
```

#### Solution
```javascript
function createPhoneNumber(numbers){
  let format = "(xxx) xxx-xxxx";
  
  for(let i = 0; i < numbers.length; i++) {
    format = format.replace('x', numbers[i]);
  }
  
  return format;
}
```
-------

3. Watch [this](https://www.youtube.com/watch?v=m_MQYyJpIjg)
- Done

-------

4. Watch [this](https://www.youtube.com/watch?v=08CWw_VD45w)
- Done

-------

5. Read [this](https://medium.com/from-the-scratch/oop-everything-you-need-to-know-about-object-oriented-programming-aee3c18e281b)

- Done

-------

6. Read [this](https://naveenkumarkoppala.medium.com/typescript-oops-c327678744b0)
- Done 

-------

7. Read [this](https://rambabupadimi.medium.com/typescript-object-oriented-programming-7a6fd905d90e)

- Done

--------

*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*
