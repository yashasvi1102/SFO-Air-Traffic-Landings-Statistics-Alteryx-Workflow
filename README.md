🗂️ Project: SFO Air Traffic Landings Statistics – Alteryx Data Profiling & Transformation (DAMG7370 Fall 2025)

This project focuses on data preparation, profiling, and transformation using Alteryx Designer and Azure SQL Database.
Below are the key components of the workflow and tasks completed:

🔹 Database Setup

Created a SQL Server / Azure SQL Database named DAMG7370FALL2025.

Created a user damg7370 and granted db_owner privileges for full database access.

🔹 Data Analysis & Profiling (Alteryx)

Imported SFO Air Traffic Landings Statistics dataset (CSV format).

Performed data profiling to assess field health — missing values, uniqueness, ranges, and data types.

Applied Auto Field tool to optimize column data types and validated the selected types.

🔹 Data Transformation

Converted Activity Period field from string to a proper Date format.

Converted date_as_of and data_loaded_at fields from PST to GMT timezone.

Created metadata fields:

DI_Created_By – captures system user name via GetEnvironmentVariable("USERNAME").

DI_Created_Dt – captures current system date/time converted to GMT using DateTimeToUTC(DateTimeNow()).

Sequence ID – generated with Record ID tool, positioned as the first column.

Used Select / Dynamic Rename tools to rename all fields into database-friendly formats (no spaces or special characters).

🔹 Data Validation

Cross-checked all columns against the DataSF Data Dictionary bounds.

Filtered out records violating catalog metadata or value constraints.

Retained only valid rows for the final output dataset.

🔹 Deliverables

.yxmd – Alteryx workflow file

Final cleaned and validated CSV output

Invalid rows (separate CSV for reference)

Profiling screenshots and supporting documentation
