# Project 1 — Excel Data Processing Automation

## Project Overview

A UiPath Windows project that processes student scores from an Excel workbook, filters records above 75, sorts the eligible results by score, writes the result to a worksheet, and exports a CSV file.

## Problem Statement

Manual review of student score sheets is repetitive and error-prone. This workflow standardizes the filtering and export process.

## Technologies Used

- UiPath Studio Community 2026.0.180 STS
- Windows project, Visual Basic expressions
- `UiPath.System.Activities` 25.10.3
- `UiPath.Excel.Activities` 3.6.0-preview

## Activities Used

- Excel Process Scope
- Use Excel File
- Read Range
- Filter
- Sort Range / Sort By Column
- Write DataTable to Excel
- Export to CSV

## Input and Output

- Input: `Input/Students.xlsx`
- Excel output sheet: `FilteredStudents`
- CSV output: `Output/EligibleStudents.csv`

## Setup and Execution

1. Open `project.json` in UiPath Studio.
2. Confirm the Excel activity package is restored.
3. Run `Main.xaml` from the project folder.
4. Review `Output/EligibleStudents.csv`.

The workflow uses `Environment.CurrentDirectory` and relative `Input`/`Output` folders so it remains portable when cloned.

## Validation Status

- Project created using UiPath Studio.
- Main workflow is based on Studio-generated modern Excel activities.
- `project.json` and `Main.xaml` passed structural validation.
- UiPath command-line analysis passed with advisory warnings only.
- The sample `.xlsx` is a valid Office package. Robot package `1.0.2` now ends with `ExcelApplicationCard: Error opening workbook` and recommends UiPath's Microsoft Office Interop Repair Tool. Excel COM opening also hangs outside UiPath. No CSV was verified; an Office repair action is required before retesting.

