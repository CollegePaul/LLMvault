In GameMaker, Tiles are used to create backgrounds or levels efficiently using smaller images called Tilesets. These tiles can be arranged in various patterns to form larger areas like floors, walls, and landscapes. This method not only saves time but also optimizes the performance of your game by reducing redundancy.

For example, if you want to create a simple platformer level using tiles, you would first import a tileset image that includes different types of ground tiles, wall tiles, and possibly some decorative elements. You can then use the Room Editor in GameMaker Studio 2 to place these tiles on a background layer or an instance layer.

Here's a basic example using GML code to create a room with a simple tile-based floor:

```gml
// Create a new room
room_add(room_example);

// Set room dimensions
room_set_viewport(room_example, 0, true, 0, 0, 640, 480);
room_set_size(room_example, 640, 480);

// Add a background layer to the room
var bg_layer = layer_create_depth(-1000); // Create a new layer with a depth of -1000
layer_background_add(bg_layer, spr_floor_tileset, true, false, 0, 0, 640, 480);

// Fill the background with tiles from the tileset
for (var i = 0; i < room_width(room_example); i += sprite_get_width(spr_floor_tileset)) {
    for (var j = 0; j < room_height(room_example); j += sprite_get_height(spr_floor_tileset)) {
        layer_background_tile_add(bg_layer, spr_floor_tileset, i, j);
    }
}
```

In this example, `spr_floor_tileset` is a sprite that contains the tiles you want to use. The code creates a new room, sets its dimensions, and then fills it with tiles from the tileset by looping through the room's width and height in increments equal to the size of each tile.

#Tiles #GamaMaker