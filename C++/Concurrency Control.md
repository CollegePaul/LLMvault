### Concurrency Control in C++

Concurrency control mechanisms are essential in programming to manage access to shared resources by multiple threads, ensuring data integrity and preventing race conditions. In C++, concurrency can be handled using various techniques provided by the C++11 standard library and beyond, including mutexes, condition variables, atomic operations, and more advanced constructs like futures and promises.

#### Mutexes
Mutexes are one of the simplest synchronization primitives used to protect shared data from being simultaneously accessed by multiple threads. A mutex allows only one thread to access a resource at a time. C++ provides `std::mutex`, `std::lock_guard`, and `std::unique_lock` for managing locks.

```cpp
#include <iostream>
#include <thread>
#include <mutex>

int shared_resource = 0;
std::mutex mtx;

void increment() {
    std::lock_guard<std::mutex> lock(mtx);
    ++shared_resource;
}

int main() {
    std::thread t1(increment);
    std::thread t2(increment);

    t1.join();
    t2.join();

    std::cout << "Shared Resource: " << shared_resource << std::endl; // Should print 2

    return 0;
}
```

#### Condition Variables
Condition variables are used to block a thread until another thread signals a condition or a timeout expires. They work in conjunction with mutexes.

```cpp
#include <iostream>
#include <thread>
#include <mutex>
#include <condition_variable>

std::mutex mtx;
std::condition_variable cv;
bool ready = false;

void worker_thread() {
    std::unique_lock<std::mutex> lock(mtx);
    cv.wait(lock, []{ return ready; });

    // Perform task
    std::cout << "Worker thread is processing data\n";
}

int main() {
    std::thread t(worker_thread);

    // Prepare data for the worker thread and notify it
    {
        std::lock_guard<std::mutex> lock(mtx);
        ready = true;
    }
    cv.notify_one();

    t.join();

    return 0;
}
```

#### Atomic Operations
Atomic operations are used to perform read, write, or update operations on shared data without requiring a mutex. C++11 introduced `std::atomic` for this purpose.

```cpp
#include <iostream>
#include <thread>
#include <atomic>

std::atomic<int> counter(0);

void increment() {
    ++counter;
}

int main() {
    std::thread t1(increment);
    std::thread t2(increment);

    t1.join();
    t2.join();

    std::cout << "Counter: " << counter << std::endl; // Should print 2

    return 0;
}
```

### Concurrency Control in Python

Python, being a higher-level language, abstracts many concurrency details. However, similar concepts can be implemented using the `threading` module.

#### Mutexes (Locks) in Python
In Python, locks can be used to ensure that only one thread can access a critical section of code at a time.

```python
import threading

shared_resource = 0
lock = threading.Lock()

def increment():
    global shared_resource
    with lock:
        shared_resource += 1

t1 = threading.Thread(target=increment)
t2 = threading.Thread(target=increment)

t1.start()
t2.start()

t1.join()
t2.join()

print("Shared Resource:", shared_resource)  # Should print 2
```

#### Condition Variables in Python
Python's `threading` module also provides condition variables.

```python
import threading

mutex = threading.Lock()
condition = threading.Condition(mutex)
ready = False

def worker_thread():
    with condition:
        while not ready:
            condition.wait()
        
        # Perform task
        print("Worker thread is processing data")

t = threading.Thread(target=worker_thread)

# Prepare data for the worker thread and notify it
with condition:
    ready = True
    condition.notify()

t.start()
t.join()
```

#### Atomic Operations in Python
Python's `threading` module does not provide atomic operations directly, but one can use locks to ensure atomicity.

```python
import threading

counter = 0
lock = threading.Lock()

def increment():
    global counter
    with lock:
        counter += 1

t1 = threading.Thread(target=increment)
t2 = threading.Thread(target=increment)

t1.start()
t2.start()

t1.join()
t2.join()

print("Counter:", counter)  # Should print 2
```

#Concurrency Control #cpp