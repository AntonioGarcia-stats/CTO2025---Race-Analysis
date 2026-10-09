# Conquer the Overlook 2025 Race Analysis

This project analysis results from the 2025 Conquer the Overlook 5k using Python.

## Project Overview
This project analyzes results from the 2025 Conquer the Overlook race using Python. 
The original race results were provided in PDF format and required extraction, cleaning, restructuring, and validation before statistical analysis.
The project demonstrates an end to end analytical workflow, from converting unstructured race result tables into an analysis ready dataset to examining finish time patterns across age groups and gender.

## Research Question
** How do finish times vary across age groups and gender among finishers of the 2025 Conquer the Overlook race?**
Since the dataset contains the full set of recorded finishers for this race, the analysis focuses primarily on population level descriptive statistics, effect sizes, regression modeling, and observed differences rather than relying only on inferential p - values.

## Data
The original dataset was obtained from the official race results website: https://runsignup.com/Race/CA/CulverCity/ConquertheOverlook5K
Variables used in the analysis include:

- 'OVR' - Overall finishing rank
- 'NAME' - Runner name
- 'HOMETOWN' - Runner hometown
- 'DIVISION' - Age and gender division
- 'TIME' - Recorded finish time
- 'PACE' - Recorded race pace
- 'GENDER_RANK' - Rank within gender
- 'DIV_RANK' - Rank within division
- 'BIB' - Runner bib number
- 'GENDER' - Gender extracted from division
- 'AGE GROUP' - Age category extracted from division
- 'TIME_MINUTES' - Finish times converted to numeric minutes

## Data Cleaning
The raw PDF results were processed using Python and 'pdfplumber'.
The cleaning workflow included:

- extracting tables from all PDF pages
- assigning standardized column names
- converting rank and bib variables to numeric format
- separating gender and age group from the original division field
- standardizing age group labels
- converting finish time into numeric minutes
- standardizing hometown text
- correcting identified hometown spelling inconsistencies
- checking missing values and duplicate bib numbers
- exporting the final analysis ready dataset as CSV

## Exploratory and Descriptive Analysis
The statistical analysis includes:

- runner frequency by hometown
- runner frequency by age group and gender
- overall finish time summary statistics
- finish time summaries by age group
- finish time summaries by gender
- finish time summaries by age group and gender
- boxplots of finish time distributions with group sample sizes

Descriptive measures include:

- sample size
- mean
- standard deviation
- median
- minimum
- first quartile
- third quartile
- maximum
- interquartile range

## Effect Sizes
Effect sizes were used to quantify the magnitude of observed differences

## Cohen's d
Cohen's d was calculated to measure the standardized difference in mean finish time between male and female runners.

## Eta-Squared
Eta-Squared was calculated to quantify the proportion of total finish time variation associated with age group differences.

## Regression Analysis
An Ordinary Least Squares regression model was used to examine the relationship between finish time, age group, and gender.

The final model is:
'''text
TIME_MINUTES ~ AGE_GROUP + GENDER

## Future Extensions

Potential extensions of this project include:
- comparing race results across multiple years
- examining changes in participation demographics
- comparing finish time distributions between years
- modeling year to year changes in performance


    
