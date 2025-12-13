# Numbers and Unitary Methods

## 1. Numbers in Programming

Unlike standard math where numbers are abstract, in computers, numbers have types and limits.

### Integers (Whole Numbers)

- Used for counting (loops, array variation indexes).
- Example: `0`, `1`, `42`, `-10`.

### Floating Point (Decimals)

- Used for precision (currency, physics, opacity).
- **The JavaScript "Gotcha"**: Computers store decimals in binary. Sometimes math isn't perfect.
  - _Real Life_: $0.1 + 0.2 = 0.3$
  - _JavaScript_: `0.1 + 0.2 === 0.30000000000000004`
  - _Lesson_: Always round your numbers when doing precise calculations like money.

## 2. Unitary Method

The unitary method is the process of finding the value of a single unit, and then calculating the value of more units.

- _Basic Math_: If 5 server requests take 500ms, how long does 1 take? (500 / 5 = 100ms).

### Application: Scalability Estimates

Developers use this logic to estimate system performance (Big O).

- "If one image is 2MB, and I have 50 users uploading images, I need 100MB of storage."
- "If a loop takes 1ms for 10 items, it might take 100ms for 1000 items (Linear scaling)."
- This thinking helps prevent server crashes when traffic spikes.
