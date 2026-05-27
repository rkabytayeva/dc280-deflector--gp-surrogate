# Gaussian process surrogate for dose rate interpolation (DC-280 deflector, 48Ca beam)

This repository contains a Gaussian process (GP) surrogate model trained on FLUKA‑calculated ambient dose equivalent rates for a tungsten electrostatic deflector irradiated by a ⁴⁸Ca beam (6 MeV/u, 1 pμA, 1‑month irradiation). The model provides continuous interpolation with uncertainty estimates for three scenarios:

- **Surface** – dose rate on the deflector front surface (mSv/h)
- **0.5 m, no shield** – dose rate at 0.5 m distance, no additional shielding (μSv/h)
- **0.5 m, 5 mm Pb** – dose rate at 0.5 m with a 5 mm lead shield (μSv/h)

## Training data
The GP was trained on 14 cooling times (0.5, 1, 2, 6, 12, 24, 36, 48, 72, 96, 120, 168, 200, 240 h) calculated with FLUKA (5×10⁸ primary ions per time point, statistical uncertainty <5 %). The data are listed in the Supplementary Material of the associated article.

## Requirements
- Python 3.8+
- numpy, pandas, scikit‑learn, matplotlib, joblib
