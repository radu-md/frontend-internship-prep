# Module 05 — OOP Cheat Sheet

A quick reference for Object-Oriented Programming concepts.
These definitions are at beginner level — just enough for internship interviews.

---

## The 4 pillars of OOP

### 1. Encapsulation

**What it means:** Keep the data (properties) and the behavior (methods) of an object together inside a class. Control what is accessible from outside.

**Why it matters:** Prevents outside code from accidentally breaking internal data.

**Simple example:**
```ts
class BankAccount {
  private balance: number = 0;

  deposit(amount: number): void {
    this.balance += amount;
  }

  getBalance(): number {
    return this.balance;
  }
}

const account = new BankAccount();
account.deposit(100);
console.log(account.getBalance());  // 100
// account.balance = -9999;  // not allowed — private
```

**In an interview, say:** "Encapsulation means hiding internal data and only allowing access through defined methods."

---

### 2. Inheritance

**What it means:** A class can inherit properties and methods from another class. The child class gets everything from the parent and can add more.

**Why it matters:** Avoids repeating code.

**Simple example:**
```ts
class Animal {
  name: string;
  constructor(name: string) { this.name = name; }
  speak(): string { return `${this.name} makes a sound.`; }
}

class Dog extends Animal {
  speak(): string { return `${this.name} barks!`; }
}

const dog = new Dog('Rex');
console.log(dog.speak());  // 'Rex barks!'
```

**In an interview, say:** "Inheritance allows one class to reuse the properties and methods of another class."

---

### 3. Polymorphism

**What it means:** The same method name can behave differently in different classes.

**Why it matters:** Lets you write flexible code that works with different types of objects.

**Simple example:**
```ts
class Shape {
  area(): number { return 0; }
}

class Circle extends Shape {
  radius: number;
  constructor(radius: number) { super(); this.radius = radius; }
  area(): number { return Math.PI * this.radius * this.radius; }
}

class Rectangle extends Shape {
  width: number;
  height: number;
  constructor(w: number, h: number) { super(); this.width = w; this.height = h; }
  area(): number { return this.width * this.height; }
}
```

**In an interview, say:** "Polymorphism means the same method name works differently depending on which class it is called on."

---

### 4. Abstraction

**What it means:** Hide the complex details and only show what is necessary.

**Why it matters:** Makes code easier to use — you don't need to understand everything inside to use it.

**Simple example:**
Imagine a `Car` class. You call `car.start()` — you don't need to know about the engine, fuel injection, or spark plugs. Those details are hidden.

```ts
class Car {
  private engineRunning: boolean = false;

  start(): void {
    this.engineRunning = true;
    console.log('Car started');
  }

  stop(): void {
    this.engineRunning = false;
    console.log('Car stopped');
  }
}
```

**In an interview, say:** "Abstraction means hiding the internal complexity and only exposing what the user needs."

---

## Key OOP terms

| Term | Simple definition |
|---|---|
| **Class** | A blueprint for creating objects |
| **Object** | An instance created from a class |
| **Property** | A variable inside a class (stores data) |
| **Method** | A function inside a class (defines behavior) |
| **Constructor** | A special method that runs when an object is created |
| **`this`** | Refers to the current object |
| **`new`** | Keyword to create an object from a class |
| **`extends`** | Keyword to inherit from another class |
| **`super()`** | Calls the parent class constructor |
| **`public`** | Accessible from anywhere |
| **`private`** | Accessible only inside the class |
| **Interface** | Describes the expected shape of an object (TypeScript) |

---

## Class vs Object — quick summary

```ts
// Class — the blueprint (defined once)
class Dog {
  name: string;
  constructor(name: string) { this.name = name; }
  bark(): void { console.log('Woof!'); }
}

// Objects — instances created from the blueprint (as many as you want)
const dog1 = new Dog('Rex');
const dog2 = new Dog('Buddy');

dog1.bark();  // Woof!
dog2.bark();  // Woof!
```

---

## Interface vs Class

| | Interface | Class |
|---|---|---|
| Creates objects? | No | Yes (with `new`) |
| Has logic/methods? | No (only signatures) | Yes |
| Used for | Describing data shape | Defining behavior + data |
| TypeScript only? | Yes | No (JS also has classes) |

---

**Next step:** Go to `03-exercises.md`.
