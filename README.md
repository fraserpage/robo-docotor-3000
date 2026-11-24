<img src="assets/icon.svg" width="64" height="64" alt="">

# Robo Doctor 3000

A pretend video-call checkup for a little one who is "too sick for school." A friendly robot doctor calls your child, runs a playful exam (temperature scan, "say AAAH", tongue, ears, heartbeat, blowing out candles, reflexes, kangaroo jumps), then reads out the result **you** chose on the parent screen.

## Use it

Open `index.html` in Chrome or Safari. No install or build step.

1. On the parent screen, type your child's name and pick today's result: *Healthy*, *A teeny bit sick (still OK for school)*, or *Sick (rest day)*.
2. Press **Start the call** and allow the camera and microphone. Nothing is recorded or sent anywhere; the camera only appears in the little "You" window.
3. Hand the device over while it rings.

**Secret parent menu:** during the call, press and hold the ⚙︎ in the top-right corner (or press `P`). From there you can change the result, skip a test (`S`) or end the call.

**Motion sensing:** with the camera on, the doctor uses [MediaPipe](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker) face and body tracking to check that your child is actually doing each test (mouth open, head turned, hand on nose, real jumps, puffed cheeks for blowing). If they don't, it asks again once or twice, then moves on cheerfully so the call never gets stuck. Everything runs on the device; the models download from Google's CDN the first time. If tracking can't load, the tests fall back to timers. Press `D` (or use the parent menu) to show tracking dots and live readings on the camera view, which helps when propping up the device.

To use it on an iPad or phone, serve the folder over HTTPS (any static host works), because browsers only give camera access to secure pages.
