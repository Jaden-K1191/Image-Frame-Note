FrameNote GitHub Complete Patch — 2026-07-19

This patch includes all integrated updates from today's work:

1. Brush Photo Edge mask/overlay update
   - Styles A–F
   - Separate landscape, portrait, and square assets
2. Photo Data template
   - Right-side data panel
   - RGB histogram, dominant colors, average color, brightness, image size, ratio, and EXIF
   - Lens display prioritizes LensModel and uses Lens only as fallback
3. Multi Frame template
   - Hero + Two · Landscape
   - Hero (Portrait) + Two Mini (Landscape)
   - Triple Strip · Panorama
   - Double Stack · Landscape
   - Diptych · Portrait
   - Original image aspect ratios preserved
   - No automatic photo repetition
   - EXIF/title/location/logo/watermark removed; author display retained
4. Existing templates and app functions remain included.

HOW TO UPDATE GITHUB

- Extract this ZIP locally.
- Open the existing FrameNote repository.
- Copy all extracted files and folders into the repository root.
- Allow replacement/overwrite of existing files.
- Upload or commit the extracted contents, not this ZIP file itself.

Important:
- Keep the folder structure exactly as included.
- The assets/brush_photo_edge folder is required. Do not upload only app.js/index.html.
- Preview-only large brush images are intentionally excluded because the running app does not reference them.
