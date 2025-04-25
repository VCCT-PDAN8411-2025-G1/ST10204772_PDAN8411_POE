# ST10204772_PDAN8411_POE
ST10204772 - Allana Morris


## Insurance Charges Analysis

This project conducts an exploratory data analysis (EDA) of a medical insurance dataset to investigate the distribution of medical charges and how various factors like smoking status, region, and sex influence those charges.

### Dataset

The dataset used is `insurance.csv`, containing the following features:

- `age`: Age of the primary beneficiary
- `sex`: Gender of the beneficiary
- `bmi`: Body Mass Index
- `children`: Number of dependents covered by health insurance
- `smoker`: Smoking status (yes/no)
- `region`: Residential area in the US (northeast, southeast, southwest, northwest)
- `charges`: Individual medical costs billed by health insurance (target variable)

---

### Project Workflow

#### 1. Importing Libraries and Loading Data

Python libraries such as `pandas`, `seaborn`, `matplotlib.pyplot`, `statsmodels`, and `scikit-learn` are imported. The dataset is loaded into a DataFrame, and basic cleaning is performed:
- Missing values are checked.
- Duplicate rows are removed.

#### 2. Visualizing the Distribution of Charges

A histogram with a KDE (Kernel Density Estimate) is used to understand the distribution of the target variable (`charges`). This visualization helps identify skewness and outliers in the data.

```python
sns.histplot(df['charges'], kde=True)
```

#### 3. Charges vs. Smoker Status

A boxplot compares the distribution of charges between smokers and non-smokers. This helps reveal the substantial impact smoking has on medical charges.

```python
sns.boxplot(x='smoker', y='charges', data=df)
```

#### 4. Charges by Region

A boxplot is used to show how medical charges vary across the four U.S. regions in the dataset. This can uncover regional trends in healthcare costs.

```python
sns.boxplot(x='region', y='charges', data=df)
```

#### 5. Charges by Sex

This boxplot examines whether there is a significant difference in charges based on the sex of the beneficiary.

```python
sns.boxplot(x='sex', y='charges', data=df)
```

---

### Libraries and Tools

- **pandas** – for data manipulation
- **seaborn** & **matplotlib.pyplot** – for data visualization
- **statsmodels** – for statistical analysis
- **scikit-learn** – for model building and evaluation

---

### How to Run This Project

1. Clone this repository or download the files.
2. Make sure you have Python 3.x and the necessary libraries installed.
3. Place `insurance.csv` in your working directory.
4. Open the Jupyter Notebook (`.ipynb` file) and run the cells sequentially.

---


