# SWF to GIF

A browser-based tool for turning old Flash (`.swf`) animations or a sequence of images into an animated GIF. It is a single HTML file with the Flash renderer, GIF encoder, and a sample SWF embedded, so it can also run offline after you save it.

**Open the tool:** [SWF to GIF](https://jairogd.github.io/swf-to-gif/)

## How to use it

1. Open the site in a current version of Chrome, Edge, or Firefox.
2. Drop in an SWF file, try the included `impact.swf` sample, or switch to **Image sequence** and select images.
3. Check the preview and adjust the capture duration, dimensions, speed, loop, or background.
4. Select **Create GIF**, then **Download GIF**.

The selected files are processed in your browser. The tool does not upload them to a server. You can also download `index.html` from this repository and open it locally.

## Limits

- GIF has at most 256 colors per frame, no audio, and only on/off transparency.
- The default SWF export uses up to 50 FPS. **All frames** keeps every captured frame, but some GIF viewers play very short delays more slowly.
- SWF export captures playback from the beginning without clicks or other interaction. Script-driven animations may need a longer capture duration.
- SWF rendering depends on Ruffle compatibility. External assets that are not embedded in the SWF are not loaded.
- Captured frames are limited to 256 MB; GIF output is limited to 12 million pixels per frame.

## Included software

The single-file build embeds Ruffle 0.2.0 for SWF rendering and gifenc 1.0.3 for GIF encoding. Their license notices are included in the **Library licenses** section of the page.

