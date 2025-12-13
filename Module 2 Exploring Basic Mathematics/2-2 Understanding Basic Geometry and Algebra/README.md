# Understanding Basic Geometry and Algebra

Geometry helps us build the "visual" world of the web, while Algebra helps us write the "logic" that powers it.

## 1. Geometry in Web Development

### The Coordinate System (X and Y axis)

The browser window is a 2D plane.

- **X-axis**: Horizontal position. (0 is usually the left).
- **Y-axis**: Vertical position. (0 is usually the top).
- **Usage**: Positioning elements (`position: absolute; top: 10px; left: 20px`), drawing on HTML5 Canvas, and creating graphs.

### Shapes and Box Model

- **Rectangles**: Every HTML element is essentially a rectangular box (The Box Model: Margin, Border, Padding, Content).
- **Angles**: Used in CSS transforms (e.g., `transform: rotate(45deg)`).
- **Radius**: Creating rounded corners (`border-radius`) or circles.

## 2. Algebra in Programming

### Variables

Algebra teaches us to use symbols to represent numbers (e.g., `x + 5 = 10`). In coding, we use **Variables** to store data.

- _Math_: $x = 5$
- _JS_: `let x = 5;`

### Functions as Formulas

A function in code is like an algebraic formula: $f(x) = x^2$.

- **Input**: Arguments passed to the function.
- **Processing**: The math inside.
- **Output**: The return value.

```javascript
// A simple algebraic function in JS
function square(x) {
  return x * x;
}
```

### Logic Operations

Solving inequalities ($x > 10$) is the basis of conditional logic in code (`if (userAge > 18) { ... }`).
