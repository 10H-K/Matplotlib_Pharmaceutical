# Utilizing Pandas, Matplotlib, and SciPy to Analyze the Treatment of Squamous Cell Carcinoma (SCC) in Mice

## Overview ##

The goal of this project is to assist Pymaceuticals, Inc., a pharmaceutical company specializing in anti-cancer medications, in evaluating the effectiveness of its developed drug, Capomulin, compared to other treatment regimens for Squamous Cell Carcinoma (SCC). Using the complete data from an animal study involving 249 mice diagnosed with SCC tumors, the project analyzes the efficacy of various drug regimens administered over a 45-day period. Tumor development and response to treatment are tracked and evaluated. The created Jupyter Notebook presents a comprehensive summary of the study's findings.

## Process ##

A) Preparation of Study Data:
  1. Importation of dependencies (Pandas, Matplotlib and SciPy)
  2. Setting file path to target csv files (mouse metadata and study results)
  3. Reading both csv files, storing into Pandas DataFrames
  4. Combination of DataFrames into single DataFrame
  5. Displaying number of unique mice IDs in combined DataFrame
  6. Using columns "Mouse ID" & "Timepoint" to create DataFrame with duplicate mouse data
  7. Identifying duplicate mouse by ID number
  8. Displaying complete data associated with duplicate mouse
  9. Creating new DataFrame where all data associated with duplicate mouse is removed
  10. Getting concise summary of newly cleaned DataFrame, including information about its structure and contents
  11. Displaying updated number of unique mice IDs in newly cleaned DataFrame

B) Generation of Summary Statistics:
  1. Summary statistics calculation of tumor volume for each treatment regimen
      - mean, median, variance, standard deviation, and standard error
  2. Creation and formatting of DataFrame displaying summary statistics

C) Creation of Bar Charts and Pie Charts:
  1. Generation of two identical bar charts showing total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study
      - Creation of first bar chart with Pandas DataFrame.plot() method
      - Creation of second bar chart with Matplotlib pyplot method

![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/c19f6f40-62e6-4d5b-8c8d-92e7d57fe2a7)
![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/94601b1f-603b-49e5-8049-c327602ec3ca)
    
  2. Generation of two identical pie charts showing distribution of female versus male mice in the study
      - Creation of first pie chart with Pandas DataFrame.plot() method
      - Creation of second pie chart with Matplotlib pyplot method

![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/db942605-e0d6-4a39-ac0f-c646bec042fc)
![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/6c250f93-6ce0-4469-aeeb-b7ee1bf62bee)

D) Calculation of Quartiles, Finding Outliers, and Creation of Box Plot:
  1. Creation of new DataFrame based on the last timepoint of each mouse across four of the most promising treatment regimens: Capomulin, Ceftamin, Infubinol, and Ramicane
       - Utilizing the three methods .isin(), .drop_duplicates(), and .sort_values() achieves this result in a concise manner
  2. Calculation of quartiles, interquartile range, median, lower bound, upper bound, and potential/actual outliers across all four treatment regimens
  3. Generating box plot showing distribution of final tumor volume for all mice in each treatment group
       - Potential outliers are highlighted in plot through changed color and style

![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/4a29b644-e508-4bfb-9f30-929859c7ccd9)

E) Creation of Line Plot and Scatter Plot:
  1. Selecting single mouse treated with Capomulin and generating line plot of tumor volume versus time point for that mouse
  2. Generating scatter plot of mouse weight versus average observed tumor volume for entire Capomulin treatment regimen mice

![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/4ca5e066-f208-409a-9f9a-613411e8e3c0)
![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/57cc697e-96e1-4bcc-aade-c3679372690d)

F) Calculation of Correlation and Regression:
  1. Calculation of Pearson correlation coefficient, coefficient of determination, and linear regression model between mouse weight and average observed tumor volume for entire Capomulin treatment regimen mice
  2. Generating plot of linear regression model on top of the previously generated scatter plot

![output](https://github.com/10H-K/Matplotlib_Pharmaceutical/assets/152930492/91086c52-6e47-48d5-8eca-768201265222)

