# Project 7 — Data Reconciliation & Duplicate Detection

## Overview

A UiPath Windows workflow that genuinely reads and compares both employee CSV datasets using EmployeeId. It reports identical records, field-level mismatches, IDs missing from either dataset, and duplicate IDs in either dataset.

## Inputs and outputs

- Inputs: `Input/Employees_A.csv` and `Input/Employees_B.csv`
- Alternate inputs: `TestData/Employees_A_Alternate.csv` and `TestData/Employees_B_Alternate.csv`
- Outputs: `Output/MatchedRecords.csv`, `Output/MismatchedRecords.csv`, `Output/DuplicateRecords.csv`, and `Output/Summary.txt`

Missing IDs are represented in `MismatchedRecords.csv` with `MissingFromA` or `MissingFromB`. Duplicate output includes the dataset and occurrence count.

## Activities and implementation

- Read Text File for Dataset A
- Read Text File for Dataset B
- Invoke Code (dictionary-based comparison, field checks, missing-ID detection, and duplicate detection)
- Create Directory
- Write Text File

Both input paths are read at runtime. The workflow does not use a hard-coded reconciliation result and does not ignore Dataset B.

## Verified runtime tests

- Robot package 2.0.1 with the default fixtures: PASS. Matched E001/E004, found the E002 salary mismatch, identified E003 as duplicated in Dataset A, and reported missing IDs.
- Robot package 2.0.2 with both alternate fixtures: PASS. Matched E100/E103, found the E101 salary mismatch, identified E102 as duplicated in Dataset A, and reported E102/E104 as missing from one side.
- Both runs completed through the installed UiPath Robot with exit code 0.
