# Day 5: HTML5 Audio and Video Elements

## HTML5 Media Elements
HTML5 introduced native support for audio and video playback without plugins.

### Audio Element
```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
    <source src="song.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>
```

Audio Attributes:
- `controls`: Shows playback controls
- `autoplay`: Plays automatically
- `loop`: Loops the audio
- `preload`: Preloads the audio
- `muted`: Mutes the audio

### Video Element
```html
<video width="320" height="240" controls>
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.ogg" type="video/ogg">
    Your browser does not support the video tag.
</video>
```

Video Attributes:
- `width`/`height`: Video dimensions
- `poster`: Image to show before video plays
- `controls`: Shows playback controls
- `autoplay`: Plays automatically
- `loop`: Loops the video
- `muted`: Mutes the audio

### Media Events
- `play`: When media starts playing
- `pause`: When media is paused
- `ended`: When media ends
- `error`: When there's an error

## Exercise
Create an HTML5 page that includes:
1. An audio player with multiple formats
2. A video player with controls
3. A playlist interface
4. Basic styling for media controls
5. Error handling for unsupported formats

Save your work as `exercise.html` in this folder.
