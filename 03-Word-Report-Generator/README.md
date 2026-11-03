# Word Report Generator

UiPath Studio Windows workflow based on the Studio-generated Word activities. It opens a predefined template, replaces report placeholders, inserts a data table, saves the Word report, and exports a PDF.

Input: `Template/StudentReportTemplate.docx` and `Template/StudentData.xlsx`.
Output: `Output/GeneratedStudentReport.docx` and `Output/GeneratedStudentReport.pdf`.

Validation: the template is now a genuine native `.docx` file and the workflow published as package `1.0.2`. UiPath Robot executed it, but the log recorded a Word Application Scope document-open error; no report/PDF output was verified.
