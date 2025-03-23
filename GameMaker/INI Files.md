### Understanding INI Files in GameMaker

INI files are configuration files that store data in a simple format consisting of sections, keys, and values. They are commonly used in GameMaker Studio to manage game settings, user preferences, or any other kind of non-volatile data that needs to be saved between game sessions.

In GameMaker, INI files can be created, modified, and read using built-in functions such as `ini_open`, `ini_write_real`, `ini_read_string`, `ini_close`, etc. These functions provide a straightforward way to interact with the file system without the need for manual parsing or writing of text files.

#### Creating an INI File

To create an INI file in GameMaker, you first need to open a connection to the file using the `ini_open` function. Once opened, you can write data to it using functions like `ini_write_real`, `ini_write_string`, and `ini_write_bool`. After writing all necessary data, close the file with `ini_close`.

```gml
// Open an INI file for writing (or create if it doesn't exist)
var iniFile = "game_settings.ini";
ini_open(iniFile);

// Write some data to the INI file
ini_write_real("Audio", "Volume", 0.75);
ini_write_string("Graphics", "Resolution", "1920x1080");
ini_write_bool("Controls", "InvertYAxis", false);

// Close the INI file after writing data
ini_close();
```

#### Reading from an INI File

Reading data from an INI file is similar to writing. First, open the file using `ini_open`, then read values with functions like `ini_read_real`, `ini_read_string`, and `ini_read_bool`. Remember to close the file after reading.

```gml
// Open the INI file for reading
var iniFile = "game_settings.ini";
ini_open(iniFile);

// Read data from the INI file
var volume = ini_read_real("Audio", "Volume", 0.5); // Default value is 0.5 if not found
var resolution = ini_read_string("Graphics", "Resolution", "1280x720");
var invertYAxis = ini_read_bool("Controls", "InvertYAxis", false);

// Close the INI file after reading data
ini_close();

// Use the read values as needed in your game logic
show_debug_message("Volume: " + string(volume));
show_debug_message("Resolution: " + resolution);
show_debug_message("Invert Y Axis: " + string(invertYAxis));
```

INI files are particularly useful for settings that need to persist across different sessions or user profiles. They provide a simple and effective way of managing configuration data without the complexity of more advanced storage solutions like databases.

#INI Files #GameMaker