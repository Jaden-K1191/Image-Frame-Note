# Brush Photo Edge Asset Pack Guide

FrameNote now supports **asset-based Brush Photo Edge rendering**.

## Naming rule
For each style, place PNG files in this folder using the following names:

- `A_landscape_mask.png`
- `A_landscape_overlay.png`
- `A_portrait_mask.png`
- `A_portrait_overlay.png`
- `A_square_mask.png`
- `A_square_overlay.png`

Repeat the same naming pattern for styles **B, C, D, E, F**.

## What each file means
- `*_mask.png`  
  White / alpha mask that defines the visible photo area. The outside should be transparent.
- `*_overlay.png`  
  Transparent PNG layer that contains brush texture painted on top of the photo edge.

## Recommended production workflow
1. Make the mask and overlay separately in a graphics editor.
2. Export both as transparent PNG.
3. Use one of the three aspect groups:
   - `landscape`
   - `portrait`
   - `square`
4. Re-open `index.html` and select **Brush Photo Edge**.

## Fallback behavior
If a matching asset file does not exist, FrameNote automatically falls back to the built-in Brush Photo Edge rendering.

## Recommended canvas sizes
- landscape: `2400 x 1800`
- portrait: `1800 x 2400`
- square: `2200 x 2200`

The app scales the files automatically.
