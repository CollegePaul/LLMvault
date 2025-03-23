### Data Structures in GameMaker

In GameMaker, data structures are used to efficiently manage and manipulate collections of data. These structures help organize game elements, player stats, levels, and more, making the code cleaner and more efficient. GameMaker offers several built-in data structures including arrays, lists, stacks, queues, maps, and sets.

#### Arrays
Arrays in GameMaker are similar to those in other languages, allowing you to store multiple values of the same type. They can be one-dimensional or multi-dimensional.

```gml
// Creating a one-dimensional array
var inventory = [10, 20, 30];

// Accessing elements
show_debug_message(inventory[0]); // Outputs: 10

// Modifying an element
inventory[1] = 25;
show_debug_message(inventory[1]); // Outputs: 25
```

#### Lists
Lists are dynamic arrays that can hold any type of data, including other lists. They are useful when the number of elements is not known in advance.

```gml
// Creating a list
var items = ds_list_create();
ds_list_add(items, "sword");
ds_list_add(items, "shield");

// Accessing elements
show_debug_message(ds_list_find_value(items, 0)); // Outputs: sword

// Deleting a list when done
ds_list_destroy(items);
```

#### Stacks and Queues
Stacks follow the Last-In-First-Out (LIFO) principle while queues follow First-In-First-Out (FIFO). They are useful for managing operations like undo/redo or scheduling tasks.

```gml
// Creating a stack
var actions = ds_stack_create();
ds_stack_push(actions, "jump");
ds_stack_push(actions, "run");

// Popping elements from the stack
show_debug_message(ds_stack_pop(actions)); // Outputs: run

// Creating a queue
var tasks = ds_queue_create();
ds_queue_enqueue(tasks, "task1");
ds_queue_enqueue(tasks, "task2");

// Dequeuing elements from the queue
show_debug_message(ds_queue_dequeue(tasks)); // Outputs: task1

// Cleaning up
ds_stack_destroy(actions);
ds_queue_destroy(tasks);
```

#### Maps and Sets
Maps store key-value pairs, making them ideal for storing settings or configurations. Sets store unique values without any particular order.

```gml
// Creating a map
var settings = ds_map_create();
ds_map_add(settings, "volume", 100);
ds_map_add(settings, "fullscreen", false);

// Accessing elements in a map
show_debug_message(string(ds_map_find_value(settings, "volume"))); // Outputs: 100

// Creating a set
var unique_ids = ds_set_create();
ds_set_add(unique_ids, player.id);
ds_set_add(unique_ids, enemy.id);

// Checking for existence in a set
if (ds_set_exists(unique_ids, player.id)) {
    show_debug_message("Player ID exists");
}

// Cleaning up
ds_map_destroy(settings);
ds_set_destroy(unique_ids);
```

Understanding and effectively using data structures can greatly enhance the functionality and performance of games developed with GameMaker. #DataStructures #GameMaker