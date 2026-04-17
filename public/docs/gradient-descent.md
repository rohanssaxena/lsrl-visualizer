# Gradient descent & views

## What runs

After **Generate LSRL**, the optimizer starts from that **(m, b)** (unless you reset the run). Each step uses the **analytic** gradient of the selected loss with respect to `m` and `b`, then applies:

`m ← m − η · ∂L/∂m`, `b ← b − η · ∂L/∂b`

where `η` is the **learning rate** (log slider in the bottom toolbar).

## Panels

- **Scatter**: regression line and optional **vertical residual segments** colored from green (small error) to red (large).
- **Loss vs iteration**: live curve; optional **log** Y-axis.
- **Contour**: approximate loss surface over `(m, b)` with the **descent path** overlaid.
- **Timeline**: scrub history, or use **playback** speed controls.

## Convergence

The run stops when gradients / steps become negligible, the loss is nearly flat, or progress **stalls** (then try a smaller learning rate). A hard cap also ends very long runs.

## Keyboard

With focus **outside** inputs: **← / →** step the timeline; **Space** toggles timeline playback.
