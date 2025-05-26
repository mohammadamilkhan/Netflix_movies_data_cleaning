##  Data Cleaning with Pandas

This project involves cleaning a Netflix titles dataset using Python and pandas. The dataset contains metadata like title, director, cast, country, date added, and more.

###  Cleaning Steps

1. **Handling Missing Values**
   - Identified missing values using `isnull().sum()`.
   - Replaced nulls in categorical fields (`director`, `cast`, `country`) with `"Unknown"`.
   - Filled missing dates with a placeholder value (`'01-01-1900'`).

2. **Removing Duplicates**
   - Removed exact duplicate rows using `drop_duplicates()` to ensure unique records.

3. **Standardizing Text Fields**
   - Trimmed and standardized text fields like `country` using `.str.title().str.strip()`.
   - Normalized a sample `gender` field (if present) to lowercase with `.str.lower()`.

4. **Date Formatting**
   - Converted `date_added` column to a consistent format: `dd-mm-yyyy` using `pd.to_datetime()`.

5. **Renaming Columns**
   - Cleaned column names by converting to lowercase and replacing spaces with underscores using:
     ```python
     df.columns = df.columns.str.strip().str.lower().str.replace(' ', '_')
     ```

6. **Fixing Data Types**
   - Ensured numeric fields like `release_year` were cast to integers.
   - Converted `date_added` to `datetime` type for consistency.

###  Dependencies
- pandas
- numpy

