# ditschiteiser

A browser plot digitizer and measuring tool. Click an image to turn pixels into real-world coordinates with an affine calibration (linear or log₁₀ axes), or measure distances from a known reference length. Export the results as CSV or copy them to the clipboard.

Live: https://fambeho75.github.io/ditschiteiser/

The same page is also at [`ditschiteiser.html`](ditschiteiser.html).

## Usage

**Load.** Drop an image onto the page, or click **Browse file**. PNG, JPG, GIF, BMP, WebP, and SVG are listed. **Load image** (later **Load new image**) returns to the drop zone and clears the current calibration, points, and measurements. A loaded image opens in digitize calibration.

**Digitize.**

1. Set **X axis** and **Y axis** to Linear or Log₁₀. Log axes require positive (non-zero) reference values.
2. Click three known locations on the image. Each click asks for a label and real-world X and Y. **Confirm** or Enter accepts the dialog; **Cancel** or Escape dismisses it.
3. After a valid calibration, the guide switches to digitize mode. Click anywhere on the image to record data points.
4. **⬇ CSV** downloads `digitized_points.csv` (`Point,X,Y`). **⎘ Copy** puts the same text on the clipboard. Both stay disabled until calibration is valid and at least one point exists.
5. **Clear** removes the data points.

**Measure.**

1. Click **Measure**.
2. Click two points on a feature of known length, then enter that real-world distance. **Confirm** or Enter accepts it; **Cancel** or Escape dismisses it.
3. Select two points to measure the distance between them. Repeat for more segments.
4. **⬇ CSV** downloads `measurements.csv` (`Measurement,Distance`). **⎘ Copy** puts the same text on the clipboard. Both stay disabled until at least one measurement exists.
5. **Clear** removes the measurements. **Recalibrate** clears the reference length and the measurements.
