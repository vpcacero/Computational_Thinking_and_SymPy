##  Question 1: Load the Dataset

**Goal:**
Load the Titanic dataset and take a first look at its structure.

**Steps:**

* Imported the Pandas library.
* Read the CSV file `titanic.csv`.
* Displayed the first 5 rows using `.head()`.

**Sample Output:**
The dataset includes columns like `PassengerId`, `Survived`, `Pclass`, `Name`, `Sex`, `Age`, `Fare`, etc.

---

##  Question 2: Check for Missing Values

**Goal:**
Find which columns have missing (empty) data.

**Steps:**

* Used `.isnull().sum()` to count missing values in each column.

**Findings:**

* `Age`: 177 missing
* `Cabin`: 687 missing (more than half!)
* `Embarked`: 2 missing

 **Conclusion:**

* `Cabin` should be dropped (too many missing).
* `Embarked` can be filled since it only has 2 missing values.

---

##  Question 3: Calculate the Survival Rate

**Goal:**
Find out how many passengers survived and what percentage that is.

**Steps:**

* Used `df["Survived"].mean()` to get the average survival rate.

**Result:**

$$
\text{Survival Rate} = 38\%
$$

 **Conclusion:**
Only 38% of passengers survived the disaster.

---

##  Question 4: Compare Ages of Survivors vs. Non-Survivors

**Goal:**
Check if age played a role in survival.

**Steps:**

* Split the dataset into survivors and non-survivors.
* Plotted a histogram showing age distribution for both groups.

**Visualization:**

* Used `matplotlib.pyplot` to create overlapping histograms.

**Conclusion:**

* Survivors tend to be **younger** on average.
* Age appears to be a factor in survival chances.

---

## Libraries Used

* `pandas` — for data manipulation
* `matplotlib.pyplot` — for visualizations

---

