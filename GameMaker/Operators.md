### Operators in GameMaker

In GameMaker Studio 2 (GMS2), operators are symbols used to perform operations on variables and values, enabling the execution of arithmetic, comparison, logical, and assignment tasks. Here's an overview of some key types:

#### Arithmetic Operators:
- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division
- `%`: Modulus (remainder after division)

**Example in GML:**
```gml
var a = 10;
var b = 5;

// Addition
var sum = a + b; // sum is 15

// Subtraction
var difference = a - b; // difference is 5

// Multiplication
var product = a * b; // product is 50

// Division
var quotient = a / b; // quotient is 2

// Modulus
var remainder = a % b; // remainder is 0
```

#### Comparison Operators:
- `==`: Equal to
- `!=` or `<>`: Not equal to
- `<`: Less than
- `>`: Greater than
- `<=`: Less than or equal to
- `>=`: Greater than or equal to

**Example in GML:**
```gml
var x = 10;
var y = 5;

// Equal to
if (x == 10) {
    show_debug_message("x is equal to 10");
}

// Not equal to
if (y != 6) {
    show_debug_message("y is not equal to 6");
}

// Less than
if (y < x) {
    show_debug_message("y is less than x");
}

// Greater than
if (x > y) {
    show_debug_message("x is greater than y");
}
```

#### Logical Operators:
- `&&`: Logical AND
- `||`: Logical OR
- `!`: Logical NOT

**Example in GML:**
```gml
var p = true;
var q = false;

// Logical AND
if (p && q) {
    show_debug_message("Both conditions are true");
} else {
    show_debug_message("At least one condition is false");
}

// Logical OR
if (p || q) {
    show_debug_message("At least one condition is true");
}

// Logical NOT
if (!q) {
    show_debug_message("The condition is not true");
}
```

#### Assignment Operators:
- `=`: Simple assignment
- `+=`: Addition and assignment
- `-=`: Subtraction and assignment
- `*=`: Multiplication and assignment
- `/=`: Division and assignment
- `%=`: Modulus and assignment

**Example in GML:**
```gml
var counter = 5;

// Simple assignment
counter = 10; // counter is now 10

// Addition and assignment
counter += 5; // counter is now 15

// Subtraction and assignment
counter -= 3; // counter is now 12

// Multiplication and assignment
counter *= 2; // counter is now 24

// Division and assignment
counter /= 6; // counter is now 4

// Modulus and assignment
counter %= 3; // counter is now 1
```

Understanding these operators is fundamental for creating logic, managing data, and controlling the flow in your GameMaker projects. #Operators #GameMaker