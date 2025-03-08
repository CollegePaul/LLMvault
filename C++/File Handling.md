### File Handling in C++

File handling in C++ involves reading from and writing to files using streams, similar to how input and output are handled using `cin` and `cout`. The primary classes used for file operations are `ifstream` (input file stream), `ofstream` (output file stream), and `fstream` (file stream). These classes are part of the `<fstream>` library.

#### Basic Operations:

1. **Writing to a File:**
   - Include the `<fstream>` header.
   - Create an object of `ofstream`.
   - Open a file using the `open()` function or constructor.
   - Use the insertion operator (`<<`) to write data to the file.
   - Close the file using the `close()` function.

   ```cpp
   #include <iostream>
   #include <fstream>

   int main() {
       std::ofstream outFile;
       outFile.open("example.txt");

       if (outFile.is_open()) {
           outFile << "Hello, world!" << std::endl;
           outFile.close();
       } else {
           std::cout << "Unable to open file" << std::endl;
       }

       return 0;
   }
   ```

2. **Reading from a File:**
   - Include the `<fstream>` header.
   - Create an object of `ifstream`.
   - Open a file using the `open()` function or constructor.
   - Use the extraction operator (`>>`) to read data from the file.
   - Close the file using the `close()` function.

   ```cpp
   #include <iostream>
   #include <fstream>

   int main() {
       std::ifstream inFile;
       std::string line;

       inFile.open("example.txt");

       if (inFile.is_open()) {
           while (getline(inFile, line)) {
               std::cout << line << std::endl;
           }
           inFile.close();
       } else {
           std::cout << "Unable to open file" << std::endl;
       }

       return 0;
   }
   ```

3. **Appending to a File:**
   - Open the file with `ios::app` mode.

   ```cpp
   #include <iostream>
   #include <fstream>

   int main() {
       std::ofstream outFile;
       outFile.open("example.txt", std::ios::app);

       if (outFile.is_open()) {
           outFile << "Appending a new line." << std::endl;
           outFile.close();
       } else {
           std::cout << "Unable to open file" << std::endl;
       }

       return 0;
   }
   ```

### File Handling in Python

In Python, file handling is done using built-in functions like `open()`, `read()`, `write()`, and `close()`. The `with` statement is often used for opening files to ensure they are properly closed after their suite finishes.

#### Basic Operations:

1. **Writing to a File:**

   ```python
   with open('example.txt', 'w') as file:
       file.write("Hello, world!\n")
   ```

2. **Reading from a File:**

   ```python
   with open('example.txt', 'r') as file:
       for line in file:
           print(line.strip())
   ```

3. **Appending to a File:**

   ```python
   with open('example.txt', 'a') as file:
       file.write("Appending a new line.\n")
   ```

#File Handling #cpp