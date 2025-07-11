
# Titanic EDA & Data Cleaning 🛳️

This project presents a complete **Exploratory Data Analysis (EDA)** and **Data Cleaning** workflow on the Titanic dataset using Python libraries like `pandas`, `seaborn`, and `matplotlib`.

---

## 📌 Project Goals

- Understand the structure and key patterns in the Titanic dataset
- Handle missing values
- Detect and remove outliers
- Prepare a cleaned version of the dataset for future modeling

---

## 🧪 Dataset

- Source: `seaborn` Titanic dataset (`sns.load_dataset('titanic')`)
- Shape before cleaning: ~891 rows × 15 columns

---

## 🔍 Exploratory Data Analysis (EDA)

Used tools like `df.info()`, `df.describe()`, `isnull()`, and group-based statistics to explore data.

### 📊 Key Visualizations:

- Survival counts using `countplot`
- Correlation heatmap
- Missing values visualized via:
  - Seaborn heatmap
  - `missingno.bar()`
- Boxplots of `fare` and `age` by survival
- Group-based survival rates:
  - By `sex`, `pclass`, `adult_male`, `alone`, and `embarked`

---

## 🧼 Data Cleaning Steps

- Filled missing `age` values with the **median**
- Filled missing `deck` values with `"Unknown"` category
- Filled missing `embarked` and `embark_town` with **mode**
- Dropped columns not relevant: `embark_town`, `alive`
- Removed **outliers** from `fare` and `age` using **IQR method**
- Dropped duplicates

---

## ✨ Feature Engineering (Optional Step)

*Prepared for modeling (commented out):*

```python
df = pd.get_dummies(df, columns=['sex','embarked','class','who','deck'], drop_first=True)


🛠️ Libraries Used
pandas
numpy
seaborn
matplotlib
missingno

📈 Future Work
Apply machine learning models (e.g., logistic regression)

Perform feature selection & hyperparameter tuning