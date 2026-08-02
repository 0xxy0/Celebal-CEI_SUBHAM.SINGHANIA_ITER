# Week 7 – Delta Lake MERGE Project

## Aim
This week’s task focuses on cleaning and transforming raw data with Python and Pandas, using the Superstore dataset as the source.

## Dataset Information
The dataset chosen is the Superstore dataset, specifically the file:

- `Sample - Superstore.csv`

## Steps Completed
- Imported the CSV file into a Pandas DataFrame  
- Conducted an initial inspection with functions like `head()`, `tail()`, `shape`, `columns`, and `dtypes`  
- Verified the presence of null values across all fields  
- Removed missing entries using `dropna`  
- Eliminated duplicate records  
- Applied a filter to retain rows where **Sales > 100**  
- Narrowed down the dataset to key attributes  
- Generated a new column **Price** calculated as `Sales / Quantity`  
- Added another column **total_amount** computed as `Price * Quantity`  
- Exported the refined dataset to `cleaned_superstore.csv`

## Final Output Dimensions
The processed dataset contains:
- **9994 rows**  
- **23 columns**

## Files Delivered
- `assignment.ipynb`  
- `Sample - Superstore.csv`  
- `cleaned_superstore.csv`  
- `README.md`

## Tools Utilized
- Python  
- Pandas  
- Jupyter Notebook  
- Visual Studio Code
