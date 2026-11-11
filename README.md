# 🏠 Housing Price Analysis & Data Preprocessing

## 📌 Project Overview

This project focuses on analyzing and preprocessing a Housing Price dataset using Python. It involves exploring the dataset, identifying data quality issues, handling missing values, removing duplicates, treating outliers, and performing exploratory data analysis (EDA).

The primary objective is to transform raw housing data into a clean and structured dataset suitable for machine learning regression algorithms.

## 🎯 Objectives

- Understand the structure and characteristics of the housing dataset.
- Perform Exploratory Data Analysis (EDA).
- Identify and handle missing values and duplicate records.
- Detect and handle inconsistent categorical values.
- Convert incorrect data types into appropriate formats.
- Identify and handle outliers using the IQR method.
- Visualize relationships between housing features.
- Export the final preprocessed dataset for further analysis and machine learning.

## 🛠️ Technologies & Libraries Used

- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Jupyter Notebook** – Development environment

## 📂 Project Structure

```text
Housing-Price-Analysis/
│
├── Housing_Price_Project.ipynb
│
├── housing_prices_regression.csv
│
├── preprocessed_housing_prices.csv
│
└── README.md
```

## 📊 Dataset Description

The dataset contains housing-related information used to analyze factors affecting house sale prices.

### Features

| Feature | Description |
|---|---|
| id | Unique house identifier |
| num_bedrooms | Number of bedrooms |
| num_bathrooms | Number of bathrooms |
| size_sqft | House size in square feet |
| year_built | Year the house was constructed |
| zipcode | Location ZIP code |
| has_garage | Whether the house has a garage |
| has_garden | Whether the house has a garden |
| sale_price | House selling price (Target Variable) |

## 🔍 Project Workflow

### 1. Importing Libraries
Imported the required Python libraries for data manipulation, numerical operations, and visualization.

### 2. Loading the Dataset
Loaded the housing dataset using Pandas.

### 3. Data Exploration
- Examined dataset structure using `df.info()`.
- Viewed initial records using `df.head()`.
- Checked missing values.
- Identified duplicate records.
- Inspected unique categorical values.
- Examined incorrect data types.
- Checked redundancy between columns.

### 4. Data Cleaning

Performed the following cleaning operations:

- Removed duplicate records.
- Dropped the redundant `zipcode_dup` column.
- Converted `size_sqft` into numerical format.
- Standardized inconsistent values in `has_garage` and `has_garden`.
- Handled missing numerical values using median imputation.
- Handled missing categorical values using mode imputation.
- Removed the original identifier column (`id`).

### 5. Outlier Detection and Handling

Applied the **Interquartile Range (IQR) method** to identify and cap outliers in:

- `size_sqft`
- `sale_price`

Used the 1.5 × IQR boundaries to cap extreme values.

### 6. Exploratory Data Analysis (EDA)

Performed different types of data analysis:

**Univariate Analysis**
- Analyzed the distribution of house sale prices using a histogram and KDE plot.

**Bivariate Analysis**
- Explored the relationship between house size and sale price using a scatter plot.

**Multivariate Analysis**
- Created a correlation heatmap to understand relationships between numerical features.

### 7. Categorical Encoding

Converted categorical variables into numerical representations:

- Yes → 1
- No → 0

Applied this encoding to:
- `has_garage`
- `has_garden`

### 8. Exporting the Preprocessed Dataset

- Generated a new sequential ID column.
- Reset the dataset index.
- Exported the cleaned dataset into a CSV file.

**Output:** `preprocessed_housing_prices.csv`

## 📈 Visualizations

The notebook includes:

1. Distribution of Housing Sale Prices.
2. House Size vs Sale Price Scatter Plot.
3. Correlation Heatmap of Numerical Features.

These visualizations help understand the distribution of housing prices and relationships between different housing attributes.

## ⚙️ Installation & Execution

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Housing-Price-Analysis.git
```

### 2. Navigate to the Project Directory

```bash
cd Housing-Price-Analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Run the Jupyter Notebook

```bash
jupyter notebook Housing_Price_Project.ipynb
```

Make sure the original dataset `housing_prices_regression.csv` is available in the project directory before executing the notebook.

## 📁 Output

The project generates a cleaned and preprocessed dataset:

`preprocessed_housing_prices.csv`

This dataset can be used for further machine learning tasks, particularly regression-based housing price prediction.

## 🚀 Future Improvements

- Perform feature engineering to create more meaningful features.
- Apply feature selection techniques.
- Implement Linear Regression, Decision Tree Regression, and Random Forest Regression.
- Evaluate models using MAE, MSE, RMSE, and R² score.
- Develop a complete housing price prediction system.
- Deploy the trained model using Flask or Streamlit.

⭐ If you find this project useful, consider giving the repository a star!
