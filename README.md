# NBA-MVP-Likelihood-Investigator
*Note* -- This is a project for RDM course where I will build the skeleton of my possible future project.


## 1. Project Overview

This project investigates how individual player performance and basic team context
relate to a player’s likelihood of winning the NBA Most Valuable Player (MVP) award
during the regular season. The primary focus is the 2025–2026 NBA season, where
player statistics are updated on a daily basis.

One maintained external dataset is reused and processed to produce cleaned,
analysis-ready datasets:

**P1 – Cleaned NBA Dataset with box scores and Stats (1947-Today)**  
P1 is a cleaned, analysis-ready subset of the original NBA player statistics
source. Each row represents a single player’s performance in a single regular
season game (2025–2026), with consistent identifiers, team information, game
context (home/away, opponent, result), and core box-score metrics (minutes,
points, rebounds, assists, shooting splits, etc.).

P1 is intended as a **demonstration of the type of processed dataset** that the
project aims to produce

The project aims to support transparent, FAIR data practices, reproducibility,
and reuse. All processing steps are documented in Jupyter notebooks and the
data management plan (DMP).

> **Note on originally planned second dataset:**  
> In the DMP a second external dataset was mentioned. However, since the primary dataset
> (R1) is actively maintained and the 2025–2026 season data is uploaded daily,
> the second dataset is *not currently required* and is therefore **not used**
> in this version of the project. It may be integrated in future work if the
> research questions evolve.

---

## 2. Folder Structure

```text
/data/raw/           Partial Original raw datasets (not redistributed; accession
                     information documented in the DMP and in the Information.md file)

/data/processed/     Produced dataset P1 (CSV)

/src/groundwork/     Notebook for data loading, cleaning,
                     and feature engineering (e.g. preprocessing.ipynb)

/src/models/         Notebook for MVP likelihood modelling
                     and forecasting (e.g. forecast.ipynb)
```
## 3. Software Requirements

This project requires the following software environment:

- Python 3.11+
- Jupyter Notebook or JupyterLab
- `ipykernel>=7.1.0`
- `pandas>=2.3.3`
- `numpy>=2.3.5`
- `matplotlib>=3.10.7`
- `scikit-learn>=1.7.2` (for baseline MVP models)
- `nba-api>=1.11.3` (only if the user would like to extend this project by using the additional dataset mentioned in the DMP)

This project uses the **uv** package manager to ensure a fully reproducible
Python environment based on `pyproject.toml`.

To reproduce the environment, install `uv` by:

```bash
pip install uv
```
Then run from the project root:

```
uv sync
```

This command will:

- create a virtual environment (if none exists),
- install all required dependencies from pyproject.toml,
- ensure version-locked, reproducible installations.

## 4. How to Reproduce the Produced Datasets

Look at the information file placed in `data/raw/Information`

### To sum it up:

Download and place the relevant source files from the original dataset (For **P1** recreation) into `data/raw/`:

- `PlayerStatistics.csv`

Open the preprocessing notebook:

`src/groundwork/preprocessing.ipynb`

Run all cells.

The notebook will:

- load and clean the NBA player statistics data → create **P1**
- export it as CSV files into `data/processed/`

## 5. Provenance of Reused Datasets

### R1 – NBA Historical Stats Dataset [1974-2025] (maintained dataset)

- **Source:** Kaggle  
- **URL:** [(https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores?select=Players.csv)]
- **Licence:** MIT License 
- **Accessed on:** 28.11.2025  

**Description**  
Dataset containing player-level statistics and basic team context for the
2025–2026 NBA regular season. The dataset is actively maintained, with new game
data uploaded on a daily basis. It forms the primary basis for all analyses in
this project.

### R2 – Additional dataset mentioned in the DMP (currently unused)

In the original project description and DMP, a second external dataset
(with data regarding the 2025-2026 season) was
originally planned. However:

- R1 is continuously maintained and already provides up-to-date data for
  the 2025–2026 season.  
- For the current research questions and scope, R1 alone is sufficient.

Therefore:

- R2 is **not used** in any of the current preprocessing or modelling workflows.  
- No files from R2 are stored or redistributed in this repository.  

R2 remains documented in the DMP as a potential future extension, should the
analysis require additional variables, longer historical coverage or alternative
performance metrics.

---

## 6. Licensing

- **Produced dataset (P1):** CC BY 4.0  
  You are free to share and adapt the data, provided appropriate credit is
  given to the author and project.

- **Source code (this repository):** MIT License  
  The source code is made available under the MIT License. See the `LICENSE`
  file in the repository for full terms.

- **Reused datasets (R1, and any future R2):**  
  - Not redistributed in this repository.  
  - Only referenced via URLs and accession information.  
  - Users must obtain the original data directly from the respective sources
    and comply with their licences and terms of use.


