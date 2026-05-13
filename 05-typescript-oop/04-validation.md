# Module 05 — Validation: TypeScript and OOP

Answer each question in your own words.

---

## Section 1 — TypeScript

**1.** What is the difference between TypeScript and JavaScript?

> Write your answer here.

---

**2.** What does this TypeScript error mean?

```
Type 'number' is not assignable to type 'string'
```

> Write your answer here.

---

**3.** What is an interface? What is it used for?

> Write your answer here.

---

**4.** What is the difference between a `class` and an `interface`?

> Write your answer here.

---

## Section 2 — OOP concepts

**5.** Explain encapsulation in simple words. Give a real-life example.

> Write your answer here.

---

**6.** Explain inheritance in simple words. Give a code example (just the idea, not full code).

> Write your answer here.

---

**7.** What is the difference between `public` and `private` in a class?

> Write your answer here.

---

**8.** What does `super()` do?

> Write your answer here.

---

**9.** What is a constructor? When does it run?

> Write your answer here.

---

## Section 3 — Read the code

**10.** What does this class do? What will `user.greet()` return?

```ts
class User {
  constructor(public name: string, private age: number) {}

  greet(): string {
    return `Hi, I am ${this.name} and I am ${this.age} years old.`;
  }
}

const user = new User('Alex', 20);
console.log(user.greet());
```

> Write your answer here.

---

**11.** What is wrong with this code?

```ts
class BankAccount {
  private balance: number = 0;
}

const account = new BankAccount();
console.log(account.balance);
```

> Write your answer here.

---

## Section 4 — Can you do it?

- [ ] I can add type annotations to variables
- [ ] I can create an interface for an object
- [ ] I can create a class with a constructor, properties, and methods
- [ ] I can use `public` and `private` correctly
- [ ] I can extend a class with `extends` and `super()`
- [ ] I can explain encapsulation, inheritance, and polymorphism simply
- [ ] I can explain the difference between a class and an interface

---

## You are ready for Module 05 when:

All boxes above are checked and you can answer at least 9 of the 11 questions without notes.

**Next step:** Go to `06-angular-basics/theory.md`
