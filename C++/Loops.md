### Loops in C++

In C++, loops are used to execute a block of code repeatedly until a certain condition is met. There are three primary types of loops available in C++:

1. **For Loop**: This loop is typically used when you know how many times you want to execute a statement or a block of statements. It consists of an initialization, a condition, and an increment/decrement expression.

   ```cpp
   for (int i = 0; i < 5; i++) {
       std::cout << "Iteration number: " << i + 1 << std::endl;
   }
   ```

2. **While Loop**: A `while` loop is used when you want to repeat an action as long as a particular condition is true. The syntax is simpler than the `for` loop and is often used when the number of iterations is not known beforehand.

   ```cpp
   int i = 0;
   while (i < 5) {
       std::cout << "Iteration number: " << i + 1 << std::endl;
       i++;
   }
   ```

3. **Do-While Loop**: Similar to the `while` loop, but with a key difference: The code inside a `do-while` loop is executed at least once regardless of whether the condition evaluates to true or false.

   ```cpp
   int i = 0;
   do {
       std::cout << "Iteration number: " << i + 1 << std::endl;
       i++;
   } while (i < 5);
   ```

Loops are essential for tasks such as iterating over arrays, processing data, and automating repetitive tasks in programming. They help in writing more efficient and concise code by reducing redundancy.

#Loops #cpp