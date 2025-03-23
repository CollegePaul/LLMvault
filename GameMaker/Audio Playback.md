### Audio Playback in GameMaker

In GameMaker Studio 2 (GMS2), audio playback is managed using a variety of functions that allow developers to control sound effects, music, and background tracks. GameMaker supports different audio formats like WAV, OGG Vorbis, FLAC, and MP3. The process involves loading audio assets into the game's resources and then playing, pausing, stopping, or manipulating them during gameplay.

#### Basic Audio Functions:
- **`audio_play_sound(snd, loop)`**: Plays a sound effect from start to finish, optionally looping it.
- **`audio_stop_sound(snd)`**: Stops all instances of a particular sound.
- **`audio_pause_sound(snd)`**: Pauses all instances of a specified sound.
- **`audio_resume_sound(snd)`**: Resumes playing a previously paused sound.

#### Music Playback:
For background music, GameMaker provides functions like `audio_play_music`, `audio_stop_music`, and others. However, these are generally less flexible than those for sound effects and are more suited for simple use cases where only one piece of music plays at a time.

- **`audio_play_music(music)`**: Plays a music track in the background.
- **`audio_stop_music()`**: Stops any currently playing background music.
- **`audio_pause_music()`**: Pauses the current background music.
- **`audio_resume_music()`**: Resumes the paused background music.

#### Examples:

**Example 1: Playing a Sound Effect**
```gml
// Load a sound effect into a variable (this is typically done in the Create event)
var snd_jump = audio_play_sound(snd_Jump, false);
```

**Example 2: Controlling Background Music**
```gml
// Play background music when entering a room (Create Event of Room)
audio_play_music(mus_BackgroundLoop);

// Stop music when exiting the room (End Room event or Exit Room Trigger)
audio_stop_music();
```

**Example 3: Looping a Sound Effect**
```gml
// Start looping a sound effect (Create Event of Object)
var snd_loop = audio_play_sound(snd_Engine, true);
```

#### Advanced Audio Management:
GameMaker also supports more advanced audio features like changing volume, panning, and controlling the pitch of sounds. This can be achieved using functions such as `audio_set_gain`, `audio_get_gain`, `audio_set_pan`, and `audio_set_pitch`.

- **`audio_set_gain(snd, gain)`**: Adjusts the volume of a sound. Gain is between 0 (silent) and 1 (full volume).
- **`audio_set_pan(snd, pan)`**: Pans a sound left or right. Pan value ranges from -1 (left) to 1 (right), with 0 being center.
- **`audio_set_pitch(snd, pitch)`**: Changes the pitch of a sound. Pitch values less than 1 lower the pitch, and values greater than 1 raise it.

**Example: Adjusting Sound Gain**
```gml
// Reduce the volume of the current sound to 50%
audio_set_gain(snd_effect, 0.5);
```

Understanding and utilizing these audio functions effectively can greatly enhance the auditory experience in your GameMaker games, making them more immersive and engaging.

#AudioPlayback #GameMaker