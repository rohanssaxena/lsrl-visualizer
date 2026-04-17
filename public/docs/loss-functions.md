# Loss functions

All losses are averaged over your plotted points. Residuals are `e = y − (mx + b)`.

## MSE — mean squared error

`L = mean(e²)`

Penalizes large errors heavily. For a linear model, minimizing MSE gives the **ordinary least squares** line. With **MSE** selected, the primary **Fit MSE (exact LSRL)** button computes that line in closed form (no gradient descent needed for the reference fit).

## MAE — mean absolute error

`L = mean(|e|)`

Treats all error sizes more evenly; more robust to outliers than MSE. The gradient uses the **sign** of `e` (subgradient at `e = 0`). With **MAE** selected, the primary fit button minimizes this loss with **batch gradient descent** to convergence (starting from the MSE line).

## Huber

For `|e| ≤ δ`: behaves like **½ e²** (MSE-like). For larger `|e|`: grows **linearly** like MAE. A compromise between sensitivity and outlier resistance. Use the **Huber δ** control when this loss is active; the reference line is fit with the same batch GD procedure as MAE and Log-cosh.

## Log-cosh

`L = mean(log(cosh(e)))`

Smooth everywhere. Near zero it behaves like MSE; for large `|e|` the slope of the loss saturates (similar spirit to MAE tails). Gradient uses `tanh(e)`. The primary fit uses batch GD to convergence, like MAE and Huber.
