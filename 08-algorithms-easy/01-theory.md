# Module 08 — Theory: Easy Algorithms

## What are algorithms?

An algorithm is a set of steps to solve a problem.

In interviews, you may be asked to write a small function that solves a simple problem — like reversing a string or finding the largest number in a list.

The goal is **not** to know advanced algorithms. The goal is to:
- read a problem and understand it
- break it into small steps
- write a working solution in JavaScript
- explain your thinking clearly

---

## How to approach any coding problem

Use this process every time:

1. **Read the problem carefully**
   - What is the input?
   - What is the expected output?

2. **Write an example by hand**
   - Input: `[3, 1, 7, 2]`
   - Expected output: `7`

3. **Think of the steps**
   - "I need to go through all numbers and find the biggest one"

4. **Write the code step by step**
   - Start simple, improve later

5. **Test with your example**
   - Does your function return `7`?

6. **Test edge cases**
   - What if the array is empty?
   - What if all numbers are the same?

---

## Common patterns you will use

### Loop through an array

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
```

### Build a new array

```js
function getEvens(numbers) {
  const result = [];
  for (let num of numbers) {
    if (num % 2 === 0) {
      result.push(num);
    }
  }
  return result;
  // or shorter: return numbers.filter(n => n % 2 === 0);
}
```

### Work with a string

```js
// Split into characters, reverse, join back
function reverseString(str) {
  return str.split('').reverse().join('');
}
```

### Count things

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
```

---

## Useful JavaScript built-ins for algorithms

| Method | What it does | Example |
|---|---|---|
| `.split('')` | Splits string into characters | `'hello'.split('')` → `['h','e','l','l','o']` |
| `.join('')` | Joins array into string | `['a','b'].join('')` → `'ab'` |
| `.reverse()` | Reverses an array | `[1,2,3].reverse()` → `[3,2,1]` |
| `.includes()` | Checks if value exists | `[1,2].includes(2)` → `true` |
| `.indexOf()` | Position of a value (-1 if not found) | `[1,2,3].indexOf(2)` → `1` |
| `.filter()` | Keep items matching a condition | `[1,2,3].filter(n => n > 1)` → `[2,3]` |
| `.map()` | Transform each item | `[1,2].map(n => n*2)` → `[2,4]` |
| `Math.max(...arr)` | Largest number | `Math.max(1,3,2)` → `3` |
| `Set` | Collection with no duplicates | `[...new Set([1,1,2])]` → `[1,2]` |

---

## In the interview

When solving an algorithm problem aloud:
- Say what you are doing before you type it
- "I will loop through the string character by character..."
- It is OK to start with a simple solution and improve it
- It is OK to say "Let me think about that for a second"
- If stuck, think about what tools you know: loops, filter, split, etc.

---

**Next step:** Go to `02-exercises.md` and solve all problems.
