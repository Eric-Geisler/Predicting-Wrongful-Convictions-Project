# Predicting-Wrongful-Convictions-Project
Can we predict the intensity of wrongful convictions in the United States justice system?

OVERVIEW:

Goal: predicting sentence received and time spent in prison of people who have been wrongfully convicted using:

3 demographic inputs (State, Race, Sex)
6 contributing factors (official misconduct, false forensic analysis, false confessions, false accusations, mistaken eyewitness identification, inadequate defense)

DATA:

The data for this research comes from The National Registry of Exonerations. The raw copy can be accessed through the WrongfulConvictions.csv file.

NOTEBOOK DETAILS:

The necessary packages to run this code are Pandas, Numpy, TensorFlow, MatPlotLib, SKLearn, and Math. With these pacakages installed, anyone should be able to run all.

The Notebook is split into five sections denoted by headings.

All points are futher explained via comments in the notebook.

1) Reading Data

  -this section imports the necessary pacakages and reads the above data as a csv

  -note: have to change the file pathway

2) Data Cleaning and Engineering

  -new columns for all inputs are created with numerical values

  -creation of two labels for time spent in prison and sentence length

  -note: specific columns within the factor of official misconduct were transformed to numerical values; these variables were not used in the model but were transformed for future use

  -note: creation of the sentence length label required bucketization of the original column for sentence length

3) Variable Visualizations (Time Spent In Prison)

  -boxplots showing the distribution of time spent in prison across levels of the input variables

4) Variable Visualizations (Sentence Category Number)

  -boxplots showing the distribution of sentence category number across levels of the input variables

5) Feed Forward Neural Network

  -the model should run as is

  -metrics/visualizations for validation data and testing data are included
