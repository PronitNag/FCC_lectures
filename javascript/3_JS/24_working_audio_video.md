# Audio and Video Processing Notes

## How Does the Audio Constructor Work, and What Are Some Common Methods?
The `Audio` constructor in JavaScript allows you to create and control audio elements dynamically.

### Example:
```javascript
const sound = new Audio('audio.mp3');
sound.play();
```

### Common Methods:
- `play()`: Plays the audio.
- `pause()`: Pauses the audio.
- `load()`: Reloads the audio file.
- `volume`: Adjusts the volume (`0.0` to `1.0`).
- `currentTime`: Sets or gets the current playback position.

---

## What Are the Different Types of Video and Audio Formats?

### Common Audio Formats:
- **MP3**: Compressed, widely used.
- **WAV**: Uncompressed, high quality.
- **AAC**: Better compression than MP3.
- **OGG**: Open-source alternative.

### Common Video Formats:
- **MP4**: Most common, supported by all browsers.
- **WebM**: Optimized for the web.
- **AVI**: Older format, large file size.
- **MKV**: Supports multiple audio and subtitle tracks.

---

## What Are Codecs and How Do They Work?
A **codec** (coder-decoder) compresses and decompresses media files to reduce size while maintaining quality.

### Examples of Codecs:
- **Audio Codecs**: MP3, AAC, Opus.
- **Video Codecs**: H.264, VP9, AV1.

### How They Work:
- Encoding: Converts raw data into a compressed format.
- Decoding: Converts compressed data back for playback.

---

## What Is the HTMLMediaElement API and How Does It Work?
The `HTMLMediaElement` API provides methods and properties to control media playback in `<audio>` and `<video>` elements.

### Example:
```javascript
const video = document.getElementById('myVideo');
video.play();
video.pause();
video.volume = 0.5;
```

### Key Properties:
- `playbackRate`: Adjusts the speed.
- `muted`: Mutes or unmutes.
- `loop`: Plays in a loop.
- `duration`: Total media duration.

---

## How Can You Work with the Media Streams to Capture Video and Audio from a Local Device?
Use the `navigator.mediaDevices.getUserMedia()` API to access a device's camera and microphone.

### Example:
```javascript
navigator.mediaDevices.getUserMedia({ video: true, audio: true })
  .then(stream => {
    document.querySelector('video').srcObject = stream;
  })
  .catch(error => console.error('Error accessing media devices.', error));
```

### Use Cases:
- Video conferencing.
- Screen recording.
- Audio recording.

---

## What Are Some Other Examples of Video and Audio APIs?
- **Web Audio API**: Advanced audio processing.
- **Media Source Extensions (MSE)**: Streaming custom media data.
- **WebRTC API**: Real-time peer-to-peer communication.
- **Speech Recognition API**: Converts speech to text.
- **Speech Synthesis API**: Text-to-speech functionality.

---

### Conclusion
These APIs and technologies allow developers to create interactive audio and video applications directly in the browser.

