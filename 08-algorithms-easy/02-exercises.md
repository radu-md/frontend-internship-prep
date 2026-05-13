# Module 08 — Exercises: Easy Algorithms

Try to solve each problem yourself before looking at `03-solutions.md`.

Write each solution as a function and test it with the example input.

---

## Problem 1 — Reverse a string

Write a function `reverseString(str)` that returns the string reversed.

```
Input:  'hello'
Output: 'olleh'

Input:  'Angular'
Output: 'ralugnA'
```

---

## Problem 2 — Check palindrome

Write a function `isPalindrome(str)` that returns `true` if the string reads the same forwards and backwards.

```
Input:  'racecar'  → true
Input:  'hello'    → false
Input:  'madam'    → true
```

Hint: compare the string to its reverse.

---

## Problem 3 — Find the largest number

Write a function `findMax(numbers)` that returns the largest number in an array.

```
Input:  [3, 7, 1, 9, 4]
Output: 9

Input:  [100, 5, 42]
Output: 100
```

---

## Problem 4 — Count vowels

Write a function `countVowels(str)` that counts the number of vowels (a, e, i, o, u) in a string. Case-insensitive.

```
Input:  'hello world'
Output: 3

Input:  'Angular'
Output: 3
```

---

## Problem 5 — Remove duplicates

Write a function `removeDuplicates(arr)` that returns a new array with duplicates removed.

```
Input:  [1, 2, 2, 3, 3, 3, 4]
Output: [1, 2, 3, 4]

Input:  ['a', 'b', 'a', 'c']
Output: ['a', 'b', 'c']
```

---

## Problem 6 — Sum all numbers

Write a function `sumArray(numbers)` that returns the sum of all numbers in an array.

```
Input:  [1, 2, 3, 4, 5]
Output: 15

Input:  [10, 20, 30]
Output: 60
```

---

## Problem 7 — Find even numbers

Write a function `getEvens(numbers)` that returns an array containing only the even numbers.

```
Input:  [1, 2, 3, 4, 5, 6]
Output: [2, 4, 6]
```

---

## Problem 8 — Count words

Write a function `countWords(str)` that counts the number of words in a sentence.

```
Input:  'the quick brown fox'
Output: 4

Input:  'hello'
Output: 1
```

Hint: use `.split(' ')`.

---

## Problem 9 — FizzBuzz

Write a function `fizzBuzz(n)` that returns an array of numbers from 1 to n, but:
- Replace multiples of 3 with `'Fizz'`
- Replace multiples of 5 with `'Buzz'`
- Replace multiples of both with `'FizzBuzz'`

```
Input:  15
Output: [1, 2, 'Fizz', 4, 'Buzz', 'Fizz', 7, 8, 'Fizz', 'Buzz', 11, 'Fizz', 13, 14, 'FizzBuzz']
```

---

## Problem 10 — Count frequency

Write a function `countFrequency(arr)` that counts how many times each item appears.

```
Input:  ['apple', 'banana', 'apple', 'cherry', 'banana', 'apple']
Output: { apple: 3, banana: 2, cherry: 1 }
```

---

## Problem 11 — Capitalize first letter

Write a function `capitalizeFirst(str)` that returns the string with the first letter capitalized.

```
Input:  'hello world'
Output: 'Hello world'
```

---

## Problem 12 — Find missing number

Given an array of numbers from 1 to n with one number missing, write a function `findMissing(arr, n)` that returns the missing number.

```
Input:  [1, 2, 4, 5], n = 5
Output: 3
```

Hint: The sum of 1 to n is `n * (n + 1) / 2`. Subtract the sum of the array.

---

**When done:** Check your answers in `03-solutions.md`, then go to `04-validation.md`.
