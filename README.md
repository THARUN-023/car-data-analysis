# 🚗 Car Dataset Analysis and Visualization

A Python-based Exploratory Data Analysis (EDA) project performed on a Cars Dataset using Pandas, NumPy, Matplotlib, and Seaborn.

This project focuses on cleaning, filtering, transforming, and analyzing car data to extract meaningful insights related to car brands, origin, engine performance, fuel efficiency, and pricing.

---

# 📌 Project Objectives

- Load and explore the cars dataset
- Check dataset dimensions
- Handle missing/null values
- Perform data cleaning
- Analyze car brands and origins
- Filter records based on conditions
- Transform MPG values
- Extract useful business insights

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / VS Code

---

# 📂 Dataset Features

The dataset contains information related to:

- Make
- Model
- Type
- Origin
- DriveTrain
- MSRP
- Invoice
- EngineSize
- Cylinders
- Horsepower
- MPG_City
- MPG_Highway
- Weight

---

# ⚙️ Project Workflow

## 1️⃣ Importing Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns


## 2️⃣ Loading Dataset

python
df = pd.read_csv("Cars Data1.csv")


## 3️⃣ Display First 5 Rows

python
df.head()


## 4️⃣ Check Dataset Shape

python
df.shape


## 5️⃣ Check Null Values

python
df.isnull().sum()


## 6️⃣ Fill Missing Values

python
df.fillna({
    **df.select_dtypes(include='number').fillna(0),
    **df.select_dtypes(include='object').fillna("Unknown")
}, inplace=True)


## 7️⃣ Count Car Brands

python
df['Make'].value_counts()


## 8️⃣ Filter Asia and Europe Cars

python
df[df['Origin'].isin(['Asia', 'Europe'])]


## 9️⃣ Remove Cars Weight Above 4000

python
df[~(df['Weight'] > 4000)]


## 🔟 Increase MPG_City Values

python
df['MPG_City'] = df['MPG_City'].apply(lambda x: x + 3)
