# Pymaceuticals, Inc.

![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/d4c42b47-3863-4ba5-b146-e85a48c6da98)

What good is data without a good plot to tell the story?

In this assignment, I will apply what I've learned about Matplotlib to a real-world situation and dataset.

# Background

I've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked me with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked for a top-level summary of the study results.

### Preparing the Data

1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining step.

3. Display the updated number of unique mice IDs.

### Generate Summary Statistics

Create two summary statistics DataFrames:

    * For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This should result in five unique series objects. Combine these objects into a single summary statistics DataFrames.

    * For the second table, use the `agg` method to produce the same summary statistics table by using a single line of code.

### Create Bar Charts and a Pie Charts

1. Generate two bar plots. Both plots should be identical and show the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

    * Create the first bar plot by using Pandas's `DataFrame.plot()` method.

    * Create the second bar plot by using Matplotlib's `pyplot` methods.
  
![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/01060604-a67d-4ef6-8286-7a774f2ebc2d)


2. Generate two pie plots. Both plots should be identical and show the distribution of female or male mice in the study.

    * Create the first pie plot by using both Pandas's `DataFrame.plot()`.

    * Create the second pie plot by using Matplotlib's `pyplot` methods.

![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/c35cb6d3-233c-4dfb-b3d6-82685450f3f8)

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR and determine if there are any potential outliers across all four treatment regimens. Follow these substeps:

    * Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    * Create a list that holds the treatment names, as well as a second, empty list to hold the tumor volume data.

    * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. 

    * Determine outliers by using the upper and lower bounds, and then print the results.
    
2. Using Matplotlib, generate a box plot of the final tumor volume for all four treatment regimens. Highlight any potential outliers in the plot by changing their color and style.

  **Hint**: All four box plots should be within the same figure. Use this [Matplotlib documentation page](https://matplotlib.org/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py) for help with changing the style of the outliers.

![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/e592b9b1-4d06-478f-bcee-88e3f768cc04)


### Create a Line Plot and a Scatter Plot

1. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.


![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/f3b5a258-ddd5-461a-aaf5-30f8306094ac)


![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/b27f383d-f76d-4d33-915f-a01c535b5cd0)


### Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Plot the linear regression model on top of the previous scatter plot.

![image](https://github.com/RaphaelSheikh/pymaceuticals-challenge/assets/166172978/ce54c4f9-7968-47ed-a5fd-4375120d8cfa)

# Analysis

This project saw the analysis of test results involving 249 mice divided in 10 drug treatments, including a placebo/control test regimen based on specific parameters help determine trends, and patterns as well as to draw conclusions that can be used to make informed decisons about anti-cancer medications.

Conclusions drawn from the thorough analyses applied to the complete data from Pymaceuticals' most recent animal study suggests:

* Capomulin and Ramicane reduces the tumor size better.

* There is a positive correlation between mouse weight and average tumor volume with a correlation value of 0.84. As the mouse weight increases, the average tumor volume increases too.

* The bar graph shows that Capomulin and Ramicane had the most number of mice tested.

- - -

## References

* Data generated by Mockaroo, LLC (2022). Realistic Data Generator. (https://www.mockaroo.com/)

* matplotlib.pyplot.legend (https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.legend.html)

* List of named colors (https://matplotlib.org/stable/gallery/color/named_colors.html)

* matplotlib.markers (https://matplotlib.org/stable/api/markers_api.html)

* Boxplots (https://matplotlib.org/stable/gallery/statistics/boxplot_demo.html)

- - -
