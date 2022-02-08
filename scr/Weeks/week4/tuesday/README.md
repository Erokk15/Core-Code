## Tuesday activity

### 1. [This](https://www.typescriptlang.org/docs/handbook/intro.html) link is nice to have and read
- Done

---------
### 2. Typescript object type
Given the data, define the interface "User" and use it accordingly.

#### Solution
```typescript
export type User = {
  name: string;
  age: number;
  occupation: string;
};

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```
--------

### 3. Read [this](https://blog.logrocket.com/types-vs-interfaces-in-typescript/)
- Done

----------

### 4. Typescript union types
Type "Person" is missing, please define it and use it in persons array and logPerson function in order to fix all the TS errors.

#### Solution
```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);

```
-------

### 5. Typescript in operator
Fix type errors in logPerson function.

logPerson function should accept both User and Admin and should output relevant information according to the input: occupation for User and role for Admin.

#### Solution
```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(person: Person) {
    let additionalInformation: string;
    if ('role' in person) {
        additionalInformation = person.role;
    } else {
        additionalInformation = person.occupation;
    }
    console.log(` - ${person.name}, 
    ${person.age}, 
    ${additionalInformation}`);
}

persons.forEach(logPerson);
```
-------

### 6. Find the odd int
Given an array of integers, find the one that appears an odd number of times.

There will always be only one integer that appears an odd number of times.

Examples
```
[7] should return 7, because it occurs 1 time (which is odd).
[0] should return 0, because it occurs 1 time (which is odd).
[1,1,2] should return 2, because it occurs 1 time (which is odd).
[0,1,0,1,0] should return 0, because it occurs 3 times (which is odd).
[1,2,2,3,3,3,4,3,3,3,2,2,1] should return 4, because it appears 1 time (which is odd).
```

#### Solution
```typescript
export const findOdd = (xs: number[]): number => {
  return xs.find(a => xs.filter(b => b === a).length % 2 === 1) || 0;
}
```
-------

### 7. Stop gninnipS My sdroW!
Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed. Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.

Examples: 
```
spinWords( "Hey fellow warriors" ) => returns "Hey wollef sroirraw"
spinWords( "This is a test") => returns "This is a test" 
spinWords( "This is another test" )=> returns "This is rehtona test"
```
#### Solution
```typescript
export function spinWords(words: string): string {
  return words.split(' ').map(function (word) {
  return (word.length > 4) ? word.split('').reverse().join('') : word;
  }).join(' ');
}
```
-------

*You can also check the solutions on my [codewars profile](https://www.codewars.com/users/Erokk15/completed_solutions)*

