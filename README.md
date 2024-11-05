# Mobile Phone Dataset Analysis

This project provides a comprehensive analysis of a mobile phone dataset. It involves data cleaning, exploration, and visualization to gain insights into various aspects of the mobile phone market, including brand analysis, pricing trends, and camera specifications.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Issues Identified and Data Cleaning](#issues-identified-and-data-cleaning)
- [Data Processing](#data-processing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Brand Analysis](#brand-analysis)
- [Correlation Analysis](#correlation-analysis)
- [Requirements](#requirements)
  

## Project Overview

This project uses a mobile phone dataset containing various features such as pricing, ratings, RAM, storage, display size, and camera specifications. The primary goal is to clean and process the data, resolve inconsistencies, and derive insights through data visualization.

## Dataset

The dataset contains 984 rows and 12 columns, including:
- `Product Name`: Name of the mobile phone.
- `Actual Price (₹)`: The original price.
- `Discount Price (₹)`: The price after discount.
- `Rating`: User rating of the mobile.
- `Reviews`: Number of user reviews.
- `RAM (GB)`: RAM size in GB.
- `Storage (GB)`: Internal storage in GB.
- `Display Size (inch)`: Size of the display in inches.
- `Camera`: Camera specifications.

## Issues Identified and Data Cleaning

Several issues were identified in the dataset, which were addressed as follows:
1. **Data Type Issues**: Some columns stored numeric data as objects. The following columns were converted to `float`:
   - `Actual Price`
   - `Discount Price`
   - `Rating`
   - `Reviews`
   - `RAM (GB)`
   - `Storage (GB)`

2. **Missing Values**: Missing values, especially in RAM and Storage columns, were handled by extracting values from the `Description` column or by replacing them with median values.

3. **Unrealistic Values**: Unrealistic values in the RAM (GB) column, such as 46875.0, were removed.

4. **Column Renaming**: Columns were renamed to make them more descriptive, e.g., `Actual Price` to `Actual_price(₹)`.

## Data Processing

### Functions Implemented:
- **Convert Columns to Float**: A function to convert object data types to float after removing non-numeric characters.
- **Extract RAM and Storage**: Extracted RAM and storage values from the `Description` column using regex.
- **Extract Brand**: Extracted brand names from `Product Name`.
- **Split and Convert Camera**: Split and converted camera specifications into `Main Camera (MP)` and `Second Camera (MP)`.

## Exploratory Data Analysis (EDA)

### Descriptive Statistics
- Calculated descriptive statistics for each column to understand the central tendency and spread of the data.

### Brand Analysis
- **Brand Frequency Analysis**: Identified the most common brands in the dataset.
- **Average Price by Brand**: Compared the average prices of different brands.

### Visualization
- Plotted brand frequency and average prices by brand.
- Plotted the distribution of various features to understand the data distribution.

## Correlation Analysis

Examined the relationships between `Actual Price`, `RAM`, `Storage`, `Main Camera`, and `Second Camera` to identify any significant correlations.

## Requirements

This project requires the following libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `re`
- `random`

To install the libraries, use:
```bash
pip install pandas numpy matplotlib seaborn
