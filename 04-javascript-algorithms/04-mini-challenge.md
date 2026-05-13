# Module 04 — Mini Challenge: JavaScript Algorithms and Common Patterns

---

## Challenge: Data dashboard (no UI needed)

**Goal:** Write a series of functions that process a dataset of employees. No HTML required — work entirely in JavaScript.

---

## The data

```js
const employees = [
  { id: 1,  name: 'Alice',   department: 'engineering', salary: 4500, yearsExp: 3, active: true  },
  { id: 2,  name: 'Bob',     department: 'marketing',   salary: 3200, yearsExp: 1, active: true  },
  { id: 3,  name: 'Charlie', department: 'engineering', salary: 5100, yearsExp: 6, active: true  },
  { id: 4,  name: 'Diana',   department: 'marketing',   salary: 3800, yearsExp: 2, active: false },
  { id: 5,  name: 'Eve',     department: 'engineering', salary: 4800, yearsExp: 4, active: true  },
  { id: 6,  name: 'Frank',   department: 'design',      salary: 4100, yearsExp: 5, active: true  },
  { id: 7,  name: 'Grace',   department: 'design',      salary: 3900, yearsExp: 2, active: false },
  { id: 8,  name: 'Henry',   department: 'marketing',   salary: 4200, yearsExp: 4, active: true  }
];
```

---

## Functions to write

### 1. `getActiveEmployees(employees)`
Returns only employees where `active === true`.

### 2. `getByDepartment(employees, department)`
Returns employees in the given department (active or not).

### 3. `getSortedBySalary(employees, order)`
Returns employees sorted by salary.
- `order = 'asc'` → lowest first
- `order = 'desc'` → highest first

### 4. `getTotalSalary(employees)`
Returns the total salary of all employees passed in.

### 5. `getAverageSalary(employees)`
Returns the average salary (rounded to 2 decimal places).

### 6. `groupByDepartment(employees)`
Returns an object where each key is a department name and the value is an array of employees in that department.

### 7. `getTopEarners(employees, n)`
Returns the top `n` highest-paid employees, sorted by salary descending.

### 8. `getDashboardSummary(employees)`
Returns a summary object:
```js
{
  total: 8,
  active: 6,
  departments: ['engineering', 'marketing', 'design'],
  highestSalary: 5100,
  lowestSalary: 3200,
  averageSalary: 4200.00
}
```

---

## How to approach it

- Write one function at a time
- Test each function before moving to the next
- Use the functions you already wrote inside the later functions (e.g. `getDashboardSummary` can call `getActiveEmployees`)

---

## Checklist

- [ ] All 8 functions written and tested
- [ ] Each function returns the correct result
- [ ] No function modifies the original `employees` array
- [ ] `getDashboardSummary` uses other functions internally

---

**Next step:** Go to `05-validation.md`.
