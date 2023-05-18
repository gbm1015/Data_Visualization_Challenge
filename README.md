# Data Visualization using Matplotlib Solution: The analysis of Pymaceuticals Inc.'s clinical study for its drug treatment Capomulin 

## Background
Pymaceuticals Inc., a new pharmaceutical company that specializes in anti-cancer medications, began screening for potential treatments for squamous cell carcinoma (SCC) which is a commonly occuring form of skin cancer.

In a recent clinical study, 248 mice that were identified with SCC tumors received a variety of 9 drug treatment regimens and a placebo. The study was conducted using approximately an equal number of female and male mice (49.4% to 50.6%). Over the course of 45 days, the tumor development/growth was observed and measured.

The objective of the clinical study was to observe and compare the performance of Pymaceuticals' drug of interest, Capomulin, against the other treatment regimens.

### Before reading the homework csv data files and coding in Python

1. I created a new repository in GitHub for this project called `Data_Visualization_Challenge`. 

2. Inside the new repository:
    * I cloned the new repository to my computer.
    * I added the following content:
      -	The Jupyter Notebook file called pymaceutical_starter.ipynb, which included the assignment's starter script and instructions.  This is the Jupyter Notebook file that I used to create and run the code for analysis.  I printed several intermediate analysis tables, that were not included in the final pymaceutical_final.ipynb.  These intermediate analysis tables were used to ensure that the code was working correctly and gerenated the anticipated output.
      -	A data folder that contained 2 csv files that I used; Mouse_metadata.csv and Study_results.csv, representing mouse level and clinical study outcome data, respectively. These two datasets were merged on Mouse ID to create a dateset that combined the information about the clinical study results, such as tumor volumes and treatment related information to each mouse.  The merged dataset is at the Mouse ID level (unique Mouse ID row).
      -	The analysis summary is included at the top of the final pymaceutical_final.ipynb Jupyter Notebook.
    * I pushed these changes back to GitHub. 

### Files including data used for analysis, and the analysis report/presentation file

* data/Mouse_metadata.csv - information about each of the 248 mice.  
* data/Study_results.csv - information about the 45 day observations for each of the 248 mice's drug treatments and the treatments' impact on the tumor volume growth.

### Jupyter Notebook files,*.ipynb

* pymaceutical_starter.ipynb - starter script and review of desired format for the assignment's output.  
* pymaceutical_final.ipynb - final script, removing intermediate output tables, that generated the final analysis output. 

## Analysis Steps
In the Pymaceutical assignment we were tasked with using Pandas, Jupyter Notebook, and Matplotlib to analyze the performance of Pymaceuticals' drug of interest, Capomulin, against the other treatment regimens by examining descriptive and graphical statistics.  The following are the analysis steps:

### 1) Preparing the Data
  * Ran the provided package dependency and data imports, and then merged the mouse_metadata and study_results DataFrames into a single DataFrame.
  * Displayed the number of unique mice IDs in the data, and then checked for any mouse ID with duplicate time points. 
  * Displayed the data associated with that mouse ID, and then created a new DataFrame where this duplicated data was removed. Useed this cleaned DataFrame for the
    remaining steps.
  * Displayed the updated number of unique mice IDs.
  
### 2) Generated Summary Statistics
  * Created a DataFrame of summary statistics. The summary statistics included:
    - A row for each drug regimen. These regimen names were contained in the index column.
    - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.
### 3) Created Bar and Pie Charts.  
   * Generated two bar charts that were identical and showed the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.
     - The first bar chart was created with the Pandas DataFrame.plot() method. 
     - The second bar chart was created with Matplotlib's pyplot methods.
   * Generated two pie charts. Both charts were identical and showed the distribution of female versus male mice in the study.
     - The first pie chart was created with the Pandas DataFrame.plot() method. 
     - The second pie chart was created with Matplotlib's pyplot methods.
### 4) Calculated Quartiles, looked for any outliers, and created a Box Plot.
   * Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. 
   * Calculated the quartiles and IQR, and determined if there were any potential outliers across all four treatment regimens, as follows: 
      - Created a grouped DataFrame that showed the last (greatest) time point for each mouse and merged this grouped DataFrame with the original cleaned DataFrame.
      - Created a list that held the treatment names as well as a second, empty list to hold the tumor volume data.
      - Looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Then appended the resulting final tumor 
        volume for each drug to the empty list.
      - Determineed outliers by using the upper and lower bounds, and then printed the results.
   * Using Matplotlib, generated a box plot that showed the distribution of the final tumor volume for all the mice in each treatment group. Then highlight any potential
     outliers in the plot by changing their color and style.
### 5)  Created a Line Plot and a Scatter Plot
    * Selected a single mouse (mouse ID l509) that was treated with Capomulin, and generated a line plot of tumor volume versus time point for that mouse.
    * Generateed a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.
### 6)  Calculated Correlation and Linear Regression Model and Line
    * Calculateed the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
    * Plotted the linear regression model on top of the previous scatter plot.

## References
* Data for the 2 datasets were generated by edX Boot Camps LLC, and are intended for educational purposes only.
