# Week 5 Lab: Data Cleaning and Outlier Detection

## Project Overview

This project demonstrates data cleaning and tidying techniques using Python, pandas, and various statistical methods. The notebook covers essential data preprocessing steps including handling missing values, detecting outliers, and transforming data into tidy formats suitable for analysis.

## Author Information

**Student Name:** [Prajesh Bhatt, Kevinkumar Patel]  
**Course:** [PROG8245 Machine Learning Programming]  
**Assignment:** Week 5 Lab - Data Cleaning and Outlier Detection  
**Date:** February 2026

## Datasets Used

1. **PEW Research Dataset** (`pew.csv`) - Religious income distribution data
2. **Billboard Dataset** (`billboard.csv`) - Billboard chart rankings over time
3. **Cars Dataset** (`cars.csv`) - Automotive specifications and performance metrics
4. **Diabetes Dataset** - Scikit-learn built-in dataset for outlier detection exercises

## Project Structure

```
week5-lab/
├── week5Lab.ipynb    # Main notebook with completed exercises
├── requirements.txt             # Python package dependencies
├── .gitignore                   # Git ignore file
├── README.md                    # Project documentation (this file)
└── CSVs/                        # Data folder (not included in repo)
    ├── pew.csv
    ├── billboard.csv
    └── cars.csv
```

## Learning Objectives

This assignment covers the following key concepts:

### 1. Data Tidying
- Understanding tidy data principles (each variable = column, each observation = row)
- Using `pd.melt()` to transform wide data to long format
- Restructuring datasets for easier analysis and visualization

### 2. Data Cleaning
- **Missing Data Handling:**
  - Identifying missing values using `isnull()` and `sum()`
  - Calculating percentages of missing data
  - Comparing strategies: dropping rows vs. dropping columns
  - Imputing missing values with mean/median
  - Using `SimpleImputer` from scikit-learn

### 3. Outlier Detection and Removal
- **Visualization Methods:**
  - Box plots for identifying outliers
  - Scatter plots for relationship analysis
  
- **Statistical Methods:**
  - Z-score method (threshold: ±3 standard deviations)
  - IQR (Inter-Quartile Range) method (1.5 × IQR rule)
  - Comparing different detection approaches

## Installation and Setup

### Prerequisites
- Python 3.13.12
- pip package manager
- Git (for version control)

### Step 1: Clone the Repository

```bash
git clone <your-repository-url>
cd week5-lab
```

### Step 2: Create Virtual Environment (Recommended)

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook week5Lab_Completed.ipynb
```

## Required Packages

The project uses the following Python packages (see `requirements.txt` for versions):

- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scipy** - Scientific computing and statistics
- **scikit-learn** - Machine learning and data preprocessing
- **jupyter** - Notebook environment

## Key Concepts Implemented

### Tidy Data Principles

1. Each variable forms a column
2. Each observation forms a row
3. Each type of observational unit forms a table

### Data Cleaning Strategies

1. **For Missing Data:**
   - Drop if < 5% missing
   - Impute with mean for normally distributed data
   - Impute with median for skewed data
   - Use domain knowledge when available

2. **For Outliers:**
   - Always visualize first (box plots, scatter plots)
   - Use Z-score for normally distributed data
   - Use IQR method as a robust alternative
   - Consider domain context before removal

## Running the Notebook

1. Ensure all CSV files are in the `CSVs/` directory
2. Open the notebook in Jupyter
3. Run cells sequentially from top to bottom
4. All code cells should execute without errors
5. Observe outputs, visualizations, and markdown explanations

## Expected Outputs

The notebook produces:

1. **Tidied datasets** in long format
2. **Statistical summaries** of missing data
3. **Visualizations:**
   - Distribution histograms
   - Box plots for outlier detection
   - Scatter plots for relationship analysis
   - Before/after comparison plots
4. **Cleaned datasets** with imputed values and removed outliers
5. **Comprehensive markdown documentation** explaining each step

## Replicability Testing

To verify the notebook runs in a different environment:

1. Use a fresh Python environment
2. Install dependencies from `requirements.txt`
3. Ensure CSV files are available in the `CSVs/` directory
4. Run all cells in sequence
5. Verify all cells execute without errors
6. Check that outputs match expected results

### Testing Checklist

- [ ] Virtual environment created successfully
- [ ] All packages installed from `requirements.txt`
- [ ] All data files accessible
- [ ] All code cells execute without errors
- [ ] All visualizations render correctly
- [ ] Statistical outputs are reasonable

## Git and GitHub Usage

### Initial Setup

```bash
# Initialize git repository
git init

# Add .gitignore
git add .gitignore

# Add project files
git add week5Lab_Completed.ipynb requirements.txt README.md

# Initial commit
git commit -m "Initial commit: Week 5 Lab completed"

# Add remote repository
git remote add origin <your-github-repo-url>

# Push to GitHub
git push -u origin main
```

### Commit Message Guidelines

- Use clear, descriptive commit messages
- Start with a verb (Add, Update, Fix, etc.)
- Keep messages concise but informative

Example commit messages:
```
Add completed data tidying exercises
Implement outlier detection methods
Update documentation with examples
Fix missing value imputation logic
```

## Troubleshooting

### Common Issues

1. **ModuleNotFoundError**: Install missing package with `pip install <package-name>`
2. **FileNotFoundError**: Ensure CSV files are in the correct directory (`CSVs/`)
3. **Encoding errors**: Use `encoding='unicode_escape'` for Billboard dataset
4. **Memory errors**: Consider using data sampling for large datasets

---


