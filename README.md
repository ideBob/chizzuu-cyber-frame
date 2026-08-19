# Chizzuu Cyber Frame

Real-time dual-hand **Cyber Frame** effect using [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker).

Form a rectangle with both hands (index fingers + thumbs) and a holographic cyan frame with scanlines appears and tracks your hands in real time.

![Demo concept](https://img.shields.io/badge/MediaPipe-Hand%20Landmarker-00C8FF?style=flat-square)
![Status](https://img.shields.io/badge/status-working-brightgreen?style=flat-square)

## Features

- Dual-hand tracking (left + right)
- Live cyber frame drawn between the four fingertips (index + thumb tips)
- Cyan holographic border + soft glow
- Semi-transparent fill with animated scanlines
- Status messages in Indonesian (matching original demo)
- Side info panel (`CAMERA NODE / 02`, `SUBJECT DETECTION`, `HAND FRAME AC`)
- Signature + camera icon UI

## How to Run

### Option 1 — Open directly
1. Download or clone this repo
2. Open `index.html` in **Chrome** or **Edge** (recommended)
3. Allow camera access when prompted
4. Form a box with both hands

> Note: Some browsers block camera access on `file://`. If that happens, use Option 2.

### Option 2 — Local server (recommended)
```bash
# Using VS Code Live Server, or:
npx serve .
# or
python -m http.server 5500
```
Then open `http://localhost:5500`

## Controls / Usage

| Action | Result |
|--------|--------|
| Show both hands | Frame appears |
| Form rectangle with index fingers + thumbs | Cyber Frame activates |
| Move / resize hands | Frame tracks in real time |
| Hide one or both hands | Frame disappears |

## Tech Stack

- Vanilla HTML / CSS / JavaScript
- [MediaPipe Tasks Vision](https://cdn.jsdelivr.net/npm/@mediapipe/tasks-vision) (Hand Landmarker)
- Webcam via `getUserMedia`
- Canvas 2D for overlay rendering

## Browser Support

- Chrome / Edge (best)
- Firefox (works, slightly lower performance)
- Safari (may need extra permissions)

Requires a device with a camera and WebGL/GPU support for best performance.

## Credits

Inspired by the original TikTok demo by **@zodvn** / Chizzuu Paparaz aesthetic.

---

Made with MediaPipe + pure frontend magic.
