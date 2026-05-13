# Module 08 — Solutions: Easy Algorithms

Read these only after you have tried each problem yourself.

---

## Problem 1 — Reverse a string

```js
function reverseString(str) {
  return str.split('').reverse().join('');
}

console.log(reverseString('hello'));    // 'olleh'
console.log(reverseString('Angular')); // 'ralugnA'
```

**Approach:** Split the string into individual characters, reverse the array, then join back into a string.

---

## Problem 2 — Check palindrome

```js
function isPalindrome(str) {
  const reversed = str.split('').reverse().join('');
  return str === reversed;
}

console.log(isPalindrome('racecar')); // true
console.log(isPalindrome('hello'));   // false
```

**Approach:** Reverse the string and compare it to the original.

---

## Problem 3 — Find the largest number

```js
function findMax(numbers) {
  let max = numbers[0];
  for (let num of numbers) {
    if (num > max) {
      max = num;
    }
  }
  return max;
}

// Alternative using Math.max:
function findMax(numbers) {
  return Math.max(...numbers);
}

console.log(findMax([3, 7, 1, 9, 4])); // 9
```

**Approach:** Loop through all numbers keeping track of the biggest seen so far.

---

## Problem 4 — Count vowels

```js
function countVowels(str) {
  const vowels = 'aeiouAEIOU';
  let count = 0;
  for (let char of str) {
    if (vowels.includes(char)) {
      count++;
    }
  }
  return count;
}

console.log(countVowels('hello world')); // 3
console.log(countVowels('Angular'));     // 3
```

**Approach:** Loop through each character and check if it is a vowel.

---

## Problem 5 — Remove duplicates

```js
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

// Alternative without Set:
function removeDuplicates(arr) {
  return arr.filter((item, index) => arr.indexOf(item) === index);
}

console.log(removeDuplicates([1, 2, 2, 3, 3, 3, 4])); // [1, 2, 3, 4]
```

**Approach:** A `Set` automatically removes duplicates. Spread it back into an array.

---

## Problem 6 — Sum all numbers

```js
function sumArray(numbers) {
  let total = 0;
  for (let num of numbers) {
    total += num;
  }
  return total;
}

// Alternative using reduce:
function sumArray(numbers) {
  return numbers.reduce((sum, num) => sum + num, 0);
}

console.log(sumArray([1, 2, 3, 4, 5])); // 15
```

**Approach:** Loop and accumulate the total, or use `reduce`.

---

## Problem 7 — Find even numbers

```js
function getEvens(numbers) {
  return numbers.filter(n => n % 2 === 0);
}

console.log(getEvens([1, 2, 3, 4, 5, 6])); // [2, 4, 6]
```

**Approach:** Use `filter` and the modulo operator `%` — if a number divided by 2 has no remainder, it is even.

---

## Problem 8 — Count words

```js
function countWords(str) {
  return str.trim().split(' ').length;
}

console.log(countWords('the quick brown fox')); // 4
console.log(countWords('hello'));               // 1
```

**Approach:** Split the string by spaces — the number of parts is the number of words.

---

## Problem 9 — FizzBuzz

```js
function fizzBuzz(n) {
  const result = [];
  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      result.push('FizzBuzz');
    } else if (i % 3 === 0) {
      result.push('Fizz');
    } else if (i % 5 === 0) {
      result.push('Buzz');
    } else {
      result.push(i);
    }
  }
  return result;
}

console.log(fizzBuzz(15));
```

**Approach:** Check divisibility by 15 first (both 3 and 5), then 3, then 5. Important: check 15 before 3 and 5.

---

## Problem 10 — Count frequency

```js
function countFrequency(arr) {
  const result = {};
  for (let item of arr) {
    if (result[item]) {
      result[item]++;
    } else {
      result[item] = 1;
    }
  }
  return result;
}

console.log(countFrequency(['apple', 'banana', 'apple', 'cherry', 'banana', 'apple']));
// { apple: 3, banana: 2, cherry: 1 }
```

**Approach:** Use an object to count. For each item, if it exists in the object, increase the count. Otherwise set it to 1.

---

## Problem 11 — Capitalize first letter

```js
function capitalizeFirst(str) {
  return str.charAt(0).toUpperCase() + str.slice(1);
}

console.log(capitalizeFirst('hello world')); // 'Hello world'
```

**Approach:** Take the first character, uppercase it, and join it with the rest of the string.

---

## Problem 12 — Find missing number

```js
function findMissing(arr, n) {
  const expectedSum = n * (n + 1) / 2;
  const actualSum = arr.reduce((sum, num) => sum + num, 0);
  return expectedSum - actualSum;
}

console.log(findMissing([1, 2, 4, 5], 5)); // 3
```

**Approach:** The sum of 1 to n is a known formula. Subtract the actual sum of the array. The difference is the missing number.

---

**Next step:** Go to `04-validation.md`.
