# Neuronal Bursting Energy Analysis

Authors: Sayam Agarwal (2024201025), Vivek Kumar Chandan (2024201032)

This repository contains code and experiments for analyzing the metabolic energy cost of neuronal bursting. It includes neuron models, analysis modules, visualization utilities, and example experiments.

**Project layout**
- `src/` : core Python packages (models, analysis, visualization, optimization)
- `experiments/` : example scripts (01..08) demonstrating analyses and pipelines
- `data/` : input and output data, processed results, and figures
- `run_pipeline.py` : example top-level runner for end-to-end pipeline
- `requirements.txt` : Python dependencies
- `test.py` : simple project-level test harness

**Requirements & environment**
- Python 3.8+ recommended (project was developed with 3.8)
- Create and activate a virtual environment (PowerShell on Windows):

```powershell
# create venv (if not present)
python -m venv env
# activate in PowerShell
.\\env\\Scripts\\Activate.ps1
```

- Install dependencies:

```powershell
pip install -r requirements.txt
```

**Quick start**
- Run the top-level pipeline (example):

```powershell
python run_pipeline.py
```

- Run an experiment script directly (examples are in `experiments/`):

```powershell
python experiments\\01_validate_basic_hh.py
python experiments\\03_frequency_sweep.py
```

- Run the simple test harness:

```powershell
python test.py
# or, if you use pytest and tests are available
pytest
```

**Data and outputs**
- Processed results and CSVs are under `data/processed/`.
- Generated figures are saved under `data/figures/` in subfolders like `novel_analysis/` and `validation/`.

**Importing `src/` modules**
- Scripts in this repo import `src` modules using relative or sys.path manipulation. If you run scripts from the project root, Python should find `src` if the current working directory is the project root. If you encounter import errors, run from the repository root or add the root to `PYTHONPATH`:

```powershell
$env:PYTHONPATH = "$PWD"
python run_pipeline.py
```

**Development notes & tips**
- Use the `experiments/` scripts as examples for how to call analyzers and plotters.
- If long-running simulations are used, consider running experiments on a machine with more CPU or by reducing simulation time `t_max` for development.

**License & credits**
- Add your chosen license here if you want the repo licensed.
- Authors: Sayam Agarwal and Vivek Kumar Chandan

**Need help?**
- I can:
  - run the tests or an experiment for you,
  - convert a script into a runnable module or wrap existing experiment code into a runner,
  - or update the README with any additional details you want included.

<end of README>
