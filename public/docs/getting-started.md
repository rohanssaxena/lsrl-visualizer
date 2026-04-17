# Getting started

The **LSRL Visualizer** helps you plot `(x, y)` data, fit a line `ŷ = mx + b`, and watch **gradient descent** minimize a chosen loss.

## Quick flow

1. Enter at least **two** points in the left table (`x` and `y` as numbers).
2. Click **Plot** to draw them on the chart.
3. Choose a **Loss** in the header (MSE, MAE, Huber, or Log-cosh), then click the green **Fit …** button. For **MSE**, that fit is the exact least-squares line (closed form). For **MAE**, **Huber**, and **Log-cosh**, the same button runs **batch gradient descent** to convergence (warm-started from the MSE line) so the drawn line minimizes the **selected** loss.
4. Open the bottom panel (after a fit) to adjust **learning rate**, **steps per second**, and **Run** gradient descent for an animated walk from the current reference line.
5. With **MSE** selected, use **Draw Squares** to see squared residuals; vertical residual segments work for every loss while optimizing or scrubbing the timeline.

## Tips

- The header **Loss** menu sets the objective for the contour, the primary **Fit** action, and **Run** gradient descent. **Huber δ** appears when Huber is selected; changing δ updates the contour and, when you release the slider, re-fits the Huber reference line.
- If optimization **stalls**, lower the learning rate or try another loss.
- **Reset** (chart toolbar) clears everything; **Reset** in the optimizer strip only clears the GD run and returns the line to the current reference fit.
