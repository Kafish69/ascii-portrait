# For You — ASCII portrait

Turn any photo into flowing ASCII art. The app finds the person in the photo, then the background characters stream downwards while the person's characters slide sideways. Every character takes the colour of the photo beneath it as it moves, so the picture stays sharp while everything flows. Add your own song and export it as a video.

Everything runs in the browser. Photos and music never leave the visitor's device.

## Use it

1. Open `index.html` in Chrome or Edge (double-click works, no server needed).
2. **CHOOSE PHOTO** — JPG, PNG, WEBP or iPhone HEIC. You can also drag a photo onto the page or paste it.
3. Move the mouse to show the controls:
   - **detail** — smaller characters = sharper picture. **speed** — how fast the characters flow.
   - **MUSIC** — pick any song from your device. If the browser blocks sound, click anywhere once.
   - **caption** — separate lines with `|`, e.g. `for you | only you`.
   - **video** — 1920×1080 landscape, 1080×1920 reel or 1080×1080 square.
   - **length** — 10, 15, 20 or 30 seconds.
   - **MAKE VIDEO** — records with the music, then shows a preview and a **DOWNLOAD VIDEO** button. Keep the tab open while it records.
   - Press **M** to pause or play the music.

## Host it free on GitHub Pages

1. Create a new public repository on GitHub, e.g. `ascii-portrait`.
2. Upload `index.html` and `README.md` (**Add file → Upload files → Commit**).
3. Go to **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, then Branch to **main** and folder to **/ (root)**, then **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/ascii-portrait/`.

Or from a terminal:

```bash
git init
git add index.html README.md
git commit -m "ASCII portrait"
git branch -M main
git remote add origin https://github.com/<your-username>/ascii-portrait.git
git push -u origin main
```

Then turn on Pages as in step 3.

## Notes

- Video export uses the browser's built-in recorder. Chrome and Edge on desktop give MP4 files. Some browsers give WEBM instead.
- On a phone, recording works in recent Chrome (Android) and Safari (iOS). Desktop is the most reliable.
- Finding the person uses Google's MediaPipe selfie segmentation, loaded from jsDelivr and run locally in the browser (the photo is not uploaded). It needs an internet connection the first time; offline, the whole picture flows as one layer.
- HEIC conversion loads a small library from jsDelivr the first time it is needed.
