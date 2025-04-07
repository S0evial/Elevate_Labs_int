# 🎬 Netflix Titles Data Cleaning Project

This project involves cleaning and preprocessing a dataset containing information about Netflix shows and movies. The dataset was sourced from Kaggle and includes details like titles, genres, release year, cast, director, duration, and more.

---

## 📁 Dataset Overview

- **Rows**: 8809
- **Columns**: 12
- **Original File**: `netflix_titles.csv`

---

## 🛠️ Cleaning Steps Performed

1. **Loaded Dataset**  
   - Read using `pandas` with correct encoding (`latin1`) to handle special characters.

2. **Dropped Unnecessary Columns**  
   - Removed unnamed index columns from the CSV.

3. **Handled Missing Values**  
   - Filled missing values in:
     - `director`: `'Unknown'`
     - `cast`: `'Not listed'`
     - `country`: `'unknown'`
     - `date_added`: `default date (2000-01-01)`
     - `rating`: `'Not Rated'`
     - `duration`: `'Unknown'`

4. **Removed Duplicates**  
   - Duplicate rows were dropped to ensure data integrity.

5. **Standardized Text Values**  
   - Columns like `country` and `director` were cleaned using `str.lower()`, `str.title()`, and `str.strip()`.

6. **Renamed Columns**  
   - All column headers were converted to lowercase, stripped of spaces, and replaced spaces with underscores for consistency.

7. **Converted Date Formats**  
   - `date_added` was converted to `datetime` format using `pd.to_datetime()`.

---

## 📦 Final Output

- **Cleaned Dataset**: `Netflix_cleaned.csv`
- **Shape**: `(8809, 12)`
- **Missing Values**: Handled completely (`0` missing in all columns)

---

## 🧰 Tools Used

- Python
- Pandas
- Jupyter Notebook / VS Code

---