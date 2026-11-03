# Project 2 — File Management Automation

## Project Overview

A UiPath Windows workflow that creates category folders, scans an input directory, routes files into PDF, Word, Excel, and Images folders, compresses the organized directory into a ZIP archive, and displays a completion message.

## Problem Statement

Manual file sorting is repetitive and inconsistent. This automation applies a predictable extension-based routing rule and produces an archive for handoff.

## Technologies Used

- UiPath Studio Community 2026.0.180 STS
- Windows project, Visual Basic expressions
- UiPath.System.Activities 25.10.3

## Activities Used

- Create Directory
- For Each File in Folder
- If / Else If
- Move File
- Compress/Zip Files
- Message Box

## Folder Layout

```text
02-File-Management-Automation/
├── Input/                    # safe test fixtures
├── Organized/PDF/
├── Organized/Word/
├── Organized/Excel/
├── Organized/Images/
└── Output/OrganizedFiles.zip
```

## Setup and Execution

1. Open `project.json` in UiPath Studio.
2. Run `Main.xaml` from the project directory.
3. Review the `Organized` folders and `Output/OrganizedFiles.zip`.

All paths are relative to `Environment.CurrentDirectory`; no personal paths or credentials are embedded.

## Validation Status

- Workflow is based on an existing UiPath Studio-generated file-sorting workflow.
- Project JSON and XAML passed structural validation.
- UiPath command-line analysis passed with advisory warnings only.
- Published package `1.0.3` executed successfully through the local UiPath Robot runner; UiPath execution logs recorded a normal start and end. The package runs in its own temporary execution directory, so generated ZIP output is not retained in the source checkout.

