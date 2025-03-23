### File IO in GameMaker

In GameMaker Studio 2 (GMS2), file input/output operations are essential for saving game progress, user settings, high scores, and other data that needs to persist between game sessions. GameMaker provides several functions to handle files, allowing developers to read from, write to, and manage files efficiently.

#### Basic File Operations

1. **Opening a File**: Use `file_text_open_read()` or `file_text_open_write()` to open a file for reading or writing.
2. **Reading/Writing Data**: Once the file is open, use functions like `file_text_read_string()`, `file_text_read_real()`, and `file_text_writeln()` to read from or write data to the file.
3. **Closing a File**: Always close files after completing operations with `file_text_close()` to free up resources.

#### Example: Saving High Scores

Here’s an example of how you might save high scores using GML:

```gml
// Function to save high score
function save_high_score(score) {
    var file = file_text_open_write("highscore.txt");
    
    // Write the new high score to the file
    file_text_writeln(file, string(score));
    
    file_text_close(file);
}

// Function to load high score
function load_high_score() {
    var file = file_text_open_read("highscore.txt");
    if (file >= 0) {  // Check if file opened successfully
        var high_score = real(file_text_read_string(file));
        file_text_close(file);
        return high_score;
    } else {
        return 0;  // Return default score if file does not exist
    }
}

// Example usage in game logic
var current_high_score = load_high_score();
show_debug_message("Current High Score: " + string(current_high_score));

if (player_score > current_high_score) {
    save_high_score(player_score);
    show_debug_message("New High Score! Saved.");
}
```

#### Explanation

- **Saving**: The `save_high_score` function opens a file named "highscore.txt" for writing, writes the player's score to it, and then closes the file.
- **Loading**: The `load_high_score` function attempts to open the same file for reading. If successful, it reads the high score from the file and converts it back to a real number. If the file does not exist, it returns 0 as a default value.

This basic example demonstrates how to perform simple file operations in GameMaker using GML to manage persistent game data.

#File IO #GameMaker