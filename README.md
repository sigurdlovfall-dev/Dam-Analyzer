# Dam Analyzer

A web-based application for analyzing the stability of gravity dams according to Norwegian Dam Safety Standards (NVE). It calculates forces, moments, and stress distributions to determine whether a dam meets safety criteria.

## Features

- **Stability Analysis** -- Calculates sliding safety factor, overturning safety factor, and base stress distribution per NVE requirements.
- **Interactive Visualization** -- Real-time 2D SVG diagram of the dam cross-section with click-and-drag editing of geometry and water levels.
- **CSV Export** -- Export analysis results (input parameters, forces, moments, stress values, safety factors) to a timestamped CSV file.

## How It Works

The tool models a trapezoidal gravity dam cross-section and computes:

| Calculation | Minimum Requirement |
|---|---|
| Sliding safety factor | >= 1.5 |
| Overturning safety factor | >= 1.5 |
| Base tension | No tensile stress allowed |

Forces considered include dam self-weight, upstream/downstream hydrostatic pressure, and uplift.

## Input Parameters

- Dam geometry: height, top width, base width
- Water levels: upstream depth, tailwater depth
- Material properties: concrete density (2200-2600 kg/m³), water density (950-1050 kg/m³)
- Coefficients: uplift reduction factor, friction coefficient

## Getting Started

1. Open `index.html` in a modern web browser.
2. An internet connection is required (React 18 and Babel are loaded via CDN).
3. Adjust parameters using the input fields or by dragging elements in the visualization.

No build tools or package managers are needed.

## Tech Stack

- React 18 (UMD via CDN)
- Babel standalone (in-browser JSX transpilation)
- SVG for visualization
- Single-file HTML application

## License

See repository for license details.
