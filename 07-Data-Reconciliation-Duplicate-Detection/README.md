# Data Reconciliation & Duplicate Detection

This Studio Windows workflow reads two CSV datasets, compares employee IDs, and generates matched, mismatched, duplicate, and summary reports. The sample data deliberately includes matches, a salary mismatch, a duplicate ID, and a record missing from Dataset B.

Inputs: `Input/Employees_A.csv` and `Input/Employees_B.csv`. Outputs: `MatchedRecords.csv`, `MismatchedRecords.csv`, `DuplicateRecords.csv`, and `Summary.txt`.

Runtime validation: package `1.0.0` executed successfully through UiPath Robot. Verified matched, mismatched, duplicate, and summary outputs: matches E001/E004, salary mismatch E002, duplicate E003, and the documented record-count statistics.
