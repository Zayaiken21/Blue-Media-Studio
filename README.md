# Blue Media Studio Pro

A static, GitHub Pages-ready media PWA that uses real browser media APIs.

## Real microphone path
- `navigator.mediaDevices.getUserMedia()` opens the physical microphone.
- Web Audio `ScriptProcessorNode` captures PCM samples directly.
- WAV is encoded locally from the captured PCM, independent of MediaRecorder codec support.
- MediaRecorder is also used when available to preserve a native compressed recording.
- Device enumeration allows choosing an available audio input after permission is granted.

## Real audio editor
- Files are read with File/Blob APIs and decoded with Web Audio `decodeAudioData()`.
- WAV/AIFF are rendered from PCM locally.
- M4A/AAC/WEBM/OGG exports are enabled only if the current browser exposes an encoder.

## Real voice modifier
- Uses OfflineAudioContext to render EQ, compression, reverb, echo, gain and pitch/rate effects.

## Real video page
- Imports an actual local file into a `<video>` element using an object URL.
- Trim export redraws decoded video frames to a canvas and records that canvas stream with the browser encoder.
- Audio from the media element is routed into the rendered export when supported.
- WAV extraction captures decoded audio from the selected video through Web Audio.
- Save Current Frame exports the current decoded video frame to PNG.

## Important browser limitation
A static GitHub Pages app cannot ship operating-system codecs that Safari/Chrome themselves do not decode/encode. The file picker therefore allows any file instead of hiding unsupported files, and the app reports codec failures after selection. MP4/H.264/MOV are typically the most reliable video inputs on iPhone; WAV/M4A/AAC/MP3 are the most reliable audio inputs.

## Deploy
Upload the contents of this folder to the root of a GitHub repository and enable GitHub Pages from the main branch.
