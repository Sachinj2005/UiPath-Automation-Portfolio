# Project 3 — Automated HTML Report Generator

## Overview

A UiPath Windows workflow that reads student data from CSV and builds a professional HTML report dynamically. The historical folder name is retained for portfolio compatibility; the workflow does not open Word and has no Office dependency.

## Inputs and outputs

- Input: `Template/Students.csv`
- Alternate verification input: `TestData/Students_Alternate.csv`
- Output: `Output/Report.html`

The report contains a heading, CSS styling, summary cards, a dynamically generated table, average/highest/lowest scores, and HTML-encoded data values.

## Activities and implementation

- Read Text File
- Invoke Code (CSV parsing, statistics, HTML generation)
- Create Directory
- Write Text File

The report rows and statistics are generated from the current CSV contents on every run. No student names or scores are hard-coded into the workflow.

## Run

Open `project.json` in UiPath Studio Community 2026.0.180 STS, run `Main.xaml`, and open `Output/Report.html` in a browser.

## Verified runtime tests

- Robot package 3.0.0 with the default fixture: PASS. The output was created and verified as valid HTML containing the styled table, Alex Student, Morgan Developer, and average 82.50.
- Robot package 3.0.1 with `Students_Alternate.csv`: PASS. The report contained the alternate names and average 78.20, and did not contain the default average 82.50.
- Both runs completed through the installed UiPath Robot with exit code 0.
