# ElevateLabs_Task1

## Dataset Overview
- Source: marketing_campaign.csv  
- Initial Rows: 2,240  
- Final Rows After Cleaning: 2,216  
- Columns: 29 
## Cleaning Steps Performed
1. Missing Values  
Dropped 24 rows with missing `Income` values.
2. Duplicates  
Removed duplicate records using `.drop_duplicates()`.
3. Text Standardization  
Cleaned `Education` and `Marital_Status` columns (fixed casing, trimmed whitespace).
4. Date Conversion  
Converted `Dt_Customer` to proper `datetime` format (`YYYY-MM-DD`).
5. Column Renaming  
Renamed all columns to lowercase with underscores (e.g., `Year_Birth` → `year_birth`).
6. Data Type Fixes  
The dt_customer column, initially stored as an object (string), was converted to a proper datetime64[ns] format using pd.to_datetime() to enable date-based operations. The income column, originally a float64 type with some missing values, was retained as float64 after dropping rows with null entries. The year_birth column was explicitly cast from int64 to int to ensure clarity 
