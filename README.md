# LSRL Visualizer

An interactive web‑based tool for visualising **Least Squares Regression Lines (LSRL)** using **D3.js**.  Users can:

- Enter up to 10 `(x, y)` data points.
- Plot the points on a four‑quadrant coordinate system.
- Generate the regression line and see its equation.
- Draw residual squares (with subtle styling) and view detailed tooltips.
- Run gradient‑descent optimisation with a controllable speed, watch the line converge, and scrub through each iteration.

The project is built with a tiny **Node.js/Express** server that serves the static front‑end.

---

## Quick Start

```bash
# Clone the repo (if you haven't already)
git clone https://github.com/rohanssaxena/lsrl-visualizer.git
cd lsrl-visualizer

# Install dependencies
npm install

# Start the server
node server.js
```

Open your browser at `http://localhost:3000`.

---

## Project Structure

```
lsrl-visualizer/
├─ public/                # Front‑end assets
│   └─ index.html        # All HTML, CSS and D3 logic
├─ server.js              # Minimal Express server
├─ package.json           # Project metadata & dependencies
└─ README.md              # ← This file
```

---

## Features

- **Four‑quadrant chart** – axes cross at (0, 0) and automatically scale to your data.
- **Dynamic tooltips** – hover over points, squares or the regression line for detailed info.
- **Residual squares** – pale fill with a 1 px border, colour‑coded by area.
- **Gradient descent animation** – adjustable speed, play/pause, scrubbable timeline.
- **Responsive UI** – dark‑theme, modern typography, smooth micro‑animations.

---

## Development

If you want to modify the visualisation, edit `public/index.html`.  The file contains:

- CSS variables for colours and spacing.
- D3‑based rendering functions (`renderPoints`, `renderLine`, `renderSquares`).
- UI logic for the data table, buttons, and animation controls.

After changes, simply refresh the page – the server serves the updated file.

---

## License

MIT © 2026 Rohan Saxena
