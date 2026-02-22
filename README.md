# Category Learning During Task Switching

This repository contains experiment code, participant data, analysis scripts, and manuscript materials for a study on motor demands in procedural category learning under random trial-by-trial task switching.

## Project Summary
The project tests whether learning during task switching is better explained by:
- motor-goal mappings, or
- motor-effector-specific mappings.

Participants switch between two categorization subtasks (square vs diamond context cues) while learning information-integration category structures. Conditions differ in whether stimulus-response mappings are congruent or incongruent across subtasks.

## Repository Structure
- `code/`: experiment and analysis scripts
- `data/`: trial-level participant CSV files
- `dbm_fits/`: decision-bound model fit outputs
- `figures/`: manuscript figures and assets
- `images/`, `img/`: cue/stimulus images and related assets
- `write/`: LaTeX manuscripts, bibliography, and build files

## Main Scripts
- `code/run_exp.py`: run the task-switching experiment and write a participant CSV to `data/`
- `code/inspect_results_dbm.py`: primary analysis pipeline used to fit decision-bound models and generate main figures/statistics
- `code/inspect_results.py`: earlier exploratory analysis script
- `write/main_GA.tex`: primary manuscript source
- `write/main.tex`: alternate/extended manuscript draft

## Environment
Recommended: Python 3.10+ in a virtual environment.

Install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy pandas scipy matplotlib seaborn pygame pingouin statsmodels patsy
```

## Running Analyses
Important: scripts use relative paths like `../data`, so run from the `code/` directory.

```bash
cd code
python inspect_results_dbm.py
```

This will load participant data, fit decision-bound models (if `../dbm_fits/dbm_results.csv` is missing), and generate key figures in `../figures/`.

## Running the Experiment
Set the participant ID in `code/run_exp.py` (`subject = ...`) before running.

```bash
cd code
python run_exp.py
```

Output is written to `data/sub_<subject>_data.csv`.

## Building Manuscript PDFs
From `write/`:

```bash
cd write
make
```

Current `Makefile` compiles `cover_letter.tex` and `main.tex`.

## Notes
- Existing data appear to include 90 analyzed participants (with one exclusion noted in manuscript text).
- `data/` and `figures/` are currently versioned as part of the research record.

## License
This repository is licensed under the Creative Commons Attribution 4.0 International License (`CC BY 4.0`).

You are free to share and adapt the materials, including code and data, provided attribution is given.

## Citation
If you use any part of this repository, please cite the associated manuscript in `write/main_GA.tex` and bibliography in `write/citations.bib`.
