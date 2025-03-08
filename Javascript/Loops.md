### Loops in JavaScript

In JavaScript, loops are used to execute a block of code repeatedly until a specified condition evaluates to false. They are essential for automating repetitive tasks without writing the same code multiple times. There are several types of loops in JavaScript:

1. **For Loop:** The `for` loop is commonly used when the number of iterations is known beforehand. It consists of three parts: initialization, condition, and increment/decrement.

   ```javascript
   for (let i = 0; i < 5; i++) {
       console.log(i);
   }
   ```

2. **While Loop:** The `while` loop continues to execute as long as the specified condition is true. It is useful when the number of iterations is not known beforehand.

   ```javascript
   let count = 0;
   while (count < 5) {
       console.log(count);
       count++;
   }
   ```

3. **Do-While Loop:** Similar to the `while` loop, but it guarantees that the block of code will be executed at least once before checking the condition.

   ```javascript
   let i = 0;
   do {
       console.log(i);
       i++;
   } while (i < 5);
   ```

4. **For-In Loop:** The `for-in` loop is used to iterate over the properties of an object or the elements of an array.

   ```javascript
   const person = {fname:"John", lname:"Doe", age:25};
   
   for (let x in person) {
       console.log(person[x]);
   }
   ```

5. **For-Of Loop:** The `for-of` loop is used to iterate over iterable objects like arrays, strings, maps, sets, etc.

   ```javascript
   const fruits = ["apple", "banana", "cherry"];
   
   for (let fruit of fruits) {
       console.log(fruit);
   }
   ```

Loops are fundamental in programming and JavaScript provides a variety to choose from depending on the specific needs of your code. #Loops #Javascript