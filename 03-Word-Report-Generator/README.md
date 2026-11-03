# Word Report Generator

UiPath Studio Windows workflow based on the Studio-generated Word activities. It opens a predefined template, replaces report placeholders, inserts a data table, saves the Word report, and exports a PDF.

Input: `Template/StudentReportTemplate.docx` and `Template/StudentData.xlsx`.
Output: `Output/GeneratedStudentReport.docx` and `Output/GeneratedStudentReport.pdf`.

Validation: the template is a valid native `.docx` package and opens manually through Word COM. Robot package `1.0.2` still reports `Word Application Scope: Error opening document` and recommends the Microsoft Office Interop Repair Tool. No report/PDF output was verified; Office repair is required before retesting.
