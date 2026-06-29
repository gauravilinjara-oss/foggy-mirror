# Fog Mirror

An interactive foggy-mirror toy that runs entirely in the browser. Your webcam becomes a misted mirror you can write on with your hand — all processing is on-device, nothing is uploaded.

## Gestures

- **Pinch** (thumb + index touch) — write in the fog
- **Fist** — wipe the glass clear
- **Two fingers** (peace sign) — mist it back up
- **Open / relaxed hand** — does nothing (move freely)
- **Blow** into the mic — also fogs the glass

A mouse/trackpad also works: just drag to write. A status readout in the top-right shows what the camera is reading (WRITE / ERASE / FOG / READY).

## Running it

It needs a secure context for the camera, so open it from `https://` or `localhost` (not `file://` in some browsers).

Locally:

```
python3 -m http.server 8000
# then open http://localhost:8000
```

## Hosting on GitHub Pages

Push this folder to a repo, then in **Settings → Pages** set the source to the `main` branch. GitHub serves `index.html` at `https://<username>.github.io/<repo>/`, where the camera works over HTTPS.

## Built with

- [MediaPipe Hand Landmarker](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) for hand tracking
- Canvas 2D for the fog/condensation rendering
