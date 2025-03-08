### Strings in C++

In C++, strings are used to store sequences of characters. They can be manipulated using various functions provided by the C++ Standard Library. The `std::string` class, defined in the `<string>` header file, is commonly used for handling strings due to its flexibility and ease of use.

Here are some basic operations you can perform with strings in C++:

1. **Initialization**: You can initialize a string using different methods:
   ```cpp
   #include <iostream>
   #include <string>

   int main() {
       std::string str1 = "Hello";
       std::string str2("World");
       std::cout << str1 << " " << str2 << std::endl; // Output: Hello World
       return 0;
   }
   ```

2. **Concatenation**: Strings can be concatenated using the `+` operator or the `append()` function:
   ```cpp
   #include <iostream>
   #include <string>

   int main() {
       std::string str1 = "Hello";
       std::string str2 = "World";
       std::string result = str1 + " " + str2; // Using +
       std::cout << result << std::endl; // Output: Hello World

       str1.append(" ").append(str2); // Using append()
       std::cout << str1 << std::endl; // Output: Hello World
       return 0;
   }
   ```

3. **Accessing Characters**: Individual characters can be accessed using the `[]` operator or the `at()` function:
   ```cpp
   #include <iostream>
   #include <string>

   int main() {
       std::string str = "Hello";
       char ch1 = str[0]; // Using []
       char ch2 = str.at(1); // Using at()
       std::cout << ch1 << ch2 << std::endl; // Output: He
       return 0;
   }
   ```

4. **Length**: The length of a string can be obtained using the `length()` or `size()` function:
   ```cpp
   #include <iostream>
   #include <string>

   int main() {
       std::string str = "Hello";
       std::cout << str.length() << std::endl; // Output: 5
       std::cout << str.size() << std::endl; // Output: 5
       return 0;
   }
   ```

5. **Substring**: You can extract a substring using the `substr()` function:
   ```cpp
   #include <iostream>
   #include <string>

   int main() {
       std::string str = "Hello World";
       std::string sub = str.substr(6, 5); // Start at index 6, length of 5
       std::cout << sub << std::endl; // Output: World
       return 0;
   }
   ```

### Examples in Python

Although the syntax and some functionalities differ, Python's `str` type also provides similar capabilities:

1. **Initialization**:
   ```python
   str1 = "Hello"
   str2 = 'World'
   print(str1, str2) # Output: Hello World
   ```

2. **Concatenation**:
   ```python
   result = str1 + " " + str2
   print(result) # Output: Hello World

   str1 += " " + str2
   print(str1) # Output: Hello World
   ```

3. **Accessing Characters**:
   ```python
   ch1 = str1[0] # Using []
   ch2 = str1[1] # Python does not have an at() function, but [] works similarly
   print(ch1, ch2) # Output: He
   ```

4. **Length**:
   ```python
   length = len(str1)
   print(length) # Output: 11
   ```

5. **Substring**:
   ```python
   sub = str1[6:11] # Start at index 6, end before index 11
   print(sub) # Output: World
   ```

#Strings #cpp