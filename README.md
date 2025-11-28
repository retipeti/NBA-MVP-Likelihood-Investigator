# NBA-MVP-Likelihood-Investigator
*Note* -- This is a project for RDM course where I will build the skeleton of my possible future project.


## 1. Project Overview

This project investigates how individual player performance and basic team context
relate to a player’s likelihood of winning the NBA Most Valuable Player (MVP) award
during the regular season. The primary focus is the 2025–2026 NBA season, where
player statistics are updated on a daily basis.

One maintained external dataset is reused and processed to produce cleaned,
analysis-ready datasets:

**P1 – NBA Dataset with box scores and Stats (1947-Today) **  
A historical dataset that contains player and team box scores and statistics for every NBA game from 1947 to the present.

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
                     information documented in the DMP)

/data/processed/     Produced datasets P1 and P2 (CSV)

/src/groundwork/     Notebook for data loading, cleaning,
                     and feature engineering (e.g. preprocessing.ipynb)

/src/models/         Notebook for MVP likelihood modelling
                     and forecasting (e.g. forecast.ipynb)


## 3. Software requirements
