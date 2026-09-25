# Week 2 Assignment : Python for AI & Data Handling

Internship Week 2 submission covering NumPy, Pandas, data cleaning, data visualization, and a mini project on student performance analysis.

## 📁 Repository Structure

```
├── Week2_Assignment_PythonForAI.ipynb   # Main notebook (all 5 tasks, executed)
├── Week2_Assignment_Report.pdf          # Written report summarizing all tasks
├── student_performance.csv              # Raw dataset (with missing values & duplicates)
├── student_performance_cleaned.csv      # Cleaned dataset (output of Task 3)
├── All generated visualizations (PNG)
└── README.md
```

## 🎯 Objective

Learn how Python is used for handling data in AI — working with NumPy arrays, Pandas DataFrames, cleaning messy data, visualizing patterns, and running a small end-to-end analysis project.

## ✅ Task 1: NumPy Fundamentals

Covers creating 1D/2D arrays, checking shape and dimensions, indexing/slicing, basic math operations, and aggregate functions (`mean()`, `max()`, `min()`, `sum()`).

## ✅ Task 2: Pandas & Dataset Handling

Loaded `student_performance.csv` with Pandas and explored it — `.head()`/`.tail()`, `.shape`, `.dtypes`, `.describe()`, column selection, and row filtering (e.g. students scoring above 80 in Math).

## ✅ Task 3: Data Cleaning

The raw dataset had real issues on purpose:

| Issue | Fix |
|---|---|
| Missing values in `Gender`, `Attendance`, `Math_Marks` | Filled numeric columns with mean, categorical column with mode |
| 3 duplicate rows | Removed with `drop_duplicates()` |
| `Attendance` stored as text (e.g. `"92%"`) | Stripped `%` and converted to numeric with `pd.to_numeric()` |

Result: dataset went from 63 rows (with missing values + duplicates) → 60 clean rows, 0 missing values, 0 duplicates. Saved as `student_performance_cleaned.csv`.

## ✅ Task 4: Data Visualization

Four charts built with Matplotlib on the cleaned data:

1. **Bar Chart** — average marks per subject
2. **Line Chart** — Math marks vs study hours (sorted)
3. **Histogram** — distribution of attendance
4. **Scatter Plot** — study hours vs Science marks

Each chart has a short written explanation in the notebook/report.

## ✅ Task 5: Mini Project — Student Performance Analysis

End-to-end analysis on the cleaned dataset:

- **Overall average marks:** 67.65 / 100
- **Highest average:** 100.0
- **Lowest average:** 22.2
- **Passed:** 51 students | **Failed:** 9 students
- **Pass rate:** 85%

Includes 3 extra charts (Pass vs Fail count, distribution of average marks, average marks by gender) plus a written conclusion on what the data shows — mainly that study hours and attendance are early indicators of performance.

## 🛠️ Tools Used

Python · NumPy · Pandas · Matplotlib · Jupyter Notebook

## ▶️ How to Run

```bash
pip install numpy pandas matplotlib jupyter
jupyter notebook Week2_Assignment_PythonForAI.ipynb
```
Run all cells (Kernel → Restart & Run All) to reproduce every output and chart.

## 📄 Report

See `Week2_Assignment_Report.pdf` for the full written report with embedded charts and explanations for each task.
