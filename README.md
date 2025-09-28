# Netflix Data Cleaning and Preprocessing Project

## Project Objective
This project was completed as part of a foundational data analysis task. The primary goal was to take a raw, real-world dataset (Netflix Movies and TV Shows) that contained common issues like missing values, inconsistent data formats, and structural problems, and transform it into a clean, analysis-ready format.

## Key Data Cleaning Tasks Performed

The cleaning process was executed using Python's **Pandas** library.

| Issue | Original State | Action Taken | Result |
| :--- | :--- | :--- | :--- |
| **Missing Values** | Nulls in `director`, `cast`, `country`, `rating`, `date_added`. | Filled categorical nulls with 'Unknown' and imputed `date_added` with a placeholder date (`1900-01-01`). | All columns are now non-null. |
| **Data Types** | `date_added` was a string (`object`). | Converted to **`datetime64[ns]`** format for time series analysis. | Date fields are usable for temporal analysis. |
| **Duration Column**| Single column (`duration`) mixing movie lengths (e.g., "93 min") and show seasons (e.g., "1 Season"). | Split into two new, numeric columns: **`duration_minutes`** and **`duration_seasons`**. | Clear separation of movie length and show season count (both as `int64`). |
| **Duplicates** | Checked for fully duplicated rows. | Used `.drop_duplicates()`. | No duplicates found, ensuring data integrity. |

## Files in this Repository

* `netflix_data_cleaning.ipynb`: The Jupyter Notebook containing the full, step-by-step cleaning code and documentation of the process.
* `netflix_titles.csv`: (Optional) The original raw dataset used for the project.
* `netflix_titles_FINAL_CLEANED.csv`: The final, processed dataset, ready for further analysis or visualization.

## Tools and Technologies

* **Python:** The primary programming language used.
* **Pandas:** Used extensively for data manipulation and cleaning.
* **Jupyter Notebook:** Used for documentation and execution of code.
* **Git & GitHub:** Used for version control and project hosting.

---
*Completed as part of a foundational data analytics exercise.*
