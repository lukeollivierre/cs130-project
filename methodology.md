# Methodology

### Data Source
* **Tennis Database:** The primary data for this analysis was sourced from [Tennis Professionals](https://www.kaggle.com/datasets/gmadevs/atp-matches-dataset) where the two CSV files: `atp_matches_2005.csv` and `atp_matches_2008.csv`were downloaded. These files contain match-level statistics for the ATP tour, including player IDs, rankings, scores, match duration, and tournament dates.

### Data Preparation/Cleaning
* **File Loading & Parsing:** Data was loaded by reading the CSV files line-by-line using Python's built-in file handling (without pandas). Rows were split by commas to extract individual fields.
* **Filtering:** The dataset was filtered to include only matches where:
    * The `surface` column was equal to "Clay".
    * Rafael Nadal (Player ID `104745`) was either the `winner_id` or the `loser_id`.
* **Sorting:** The raw data in the CSV files was not strictly chronological. A "helper list" approach was used to sort the matches based on the `tourney_date` column to ensure accurate timeline analysis.
* **Data Type Conversion:** Numeric fields such as `minutes`, `winner_rank`, and `loser_rank` were converted from strings to integers or floats. Empty strings in these fields were handled by skipping the conversion to avoid errors.
* **Score Parsing:** The `score` string (e.g., "6-3 4-6 6-4") was parsed to count specific metrics like "Sets Lost." Tie-break representations (e.g., "7-6(4)") were cleaned to standard game scores ("7-6") for calculation.

### Assumptions
* **Chronological Order:** It was assumed that the `tourney_date` (which typically indicates the start of the tournament) is sufficient for ordering matches to calculate win streaks. While matches within a tournament occur on different days, sorting by tournament date groups them effectively enough for season-long streak analysis.
* **Opponent Rank as Quality:** It was assumed that a lower numerical rank (e.g., Rank 1 vs. Rank 100) equates to a "higher quality" opponent.
* **Streak Logic:** A "Win Streak" was defined as continuous wins in the sorted list of matches. Any loss in the dataset immediately resets the streak count to zero.
* **Tournament Titles:** It was assumed that a match with the round labeled "F" (Final) where Nadal was the winner constitutes a tournament title.

### Limitations
* **Date Resolution:** The dataset provides dates per tournament, not per match. This means the specific day-to-day timeline within a single week is inferred rather than explicit.
* **Missing Data:** Some matches had missing values for match duration (`minutes`) or opponent rankings. These instances were excluded from average calculations, which may slightly impact the precision of the "Average Duration" and "Average Rank" metrics.
* **Retirements/Walkovers:** The logic for counting "sets lost" relies on completed set scores. Matches ending in retirement (`RET`) or walkover (`W/O`) might not fully reflect the competitive nature of that specific match in the "sets lost" metric.

***