# MSCS 634 Lab 1 – Data Visualization, Preprocessing, and Statistical Analysis

## Overview

This repository contains the work completed for **MSCS 634 Lab 1: Data Visualization, Preprocessing, and Statistical Analysis**. The lab uses a retail sales dataset containing product information, sales quantities, prices, discounts, customer ratings, categories, and regions. Python and Pandas were used to load, explore, visualize, preprocess, and statistically analyze the dataset.

## Dataset

The dataset is stored in:

```text
retail_sales_data.csv
```

The dataset contains **30 rows and 9 columns**:

* Product_ID
* Product
* Category
* Quantity
* Unit_Price
* Discount_Percent
* Customer_Rating
* Region
* Total_Sales

`Total_Sales` was calculated using the quantity sold, unit price, and discount percentage.

## Step 1: Data Loading and Exploration

The retail sales dataset was created and loaded into a Pandas DataFrame. The dataset dimensions were examined, and the first five records were displayed to verify that the data was loaded correctly.

## Step 2: Data Visualization

Several visualization techniques were used to explore relationships and distributions within the retail sales data. The visualizations included charts such as scatter plots, bar charts, histograms, box plots, and pie charts as appropriate for the dataset.

The visualizations were kept at a manageable size so that they could be clearly viewed and captured as screenshots.

## Step 3: Data Preprocessing

The following preprocessing techniques were performed:

### Missing Values

Missing values were detected using Pandas. Missing numerical values were handled using appropriate replacement techniques, including mean replacement.

### Outlier Detection

The **Interquartile Range (IQR)** method was used to identify potential outliers in numerical variables. The first quartile (Q1), third quartile (Q3), IQR, lower bound, and upper bound were calculated. Rows containing identified outliers were then removed from the working dataset.

### Data Reduction

Data reduction was performed by randomly sampling **80% of the rows** and eliminating the `Product_ID` column because it functions as an identifier rather than an analytical variable.

### Data Scaling and Discretization

**Min-Max Scaling** was applied to the `Unit_Price` variable. Customer ratings were also discretized into meaningful categories such as **Low, Medium, and High**.

## Step 4: Statistical Analysis

Statistical analysis was performed using Pandas and NumPy.

The analysis included:

* Dataset information using `.info()`
* Descriptive statistics using `.describe()`
* Minimum and maximum values
* Mean
* Median
* Mode
* Range
* Quartiles
* Interquartile Range (IQR)
* Variance
* Standard deviation
* Correlation matrix using `.corr()`

The correlation analysis was used to examine linear relationships between numerical variables including Quantity, Unit_Price, Discount_Percent, Customer_Rating, and Total_Sales.

## Repository Structure

```text
MSCS_634_Lab_1/
│
├── MSCS_634_Lab_1_Data_Visualization_Preprocessing_Statistics.ipynb
├── retail_sales_data.csv
├── README.md
│
└── screenshots/
    ├── 01_missing_values_before.png
    ├── 02_missing_values_after.png
    ├── 03_iqr_calculation.png
    ├── 04_identified_outliers.png
    ├── 05_outliers_removed.png
    ├── 06_data_reduction_before.png
    ├── 07_data_reduction_after.png
    ├── 08_scaling_before.png
    ├── 09_scaling_after.png
    ├── 10_dataset_info.png
    ├── 11_descriptive_statistics.png
    ├── 12_central_tendency.png
    ├── 13_dispersion_measures.png
    └── 14_correlation_matrix.png
```

## Technologies Used

* **Python 3**
* **Jupyter Notebook**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**

## How to Run

1. Download or clone this repository.
2. Make sure Python 3 is installed.
3. Install the required libraries if necessary:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

4. Open Jupyter Notebook.
5. Open:

```text
MSCS_634_Lab_1_Data_Visualization_Preprocessing_Statistics.ipynb
```

6. Make sure `retail_sales_data.csv` is located in the same folder as the notebook.
7. Run the notebook cells from beginning to end.

## Screenshots

The `screenshots` folder contains the required evidence for the data visualization, preprocessing, and statistical analysis steps. Each screenshot is clearly labelled according to the corresponding task in the lab instructions.

## Conclusion

This lab demonstrates a complete data analysis workflow beginning with dataset creation and exploration, followed by visualization, preprocessing, and statistical analysis. The preprocessing stage addressed missing values, outliers, data reduction, scaling, and discretization. The statistical analysis provided measures of central tendency, dispersion, and correlation that helped describe the characteristics and relationships within the retail sales dataset.
