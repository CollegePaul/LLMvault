### RAII Idiom in C++

The RAII (Resource Acquisition Is Initialization) idiom is a core concept in C++ that ensures proper management of resources. It is based on the principle that resource acquisition should be tied to object initialization, and resource release should be handled by the destructor when the object goes out of scope. This guarantees that all resources are properly cleaned up, even if exceptions occur.

#### Key Points:
- **Resource Acquisition**: When an object is created, it acquires a resource.
- **Resource Release**: The destructor automatically releases the resource when the object is destroyed (goes out of scope).

#### Example in C++:

```cpp
#include <iostream>
#include <fstream>

class FileHandler {
public:
    // Constructor: Opens the file and acquires the resource
    FileHandler(const std::string& filename) : file(filename, std::ios::out) {
        if (!file.is_open()) {
            throw std::runtime_error("Failed to open file");
        }
        std::cout << "File opened successfully." << std::endl;
    }

    // Destructor: Closes the file and releases the resource
    ~FileHandler() {
        if (file.is_open()) {
            file.close();
            std::cout << "File closed successfully." << std::endl;
        }
    }

    // Method to write data to the file
    void write(const std::string& data) {
        file << data;
    }

private:
    std::ofstream file;
};

int main() {
    try {
        FileHandler handler("example.txt");
        handler.write("Hello, RAII!");
    } catch (const std::exception& e) {
        std::cerr << "Exception: " << e.what() << std::endl;
    }

    // The file is automatically closed when handler goes out of scope
    return 0;
}
```

#### Explanation:
In this C++ example, the `FileHandler` class manages a file resource. The constructor opens the file, and the destructor ensures that the file is closed, even if an exception occurs during file operations.

### Similar Concept in Python

Python doesn't have explicit destructors like C++, but it does manage resources using context managers (`with` statement). This mechanism can be used to achieve similar behavior as RAII.

#### Example in Python:

```python
class FileHandler:
    def __init__(self, filename):
        self.file = open(filename, 'w')
        print("File opened successfully.")

    def __enter__(self):
        return self

    def write(self, data):
        self.file.write(data)

    def __exit__(self, exc_type, exc_value, traceback):
        self.file.close()
        print("File closed successfully.")

def main():
    try:
        with FileHandler('example.txt') as handler:
            handler.write("Hello, RAII-like in Python!")
    except Exception as e:
        print(f"Exception: {e}")

# The file is automatically closed when the 'with' block is exited
if __name__ == "__main__":
    main()
```

#### Explanation:
In this Python example, the `FileHandler` class uses context management methods (`__enter__` and `__exit__`) to manage the file resource. When used with a `with` statement, the file is automatically closed when the block is exited, similar to how RAII works in C++.

#RAII Idiom #cpp