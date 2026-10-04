# Blue Media Studio

Static, GitHub Pages-ready progressive web app for:

- Microphone recording with live level meter
- Direct WAV export
- Common audio conversion through FFmpeg WebAssembly loaded on demand
- Audio import, trim, gain, fade, normalize and reverse
- Video/media preview, trim and conversion
- Audio extraction from video
- Voice modifying with pitch, EQ, compression, reverb and echo
- Add to Home Screen / PWA support
- Responsive layouts with iPhone safe-area support

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Upload every file and folder from this project to the repository root.
3. In GitHub: **Settings → Pages**.
4. Set **Source** to **Deploy from a branch**.
5. Select `main` and `/ (root)`, then save.
6. Open the generated `https://USERNAME.github.io/REPOSITORY/` URL.

Microphone access requires HTTPS. GitHub Pages provides HTTPS automatically.

## Install on mobile

- **Android / Chrome:** use the Install button or browser menu → Add to Home screen / Install app.
- **iPhone / iPad:** open in Safari → Share → Add to Home Screen.

## Important browser limitations

This project is static and performs processing locally. Browser codec support varies. WAV is the most reliable audio export. FFmpeg WebAssembly is loaded from public CDNs only when a conversion requiring it is requested. Very large/4K video files can exceed mobile-browser memory limits.
