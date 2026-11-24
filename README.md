# Thermal Studio

A lightweight, no-build browser workbench for exploring first-pass thermal management trade-offs in CPUs, GPUs, batteries, and rack-scale systems.

## Run locally

Open `index.html` in a modern browser. The app has no build step or runtime dependencies.

## What it models

- Steady-state junction temperature from a simplified effective thermal resistance.
- Air, single-phase liquid, and indicative two-phase architecture comparisons.
- Minimum estimated airflow / coolant flow to meet a user-defined temperature limit.
- Estimated pressure drop and fan / pump power from simplified flow correlations.
- Device presets and an inline temperature-vs-flow comparison chart.

## Deploy

The included GitHub Actions workflow publishes the root of `main` to GitHub Pages. Once Pages is enabled for GitHub Actions, the site is available at `https://raghav1822.github.io/electronics-thermal-simulator/`.

## Engineering note

This is a screening calculator, not a validated design tool. Thermal resistance and hydraulic coefficients are illustrative assumptions, and the two-phase mode is not a boiling-flow solver. Validate all assumptions against component and loop data, then use appropriate simulation and physical testing before making hardware decisions.
