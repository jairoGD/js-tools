# JS Tools

Two browser-based GIF tools. [Open the site](https://jairogd.github.io/js-tools/) and choose a tool from the home page.

| Tool | What it does | Open directly |
| --- | --- | --- |
| SWF to GIF | Converts SWF animations or image sequences to GIF, with a preview and capture settings. | [SWF to GIF](https://jairogd.github.io/js-tools/swf-to-gif.html) |
| GIF Creator | Creates an animated GIF from images with an adjustable delay between frames. | [GIF Creator](https://jairogd.github.io/js-tools/gif-creator.html) |

Files are processed in your browser. To use the tools locally, download the repository and open `index.html`. Keep `gif-creator.html` and `gifshot.min.js` in the same folder. `swf-to-gif.html` already includes its SWF renderer and GIF encoder.

## Files

- `index.html`: home page for choosing a tool.
- `swf-to-gif.html`: SWF and image sequence converter.
- `gif-creator.html`: simple image-to-GIF tool moved from `animated-Gif-creator`.
- `gifshot.min.js`: gifshot 0.3.2, used by GIF Creator. Its license is in `GIFSHOT-LICENSE.txt`.

## SWF converter limitations

- GIF supports at most 256 colors per frame, no audio, and only on/off transparency.
- The default export uses up to 50 FPS. **All frames** preserves every captured frame, but some GIF viewers play very short delays more slowly.
- SWF capture starts at the beginning without clicks or other interaction. Script-driven animations may need a longer capture duration.
- SWF rendering depends on Ruffle compatibility. External resources that are not embedded in the SWF are not loaded.
- Captured frames are limited to 256 MB; each GIF frame is limited to 12 million pixels.

The SWF converter includes Ruffle 0.2.0 and gifenc 1.0.3. Their license notices are included on the tool page.
