# Even and Odd Numbers, Leap Years

This section covers discrete logic. In programming, these concepts are mastered using the **Modulo Operator (`%`)**. The modulo operator gives you the **remainder** of a division.

## 1. Even and Odd Numbers

Computers don't "know" if a number is even or odd; we have to test it.

### The Logic (Modulo)

- If a number is divided by 2 and the remainder is 0, it is **Even**.
- If the remainder is 1, it is **Odd**.

```javascript
if (number % 2 === 0) {
  // It's Even
} else {
  // It's Odd
}
```

### Visual Application: Zebra Striping

Web developers use this extensively for "Zebra Striping" tables to improve readability.

- **CSS**:
  ```css
  tr:nth-child(even) {
    background-color: #f2f2f2;
  }
  tr:nth-child(odd) {
    background-color: #ffffff;
  }
  ```
  This automatically colors every other row differently.

## 2. Leap Years

Date calculation is notoriously difficult in programming. A leap year (366 days) occurs to keep our calendar in sync with the Earth's orbit.

### The Algorithm

Finding a leap year is a classic logic interview question. It's not just "every 4 years".

1.  Divisible by 4? (Yes = maybe leap)
2.  Divisible by 100? (Yes = NOT leap, unless...)
3.  Divisible by 400? (Yes = LEAP)

### The Code Logic

```javascript
function isLeapYear(year) {
  return (year % 4 === 0 && year % 100 !== 0) || year % 400 === 0;
}
```

- **2000**: Divisible by 400 → **Leap Year**.
- **1900**: Divisible by 100 but not 400 → **Not a Leap Year**.
- **2024**: Divisible by 4 → **Leap Year**.

_Knowing these edge cases prevents bugs in calendar apps and scheduling software._
