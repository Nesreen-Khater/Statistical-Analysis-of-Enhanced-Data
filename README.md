# Statistical Analysis of Enhanced Data

## Description
This project performs a statistical analysis of enhanced numerical data using the Interquartile Range (IQR) method. It focuses on detecting, scoring, and classifying outliers and studying their impact on key statistics such as mean, median, and standard deviation through visualization and progressive outlier removal.

---

## Dataset
- **File name:** Data1.txt  
- **Type:** One-dimensional numerical data  
- **Description:** A set of enhanced numerical values used to analyze data distribution and outliers.

---

## Objectives
- Analyze the statistical distribution of the data.
- Compute basic descriptive statistics before and after outlier removal.
- Detect outliers using the IQR method.
- Assign outlier scores and classify outliers into different severity levels.
- Study the impact of removing different outlier levels on data statistics.
- Visualize data distribution and statistical changes.

---

## Statistical Measures
The following measures are calculated:
- Mean
- Median
- Standard Deviation
- Variance
- First Quartile (Q1)
- Second Quartile (Median / Q2)
- Third Quartile (Q3)
- Interquartile Range (IQR)

All statistics are computed:
- On the original dataset
- After removing Moderate outliers
- After removing High outliers
- After removing Extreme outliers

---

## Outlier Detection and Classification

### Outlier Detection (IQR Method)
- **Outliers:**  
  Values below `Q1 − 1.5 × IQR` or above `Q3 + 1.5 × IQR`
- **Extreme Outliers:**  
  Values below `Q1 − 3 × IQR` or above `Q3 + 3 × IQR`

### Outlier Scoring
- For values above the upper bound:  
  `(Value − Q3) / IQR`
- For values below the lower bound:  
  `(Q1 − Value) / IQR`

### Outlier Levels
- **Moderate:** 1.5 ≤ Score < 3  
- **High:** 3 ≤ Score < 5  
- **Extreme:** Score ≥ 5  

Each outlier is listed with its value, score, and classification.
Boxplot for the data after removal of extreme levels
<img width="552" height="413" alt="image" src="https://github.com/user-attachments/assets/13554d61-c432-4da6-aa35-0f31d01e5b80" />



---

## Impact Assessment
The dataset is analyzed after progressively removing:
1. Moderate outliers
2. High outliers
3. Extreme outliers

At each stage, changes in mean, median, and standard deviation are recorded and analyzed to understand how different outlier levels affect the data distribution.

---

## Visualizations
The notebook includes:
- Histogram and box plot of the original data
- Histogram and box plot after each outlier removal level
- Line plot showing changes in mean, median, and standard deviation across removal stages

These visualizations help illustrate the influence of outliers on the dataset.

---

## Tools and Libraries
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## How to Run
1. Clone the repository
2. Place `Data1.txt` in the project directory
3. Open the Jupyter Notebook
4. Run all cells to reproduce the analysis and visualizations

---

## Discussion
Outliers can significantly affect statistical measures, especially the mean and standard deviation. Moderate and high outliers often represent natural variability, while extreme outliers may result from data entry errors, sensor faults, or rare events. Progressive outlier removal provides a clearer understanding of the underlying data distribution.



