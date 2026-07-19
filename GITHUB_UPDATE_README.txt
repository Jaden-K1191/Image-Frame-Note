FrameNote GitHub Pages cache-safe update

This patch uses a new JavaScript filename: app-v249-20260719.js
The index.html file points to that filename, preventing GitHub Pages/browser cache from reusing an older app.js.

Upload the extracted contents to the repository root.
Do not upload the ZIP itself.
Keep existing assets/vendor, assets/fonts, assets/logos and other existing assets.
The included assets/brush_photo_edge folder must be uploaded.
