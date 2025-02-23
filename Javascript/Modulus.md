### Modulus in Javascript

The modulus operator (`%`) in JavaScript is used to find the remainder after dividing one number by another. It works similarly to division but instead of returning the quotient, it returns the leftover part that does not fit into the division.

For example, `5 % 2` would result in `1` because when you divide 5 by 2, the quotient is 2 (since 2 fits into 5 two times) and there is a remainder of 1. The modulus operator is particularly useful for checking if a number is even or odd, or for cycling through a fixed set of values.

Here are a few examples to illustrate how the modulus operator works in JavaScript:

```javascript
console.log(5 % 2); // Output: 1
console.log(8 % 4); // Output: 0
console.log(7 % 3); // Output: 1
console.log(9 % 5); // Output: 4
```

In the first example, `5 % 2` returns `1` because 2 goes into 5 two times (totaling 4) and there's a remainder of 1. In the second example, `8 % 4` returns `0` because 4 divides evenly into 8 with no remainder.

### Real-world Application Example

A common use case for the modulus operator is to determine if a number is even or odd:

```javascript
function isEven(number) {
    return number % 2 === 0;
}

console.log(isEven(4)); // Output: true
console.log(isEven(7)); // Output: false
```

In this example, the `isEven` function checks if a number is divisible by 2 with no remainder. If it is, the function returns `true`, indicating that the number is even; otherwise, it returns `false`.

#Modulus #Javascript