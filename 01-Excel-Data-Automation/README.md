# Project 1 — CSV Data Processing Automation

## Overview

A portable UiPath Windows workflow that reads student records from a CSV file at runtime, filters scores above 75, sorts the qualifying records from highest to lowest, and calculates summary statistics. The historical folder name is retained for portfolio compatibility; the workflow does not use Excel or Office activities.

## Inputs and outputs

- Input: `Input/Students.csv`
- Alternate verification input: `TestData/Students_Alternate.csv`
- Outputs: `Output/FilteredStudents.csv` and `Output/Summary.txt`

## Activities and implementation

- Read Text File
- Invoke Code (VB.NET parsing, filtering, sorting, and statistics)
- Create Directory
- Write Text File

The CSV is read on every run. Student names, courses, scores, totals, averages, and sorted rows are derived from the current input; no student values are embedded in the workflow. Invalid or non-numeric score rows are excluded from the valid-score statistics.

## Run

Open `project.json` in UiPath Studio Community 2026.0.180 STS and run `Main.xaml`, or publish the Windows project and execute it with UiPath Robot. The workflow uses `Environment.CurrentDirectory` and relative folders.

## Verified runtime tests

- Robot package 3.1.0 with the default fixture: PASS. Generated three rows above 75 in descending order (91, 86, 79); average 82.50.
- Robot package 3.1.1 with `Students_Alternate.csv`: PASS. Generated Chris Developer 95, Aditi Rao 88, Dina QA 76; average 78.20.
- Both runs completed through the installed UiPath Robot with exit code 0.

