### P1 – Cleaned NBA Player Game Statistics (2025–2026)

#### 1. Description

P1 is a cleaned subset of the original NBA player statistics dataset.
Each row corresponds to a single player’s performance in a single NBA game
during the 2025–2026 regular season.

The dataset provides a sample of what a tidied, analysis ready dataset could be if it was actually developed.

#### 2. Variables

*(This table reflects the columns in `Processed_Stat.csv`.)*

| Column                  | Description                                                               |
|-------------------------|---------------------------------------------------------------------------|
| `Row_ID`                | Row index from the original export (technical column, no analytical role)|
| `firstName`             | Player’s first name                                                       |
| `lastName`              | Player’s last name                                                        |
| `personId`              | Unique player identifier (numeric; provided by the data source)          |
| `gameId`                | Unique game identifier                                                    |
| `gameDateTimeEst`       | Game date and tip-off time in Eastern Time (`YYYY-MM-DD HH:MM:SS`)       |
| `playerteamCity`        | City of the player’s team                                                 |
| `playerteamName`        | Name of the player’s team                                                 |
| `opponentteamCity`      | City of the opponent team                                                 |
| `opponentteamName`      | Name of the opponent team                                                 |
| `gameType`              | Type of game (e.g. regular season)                                       |
| `gameLabel`             | Human-readable game label (e.g. “Suns @ Kings”)                          |
| `gameSubLabel`          | Additional game label / subtitle (if provided by the data source)        |
| `seriesGameNumber`      | Game number in a series (mainly relevant for playoffs; may be empty)     |
| `win`                   | Indicator if the player’s team won the game                              |
| `home`                  | Indicator if the player’s team played at home                            |
| `numMinutes`            | Minutes played by the player in the game                                 |
| `points`                | Total points scored                                                       |
| `assists`               | Total assists                                                             |
| `blocks`                | Total blocks                                                              |
| `steals`                | Total steals                                                              |
| `fieldGoalsAttempted`   | Field goals attempted                                                     |
| `fieldGoalsMade`        | Field goals made                                                          |
| `fieldGoalsPercentage`  | Field goal percentage (0–1 or 0–100, depending on the source definition) |
| `threePointersAttempted`| Three-point field goals attempted                                         |
| `threePointersMade`     | Three-point field goals made                                              |
| `threePointersPercentage`| Three-point field goal percentage                                        |
| `freeThrowsAttempted`   | Free throws attempted                                                     |
| `freeThrowsMade`        | Free throws made                                                          |
| `freeThrowsPercentage`  | Free throw percentage                                                     |
| `reboundsDefensive`     | Defensive rebounds                                                        |
| `reboundsOffensive`     | Offensive rebounds                                                        |
| `reboundsTotal`         | Total rebounds (defensive + offensive)                                   |
| `foulsPersonal`         | Personal fouls committed                                                  |
| `turnovers`             | Turnovers                                                                 |
| `plusMinusPoints`       | Plus/minus value for the player in that game                             |


#### 3. Provenance

Derived from the reused dataset:

**R1 – NBA Player Statistics 2025–2026**

- Source: Kaggle
- URL: [(https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores?select=Players.csv)]
- Accessed: 28.11.2025 
- Licence: MIT License 

P1 is generated from R1 using scripted preprocessing (no manual editing of
individual rows).

#### 4. Preprocessing Steps

Key steps to create P1:

- Selected the player game statistics.  
- Preserved core game, team, and box-score columns as listed above.  
- Filtered for the first 3 rows of the original dataset

All steps are documented in:

- `src/groundwork/preprocessing.ipynb`

#### 5. File Format

- Format: CSV (comma-separated values)  
- Encoding: UTF-8  
- Example filename: `Processed_Stat.csv`  

#### 6. Licence

The P1 dataset is published under the **Creative Commons Attribution 4.0 (CC BY 4.0)** licence.

Users are free to share and adapt the data, provided appropriate credit is given
to the author and this project, and any changes are indicated.
