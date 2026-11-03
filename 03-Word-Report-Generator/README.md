# Word Report Generator

UiPath Studio Windows workflow based on the Studio-generated Word activities. It opens a predefined template, replaces report placeholders, inserts a data table, saves the Word report, and exports a PDF.

Input: `Template/StudentReportTemplate.docx` and `Template/StudentData.xlsx`.
Output: `Output/GeneratedStudentReport.docx` and `Output/GeneratedStudentReport.pdf`.

Validation: `Main.xaml` passed XML parsing and UiPath command-line structural analysis. Runtime is pending because the checked-in sample template is a safe placeholder fixture rather than a native Word document; replace it with a real `.docx` template in Studio before attended execution.
