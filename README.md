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

## 1) Reading Data
- Imports the necessary packages and reads the dataset as a CSV.  
- **Note:** Update the file path before running.

---

## 2) Data Cleaning and Engineering
- New columns for all inputs are created with numerical values.  
- Creation of two labels:
  - **Time spent in prison**
  - **Sentence length**  
- **Note:** Specific columns within the factor of *official misconduct* were transformed into numerical values. These variables were not used in the model but prepared for future use.  
- **Note:** Creation of the sentence length label required bucketization of the original column.

---

## 3) Variable Visualizations (Time Spent in Prison)
- Boxplots showing the distribution of time spent in prison across levels of the input variables.

---

## 4) Variable Visualizations (Sentence Category Number)
- Boxplots showing the distribution of sentence category number across levels of the input variables.

---

## 5) Feed Forward Neural Network
- The model should run as-is.  
- Metrics and visualizations for **validation data** and **testing data** are included.

