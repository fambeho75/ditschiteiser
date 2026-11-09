<img src="icon-512.png" width="96">

# ditschiteiser

A browser plot digitizer and measuring tool. Click an image to turn pixels into real-world coordinates with an affine calibration (linear or log₁₀ axes), or measure distances from a known reference length. Export the results as CSV or copy them to the clipboard.

Live: https://fambeho75.github.io/ditschiteiser/

The same page is also at [`ditschiteiser.html`](ditschiteiser.html).

## Usage

**Load.** Drop an image onto the page, click **Browse file**, or paste with Ctrl/Cmd+V. PNG, JPG, GIF, BMP, WebP, and SVG are listed. **Load new image** asks before discarding the current calibration, points, and measurements, then returns to the drop zone. A loaded image opens in digitize calibration.

**Digitize.**

1. Set **X axis** and **Y axis** to Linear or Log₁₀. Log axes require positive (non-zero) reference values.
2. Click three known locations on the image. Each click asks for a label and real-world X and Y. **Confirm** or Enter accepts the dialog; **Cancel** or Escape dismisses it.
3. After a valid calibration, the guide switches to digitize mode. Click anywhere on the image to record data points.
4. **⬇ CSV** downloads `digitized_points.csv` (`Point,X,Y`). **⎘ Copy** puts the same text on the clipboard. Both stay disabled until calibration is valid and at least one point exists.
5. **Clear** asks before removing the data points.

**Measure.**

1. Click **Measure**.
2. Click two points on a feature of known length, then enter that real-world distance. **Confirm** or Enter accepts it; **Cancel** or Escape dismisses it.
3. Select two points to measure the distance between them. Repeat for more segments.
4. **⬇ CSV** downloads `measurements.csv` (`Measurement,Distance`). **⎘ Copy** puts the same text on the clipboard. Both stay disabled until at least one measurement exists.
5. **Clear** asks before removing the measurements. **Recalibrate** asks before clearing the reference length and the measurements.

## Shortcuts

- **Ctrl/Cmd+V** pastes an image from the clipboard. If an image is already loaded, or calibration or points exist, the app asks before replacing them.
- **Mouse wheel** zooms around the cursor, from 0.05× to 40×.
- **Middle-drag**, **right-drag**, or **Space+drag** pans the image.
- **Fit**, or the **0** / **F** keys, fits the image to the window.
- The sun/moon button in the top bar toggles light and dark. The first visit follows the system setting, and the theme is remembered in the browser.
