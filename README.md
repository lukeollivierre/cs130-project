# Nadal Clay Dominance: 2005 vs. 2008

This project was completed for my CS-130 class. It uses Python to analyze Rafael Nadal's clay-court performance in two important seasons of his career: his 2005 breakout year and his 2008 peak season.

The project was designed to showcase Python programming skills through data loading, cleaning, filtering, analysis, and visualization. Instead of only writing about tennis, I used real ATP match data to answer a specific research question with code and evidence.

The main question behind the project is:

**Was Nadal's 2005 clay season better than his 2008 clay season, or was 2008 more impressive because of the quality of competition he faced?**

## Project Overview

Rafael Nadal is widely known as one of the greatest clay-court tennis players of all time. This project compares his 2005 and 2008 clay seasons using ATP match data. The analysis looks beyond simple win totals and compares both the amount of success Nadal had and the difficulty of the matches he played.

The project focuses on metrics such as:

- Total clay-court matches played
- Clay-court wins
- Tournament titles
- Win streaks
- Opponent rankings
- Average match duration
- Sets lost

The goal is to determine whether 2005 was stronger because Nadal played and won more matches, or whether 2008 was stronger because he faced tougher opponents and performed at a higher level.

## Key Findings

The analysis shows that Nadal's 2005 season was dominant in terms of volume. He played more clay matches, won more titles, and built a longer winning streak. At only 19 years old, he had an extremely active and successful clay season.

However, the 2008 season appears stronger when looking at opponent quality. Nadal faced higher-ranked players more consistently in 2008, and his matches were slightly longer on average. This suggests that even though he played fewer matches, the level of competition was tougher.

Overall, the project concludes that:

- **2005 was better for total dominance and volume.**
- **2008 was better for peak performance and opponent quality.**

## Repository Contents

- `analysis.ipynb` - Jupyter Notebook containing the Python data analysis and visualizations.
- `article.md` - Written article explaining the project, results, charts, and conclusion.
- `methodology.md` - Explanation of the data source, cleaning process, assumptions, and limitations.
- `atp_matches_2005.csv` - ATP match data for the 2005 season.
- `atp_matches_2008.csv` - ATP match data for the 2008 season.
- `images/` - Folder containing the charts used in the article.

## Python Skills Demonstrated

This project demonstrates several Python skills learned and practiced in CS-130:

- Reading and working with CSV data files
- Using file handling to load match data
- Filtering large datasets based on specific conditions
- Cleaning and converting data types from strings to numbers
- Handling missing or incomplete values
- Sorting data chronologically using tournament dates
- Using conditional logic to identify Nadal's wins, losses, opponents, and match results
- Creating custom calculations for statistics such as win streaks, titles, sets lost, average opponent ranking, and average match duration
- Parsing tennis score strings to calculate match-based metrics
- Organizing analysis inside a Jupyter Notebook
- Creating charts and visualizations to communicate results clearly
- Writing a data-based conclusion using evidence from the analysis

## Data Source

The data used in this project comes from the ATP matches dataset on Kaggle. The CSV files include match-level information such as players, rankings, scores, match duration, tournament dates, and court surface.

For this project, the data was filtered to include only clay-court matches involving Rafael Nadal during the 2005 and 2008 seasons.

## How Python Was Used

The analysis was completed in Python using a Jupyter Notebook. Python was used to load the ATP match CSV files, clean the data, filter the matches, calculate statistics, and generate visualizations.

The project filtered matches based on:

- Surface: clay
- Player: Rafael Nadal
- Seasons: 2005 and 2008

After filtering the data, Python was used to compare both seasons through calculated statistics and charts. Opponent ranking was used as a measure of competition quality, with lower ranking numbers representing stronger opponents.

Some of the Python logic included:

- Checking whether Nadal was the winner or loser in each match
- Finding the opponent's ranking depending on whether Nadal won or lost
- Counting titles by identifying final-round wins
- Tracking win streaks by looping through matches in chronological order
- Calculating averages for match duration and opponent rank
- Cleaning score strings so sets lost could be counted more accurately

## Methodology

The raw ATP data was prepared by reading the 2005 and 2008 CSV files, filtering for Nadal's clay-court matches, and sorting the results by date. Numeric fields such as match duration and ranking were converted into usable number values so calculations could be performed.

Once the data was cleaned, the notebook calculated summary statistics and produced charts comparing Nadal's 2005 and 2008 clay seasons. These results were then explained in `article.md`, while `methodology.md` documents the data source, assumptions, and limitations.

## Limitations

Some limitations of the project include:

- The dataset provides tournament dates, not exact match dates.
- Some matches have missing values for match duration or opponent ranking.
- Retirements and walkovers may affect score-based calculations.
- Opponent ranking is useful, but it does not capture every part of match difficulty.

## Conclusion

This project shows that the answer depends on how "better" is defined. Nadal's 2005 clay season was more impressive statistically because of the number of matches, wins, titles, and his long winning streak. His 2008 season, however, was more impressive in terms of quality because he faced stronger opponents and still dominated.

For a CS-130 data analysis project, this comparison demonstrates how Python can be used to turn raw data into a clear argument. The project shows skills in data cleaning, loops, conditionals, calculations, visualization, and evidence-based writing.