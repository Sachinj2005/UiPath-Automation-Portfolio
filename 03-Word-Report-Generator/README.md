# HTML Report Generator

UiPath Studio Windows workflow using only System activities. It reads CSV student data and writes a styled HTML report with headings, a table, CSS, and summary statistics. It does not use Word or Office.

Input: `Template/Students.csv`.
Output: `Output/Report.html`.

Validation: replacement package `2.0.2` executed successfully through UiPath Robot. `Output/Report.html` was verified as a readable HTML document containing the styled table and summary.
