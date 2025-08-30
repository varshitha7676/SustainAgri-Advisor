# SustainAgri-Advisor: Crop & Eco‑Fertilizer Recommendation

A simple, self‑contained demo project that recommends crops and eco‑friendly fertilizer plans
from basic soil and weather inputs. Designed for quick upload to GitHub and easy grading.

## Features
- Rule‑based recommendations (no heavy ML needed to run).
- CLI tool: process a CSV of plots and get crop + eco‑fertilizer advice.
- Sample dataset and generated results included.
- Screenshot of sample run in `screenshots/`.
- MIT License.

## Quick Start
```bash
# 1) (Optional) create venv
python -m venv .venv && . .venv/bin/activate  # Windows: .venv\Scripts\activate

# 2) Install (no external deps required)
pip install -r requirements.txt

# 3) Run demo on sample data
python src/app.py --input data/sample_input.csv --output output/results.csv

# 4) See screenshot of expected output in screenshots/output.png
```

## Input format
CSV with columns:
- `plot_id`: string
- `nitrogen`, `phosphorus`, `potassium`: integers (kg/ha)
- `ph`: float (0–14)
- `rainfall_mm`: integer (monthly average)
- `region`: string (for simple monsoon logic)

See `data/sample_input.csv` for an example.

## Output
CSV with recommended columns:
- `recommended_crop`
- `fertilizer_bio`
- `notes`

## Notes
This is a compact educational demo. You can extend the rules or swap in a trained model later.
