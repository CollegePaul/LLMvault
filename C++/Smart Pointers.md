### Smart Pointers in C++

Smart pointers are a type of smart class provided by the C++ Standard Library to manage dynamic memory automatically. They help prevent memory leaks by ensuring that dynamically allocated memory is properly deallocated when it is no longer needed. The main types of smart pointers are `std::unique_ptr`, `std::shared_ptr`, and `std::weak_ptr`.

1. **`std::unique_ptr`:** This smart pointer owns and manages another object through a pointer and disposes of that object when the `unique_ptr` goes out of scope. A unique pointer ensures that there is only one owner of the resource.

   ```cpp
   #include <memory>
   #include <iostream>

   int main() {
       std::unique_ptr<int> ptr(new int(10));
       std::cout << *ptr << std::endl;  // Outputs: 10
       return 0;
   }
   ```

2. **`std::shared_ptr`:** This smart pointer allows multiple pointers to own the same resource. The resource is deallocated only when the last `shared_ptr` pointing to it goes out of scope.

   ```cpp
   #include <memory>
   #include <iostream>

   int main() {
       std::shared_ptr<int> ptr1(new int(20));
       {
           std::shared_ptr<int> ptr2 = ptr1;
           std::cout << *ptr2 << " (inside scope)" << std::endl;  // Outputs: 20
       }
       std::cout << *ptr1 << " (outside scope)" << std::endl;  // Outputs: 20
       return 0;
   }
   ```

3. **`std::weak_ptr`:** This smart pointer is used in conjunction with `shared_ptr`. It holds a non-owning reference to an object that is managed by one or more `shared_ptr` instances but does not participate in owning the object.

   ```cpp
   #include <memory>
   #include <iostream>

   int main() {
       std::shared_ptr<int> ptr1(new int(30));
       std::weak_ptr<int> weakPtr = ptr1;

       if (std::shared_ptr<int> shared = weakPtr.lock()) {  // Attempt to lock the weak pointer
           std::cout << *shared << std::endl;  // Outputs: 30
       } else {
           std::cout << "Resource has been freed" << std::endl;
       }
       return 0;
   }
   ```

While Python does not have a direct equivalent to C++ smart pointers, it uses automatic garbage collection to manage memory. However, similar concepts can be illustrated using Python's `weakref` module for weak references:

```python
import weakref

class MyClass:
    def __init__(self, value):
        self.value = value
    def __del__(self):
        print("Object is being deleted")

obj = MyClass(40)
weak_ref_to_obj = weakref.ref(obj)

print(weak_ref_to_obj())  # Outputs: <__main__.MyClass object at ...>
del obj
print(weak_ref_to_obj())  # Outputs: None (object has been garbage collected)
```

In this example, `weak_ref_to_obj` is a weak reference to an instance of `MyClass`. When the original object (`obj`) is deleted, the weak reference no longer points to it.

#Smart Pointers #cpp