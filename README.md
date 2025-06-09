# My Python Scripts

Collection of python scripts,  noteboos and mini projects.

## Directory Structure

```plaintext
my-project/
│
├── notebooks/              # Jupyter notebooks for EDA, experiments, and demos
│   ├── 01_data_cleaning.ipynb
│   └── 02_model_training.ipynb
│
├── src/                    # Reusable source code (modularized)
│   ├── data/
│   │   └── loader.py       # Functions for loading/cleaning data
│   ├── models/
│   │   └── trainer.py      # Model training and evaluation code
│   └── utils/
│       └── helpers.py      # Helper functions and utilities
│
├── scripts/                # One-off or batch scripts
│   ├── preprocess_data.py  # CLI or automation script for preprocessing
│   └── train_model.py      # CLI or automation script for training
│
├── tests/                  # Unit tests for the src modules
│   ├── test_loader.py
│   └── test_trainer.py
│
├── data/                   # Sample dataset (avoid large/raw data here)
│   └── sample.csv
│
├── .gitignore              # Standard gitignore file
├── README.md               # This file
├── requirements.txt        # Python dependencies (pip)
└── pyproject.toml          # Optional: modern build system configuration
```

## Notebooks

Place notebooks under `notebooks/`. These should be for:
- Exploratory Data Analysis (EDA)
- Experimental model runs
- Reports or demos

> Reuse logic from `src/` — avoid writing all code directly in notebooks.

## 🛠️ Scripts

Scripts in `scripts/` are for running specific actions:
- Can be used for automation
- Should import and use code from `src/`
- Can be run from the command line

Example:
```bash
python scripts/train_model.py
```

## src/

This is your Python package. It should contain:
- All reusable business logic
- Clean, testable functions
- Modular code, grouped by domain (e.g., `data`, `models`, `utils`)

Use `__init__.py` to make subfolders importable as modules.

## Tests

Tests live in `tests/` and should mirror the structure of `src/`.

Use `pytest` to run tests:
```bash
pytest tests/
```

## Environment Setup

1. Clone the repo
2. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```

**Author:** Nathan Zwelibanzi Khupe

