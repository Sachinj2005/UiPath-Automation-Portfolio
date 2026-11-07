# Project 5 — Automated Log Analyzer

## Overview

A UiPath Windows workflow that reads actual application log entries, identifies INFO, WARNING, and ERROR severity tokens, counts each severity, extracts every ERROR line, and creates two reports. The historical folder name is retained for portfolio compatibility; the workflow does not use PowerPoint, Excel, or Office.

## Inputs and outputs

- Input: `Template/application.log`
- Alternate verification input: `TestData/application_alternate.log`
- Outputs: `Output/ErrorReport.txt` and `Output/LogSummary.csv`

## Activities and implementation

- Read Text File
- Invoke Code (line-by-line severity detection and error extraction)
- Create Directory
- Write Text File

The workflow counts and reports the current log contents at runtime. It does not embed the default error messages or counts.

## Run

Open `project.json` in UiPath Studio Community 2026.0.180 STS and run `Main.xaml`. Review both files under `Output`.

## Verified runtime tests

- Robot package 3.0.0 with the default log: PASS. Generated INFO=3, WARNING=1, ERROR=2 and extracted both default ERROR entries.
- Robot package 3.0.1 with `application_alternate.log`: PASS. Generated INFO=2, WARNING=2, ERROR=1 and extracted the alternate cache-error entry.
- Both runs completed through the installed UiPath Robot with exit code 0.
