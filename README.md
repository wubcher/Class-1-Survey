# Class 1 Survey Data Analysis

## Project Overview
This project analyzes survey responses from 58 students in a graduate-level Advanced Data Analysis course. The analysis demonstrates data cleaning techniques, exploratory data analysis, and variable creation using R programming. This work serves as a practical exercise in handling real-world survey data with common data quality issues.

## Dataset Description
- **Source**: Class 1 student survey
- **Sample Size**: 58 respondents  
- **Variables**: 27 survey questions covering demographics, preferences, academic background, and personal information
- **Data Types**: Mix of character responses (23 variables) and numeric responses (4 variables)

## Files Included
- `class1_survey.csv`: Raw survey dataset (original responses as collected)
- `Class1Survey_cleaned.csv`: Processed dataset with renamed variables and data cleaning applied
- `analysis_code.Rmd`: Complete R Markdown analysis script
- `README.md`: This documentation file

## Key Analysis Components

### Data Cleaning and Preparation
- **Variable renaming**: Converted lengthy question text to concise, analysis-friendly variable names
- **Birthday data cleaning**: 
  - Standardized inconsistent date formats (e.g., "June 2nd", "August 2nd 1997", "15-Nov")
  - Converted text month names to numeric values
  - Handled misspellings and case sensitivity issues
- **Missing data assessment**: Identified and documented incomplete responses

### Variable Creation
- **Birth seasons**: Classified respondents into meteorological seasons (Winter, Spring, Summer, Fall)
- **Astrological signs**: Determined zodiac signs based on birth month and day
- **Numeric conversions**: Transformed character variables to appropriate data types for analysis

### Statistical Analysis
- **Descriptive statistics**: Calculated medians, frequency distributions, and summary statistics
- **Data validation**: Range checks and unusual value detection
- **Cross-tabulations**: Season by month verification tables using `addmargins()`

### Key Findings
- **Birth season distribution**: Spring and Summer tied for most common (16 students each), Winter least common (10 students)
- **Median birth date**: 18th day of June
- **Most common zodiac signs**: Gemini (8 students), Taurus (7 students)
- **Data quality**: Successfully cleaned and standardized 98% of birth date responses

## Technical Skills Demonstrated
- Data import and initial exploration using `sapply()` and `class()`
- Complex data cleaning with `case_when()` and regular expressions
- String manipulation and standardization
- Missing data handling strategies
- Cross-tabulation and frequency analysis
- Conditional variable creation based on multiple criteria
- Data validation and quality assessment

## How to Reproduce This Analysis

### Prerequisites
- R (version 4.0+ recommended)
- RStudio (recommended IDE)
- Required packages: `dplyr`, `stringr`

### Steps
1. **Setup**:
   ```r
   # Install required packages if needed
   install.packages(c("dplyr", "stringr"))
   ```

2. **Download files**:
   - Clone this repository or download all files to a local folder
   - Ensure `class1_survey.csv` is in your working directory

3. **Run analysis**:
   - Open `analysis_code.Rmd` in RStudio
   - Set working directory to the folder containing your files
   - Run all code chunks sequentially or knit the entire document

### Expected Output
- Cleaned dataset with standardized variable names
- Summary tables of variable types and distributions
- Birth season and zodiac sign classifications
- Data quality assessment reports

## Learning Outcomes
This project demonstrates proficiency in:
- Real-world data cleaning challenges
- Survey data analysis techniques
- R programming for data manipulation
- Documentation and reproducible research practices
- Statistical thinking and data validation

## Future Enhancements
- Visualization of birth date distributions
- Analysis of relationships between variables (e.g., favorite season vs. birth season)
- Text analysis of open-ended responses
- Missing data imputation strategies

## Author Information
- **Name**: Yosef Chernet
- **Course**: Advanced Data Analysis
- **Institution**: Washington University in St.Louis
- **Date**: 9/16/2025

## Contact
For questions about this analysis or suggestions for improvements, please contact c.yosef@wustl.edu or create an issue in this repository.

---
*This project was completed as part of coursework in Advanced Data Analysis, focusing on practical application of data cleaning and exploratory analysis techniques in R.*