# AI-2025-001-Clean-Synthetic-Dataset-for-Backlog-Demo-Data-Cleaning

#### Task Summary and Cleaning Approach

The task involved cleaning and standardizing a synthetic radiology backlog dataset using Python and the pandas library. The goal was to ensure the dataset was consistent, accurate, and ready for further analysis by addressing issues such as inconsistent column names, duplicates, placeholders, and missing values.


#### Steps Performed

- Imported the dataset into pandas and examined its structure to identify inconsistencies and missing fields.

- Renamed all columns to snake_case for readability and uniformity.

- Removed duplicate records based on a composite key (study_id + patient_id).

- Missing Value Treatment: Several categorical columns, such as "follow_up_type", "body_part", and "priority", contained "None" and "Nan" values. These were not modified, as pandas automatically interprets "None" as missing in object-type columns. Leaving them unchanged keeps the dataset’s integrity while still allowing them to be recognized as missing values in any analysis.

- Several categorical columns, such as "follow_up_type", "body_part", and "priority", contained "None" and "Nan" values. These were not modified, as pandas automatically interprets None as missing in object-type columns. Leaving them unchanged keeps the dataset’s integrity while still allowing them to be recognized as missing values in any analysis.

- Date Columns: Non-date placeholders (e.g., “tbc”) in the "follow_up_due_date" column were replaced with proper missing datetime values (NaT) for consistency.

- Standardized the values in the "follow_up_recommended" column to Boolean (True / False).

- Formatted date columns (request_date, scan_date, report_date, follow_up_due_date) into ISO format (YYYY-MM-DD).

- Confirmed data types and ensured consistent date formats across all records.


#### Final Dataset Description

- The final cleaned dataset is a structured, analysis-ready version of the original radiology backlog data.

- All column names follow a consistent naming convention.

- Duplicates and placeholder entries were resolved.

- Missing values are properly recognized by pandas (NaN/NaT).

- Dates follow the standard ISO format.
