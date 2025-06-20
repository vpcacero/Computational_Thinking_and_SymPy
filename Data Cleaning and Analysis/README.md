---
This project explores the Titanic passenger dataset by first **cleaning** the data and then **analyzing survival patterns** based on class, family members, and embarkation point.
---

##  Question 1: Load and Prepare the Dataset

### Load the Dataset

We begin by importing the dataset using pandas:

**Code:**
import pandas as pd
df = pd.read\_csv("train.csv")

---

###  Inspect the Dataset

We use the following functions to understand the data structure:

* df.head() — shows the first few rows
* df.info() — displays column types, non-null values, and memory usage
* df.describe() — gives statistical summaries (mean, std, min, quartiles, etc.)
* df.columns — lists all column names

**Observation:**

* The dataset has **891 rows** and **12 columns**.
* Key columns like **Age**, **Cabin**, and **Embarked** have **missing values**.

---

###  Handle Missing Values

We identify missing values in each column:

**Code:**
df.isnull().sum()

**Missing Data Summary:**

* Age: 177 missing
* Cabin: 687 missing (over 70%)
* Embarked: 2 missing

**Actions Taken:**

* Dropped "Cabin" column since it had too many missing values
  → df.drop(columns=\["Cabin"], inplace=True)
* Retained "Age" for now
* Left "Embarked" since only 2 entries are missing

---

###  Remove Duplicates

Check for and confirm there are no duplicate rows:

**Code:**
df.duplicated().sum()

---

### Convert to Categorical Data

Convert specific columns to category type for efficiency:

**Code:**
df\["Survived"] = df\["Survived"].astype("category")
df\["Pclass"] = df\["Pclass"].astype("category")

---

###  Standardize Column Names

Make all column names lowercase for consistency:

**Code:**
df.columns = df.columns.str.lower()

---

###  Export Cleaned Data

Save the cleaned dataset:

**Code:**
df.to\_csv("titanic\_cleaned.csv", index=False)

---

##  Question 2: Analyze the Cleaned Data

###  Load Cleaned Dataset

**Code:**
df = pd.read\_csv("titanic\_cleaned.csv")
df.head()

---

## Analysis 1: Average Number of Family Members by Class

Analyzed how the average number of siblings/spouses (`sibsp`) varies across passenger classes.

**Interpretation:**
First-class passengers often traveled alone or as couples. Third-class passengers were more likely to travel in larger family groups, reflecting economic migration behavior.

---

## Analysis 2: Survival Rate by Embarkation Point

Studied survival rates based on where passengers boarded the Titanic.

**Interpretation:**

* Cherbourg (C): Highest survival rate
* Queenstown (Q): Moderate
* Southampton (S): Lowest

This suggests that passengers boarding at Cherbourg had a better chance of survival—possibly due to class distribution or cabin locations.

---

##  Libraries Used

* pandas — for loading, cleaning, and manipulating data
* matplotlib.pyplot — for visualization


