# Students Performance Analysis

This repository contains a Jupyter Notebook (`students_performance_analysis.ipynb`) that explores the factors influencing student performance using a dataset containing various student attributes and their academic results. The primary goal of this analysis is to identify which of these factors have a significant impact on a student's Grade Point Average (GPA).

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Analysis Steps](#analysis-steps)
- [Key Findings](#key-findings)
- [Requirements](#requirements)
- [How to Run the Notebook](#how-to-run-the-notebook)
- [Conclusion](#conclusion)
- [License](#license)

## Project Overview

This project delves into a student performance dataset to understand the relationships between various student characteristics and their academic achievement as measured by GPA. The analysis includes data loading, cleaning, exploratory data analysis (EDA), statistical testing, and regression modeling to identify key predictors of GPA.

## Dataset

The dataset used in this analysis is `Students_Performance.csv`. It includes columns such as:

- Age
- Grade
- Gender
- Race
- SES Quartile (Socioeconomic Status)
- Parental Education
- School Type
- Locale
- Test Scores (Math, Reading, Science)
- GPA
- Attendance Rate
- Study Hours
- Internet Access
- Extracurricular Activities
- Part-Time Job
- Parent Support
- Romantic Relationship
- Free Time
- Go Out

## Analysis Steps

The notebook follows a structured approach:

1.  **Data Loading and Overview**: Loading the dataset and performing initial checks (`.info()`, `.describe()`).
2.  **Data Cleaning and Preprocessing**: Creating a categorical 'GPA_Class' column based on GPA ranges.
3.  **Exploratory Data Analysis (EDA)**:
    *   Visualizing the distribution of categorical and numerical features.
    *   Examining the relationship between categorical features and 'GPA_Class' using Chi-squared tests and proportional distributions.
    *   Analyzing the correlation between numerical features using a heatmap.
    *   Visualizing the relationships between GPA and key numerical factors (Test Scores, Attendance Rate, Study Hours).
    *   Investigating outliers in 'Study Hours' and their characteristics.
4.  **Statistical Analysis**:
    *   Calculating confidence intervals for mean 'Attendance Rate' and 'Study Hours' for students with "Excellent" GPA.
    *   Performing independent samples t-tests to compare 'Attendance Rate' and 'Study Hours' between "Excellent" and "Very Good" GPA groups.
5.  **Regression Modeling**:
    *   Building a linear regression model to predict GPA based on 'Total Test Score', 'Study Hours', and 'Attendance Rate'.
    *   Evaluating the model's performance using R-squared, MSE, and RMSE.

## Key Findings

*   Numerical factors such as Total Test Score, Attendance Rate, and Study Hours show positive correlations with GPA.
*   Total Test Score was identified as a highly statistically significant predictor of GPA in the linear regression model.
*   While Chi-squared tests on categorical features and 'GPA_Class' did not show strong statistical dependencies, visual inspection suggested some subtle trends related to Parental Education, Internet Access, and Extracurricular activities.
*   Students with "Excellent" and "Very Good" GPAs showed statistically significant differences in their mean Attendance Rates and Study Hours.
*   The linear regression model explained approximately 58.4% of the variance in GPA using Total Test Score, Study Hours, and Attendance Rate.

## Sample Visualizations

**1. Distribution of GPA**
![GPA Distribution]("C:\Files\Projects\EDA\outputs\figures\Distribution of GPA.png")

**2. Correlation Heatmap**
![Correlation Heatmap]("C:\Files\Projects\EDA\outputs\figures\Correlation Heatmap of Numerical Features.png")

**3. GPA vs Study Hours and Attendance Rate**
![GPA vs Study Hours and Attendance Rate]("C:\Files\Projects\EDA\outputs\figures\GPA by Attendance Rate and Study Hours.png")

## Requirements

The notebook requires the following libraries:

*   pandas
*   numpy
*   matplotlib
*   seaborn
*   scipy
*   statsmodels

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.