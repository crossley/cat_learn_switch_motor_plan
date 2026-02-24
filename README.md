# Category Learning During Task Switching (Monorepo)

This repository contains two closely related projects:

- `switch_motor_plan_1/`: original study (experiment, data, analyses, manuscript materials)
- `switch_motor_plan_2/`: follow-up study with related experiment/analysis code

## Layout

- `LICENSE`: repository license
- `switch_motor_plan_1/README.md`: study 1 details and usage
- `switch_motor_plan_2/README.md`: study 2 details and usage

## Running Code

Most scripts in both studies use relative paths like `../data` and `../images`.
Run them from each study's `code/` directory, for example:

```bash
cd switch_motor_plan_1/code
python inspect_results_dbm.py
```

or

```bash
cd switch_motor_plan_2/code
python run_exp.py
```
