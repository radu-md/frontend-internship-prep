# Module 05 — Theory: TypeScript and OOP

## What is TypeScript?

TypeScript is JavaScript with **types**.

In JavaScript, you can put any value in a variable without saying what type it is:

```js
let name = 'Alex';  // JavaScript — no type declared
name = 42;             // works, but probably a mistake
```

In TypeScript, you declare the type. If you try to put the wrong type, TypeScript warns you **before** you run the code:

```ts
let name: string = 'Alex';
name = 42;  // TypeScript error: Type 'number' is not assignable to type 'string'
```

This catches bugs early and makes code easier to understand.

Angular is written in TypeScript, so you need to be comfortable with it.

---

## Basic types

```ts
let name: string = 'Alex';
let age: number = 20;
let isActive: boolean = true;
let score: number[] = [85, 90, 78];  // array of numbers
let nothing: null = null;
```

### Type inference

TypeScript is smart — if you assign a value immediately, it figures out the type:

```ts
let name = 'Alex';  // TypeScript knows this is a string
```

---

## Interfaces

An **interface** describes the shape of an object — what properties it has and what types they are.

```ts
interface User {
  name: string;
  age: number;
  email: string;
  isAdmin: boolean;
}

const user: User = {
  name: 'Alex',
  age: 20,
  email: 'Alex@email.com',
  isAdmin: false
};
```

If you miss a property or use the wrong type, TypeScript warns you.

### Optional properties

Use `?` to mark a property as optional:

```ts
interface Product {
  name: string;
  price: number;
  description?: string;  // optional
}
```

---

## Classes

A **class** is a blueprint for creating objects.

```ts
class User {
  name: string;
  age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  greet(): string {
    return `Hello, I am ${this.name}`;
  }
}

const user = new User('Alex', 20);
console.log(user.greet());  // 'Hello, I am Alex'
```

- `constructor` runs automatically when you create a new object
- `this` refers to the current object
- Methods are functions defined inside the class

### Access modifiers

```ts
class BankAccount {
  public owner: string;    // accessible from anywhere
  private balance: number; // only accessible inside this class

  constructor(owner: string, balance: number) {
    this.owner = owner;
    this.balance = balance;
  }

  getBalance(): number {
    return this.balance;  // OK — inside the class
  }
}

const account = new BankAccount('Alex', 1000);
console.log(account.owner);    // OK
console.log(account.balance);  // TypeScript error — private
console.log(account.getBalance());  // OK — use the public method
```

### Shorthand constructor

TypeScript has a shortcut to declare and assign in one step:

```ts
class User {
  constructor(
    public name: string,
    private age: number
  ) {}
}
```

This is the same as the longer version above.

---

## Inheritance

One class can **extend** another to reuse its properties and methods.

```ts
class Animal {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  speak(): string {
    return `${this.name} makes a sound.`;
  }
}

class Dog extends Animal {
  breed: string;

  constructor(name: string, breed: string) {
    super(name);  // call the parent constructor
    this.breed = breed;
  }

  speak(): string {
    return `${this.name} barks!`;  // overrides the parent method
  }
}

const dog = new Dog('Rex', 'Labrador');
console.log(dog.speak());  // 'Rex barks!'
```

- `extends` sets up inheritance
- `super()` calls the parent class constructor
- You can override methods in the child class

---

## Enums

Enums define a set of named constants:

```ts
enum Status {
  Active = 'active',
  Inactive = 'inactive',
  Pending = 'pending'
}

const userStatus: Status = Status.Active;
```

---

## Summary

| Concept | What it is |
|---|---|
| TypeScript | JavaScript + types |
| Type annotation | Declaring what type a variable holds |
| Interface | Describes the shape of an object |
| Class | Blueprint for creating objects |
| Constructor | Runs when a new object is created |
| `public` | Accessible from anywhere |
| `private` | Accessible only inside the class |
| Inheritance | A class can extend another class |
| `super()` | Calls the parent class constructor |
| Enum | A set of named constants |

**Next step:** Read `02-oop-cheatsheet.md` for a quick OOP reference.
