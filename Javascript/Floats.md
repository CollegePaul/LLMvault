### Understanding Floats in JavaScript

In JavaScript, numbers are all stored as floating-point numbers, according to the IEEE 754 standard. This means that JavaScript does not differentiate between integers and floating-point numbers like some other programming languages do (e.g., Java or C++). All numeric values in JavaScript are of type "Number" and are represented using double-precision 64-bit binary format.

#### Key Points:
- **Precision**: Due to the way they are stored, floating-point numbers can sometimes lead to precision issues. For example, operations like `0.1 + 0.2` might not yield exactly `0.3` due to rounding errors.
- **Range**: JavaScript numbers can range from approximately \( -1.8 \times 10^{308} \) to \( 1.8 \times 10^{308} \).
- **Special Values**: There are some special numeric values in JavaScript like `Infinity`, `-Infinity`, and `NaN` (Not-a-Number).

#### Examples:

```javascript
// Basic floating-point arithmetic
let num1 = 0.1 + 0.2;
console.log(num1); // Output: 0.30000000000000004

// Precision issues
let num2 = 0.1 * 0.7;
console.log(num2); // Output: 0.07000000000000001

// Special numeric values
let inf = Infinity;
let negInf = -Infinity;
let notANumber = NaN;

console.log(inf + 1);      // Output: Infinity
console.log(negInf * 2);   // Output: -Infinity
console.log(notANumber * 5);// Output: NaN

// Checking if a value is finite, infinite or NaN
console.log(isFinite(num1));       // Output: true
console.log(Number.isNaN(notANumber));// Output: true
```

#Floats #Javascript