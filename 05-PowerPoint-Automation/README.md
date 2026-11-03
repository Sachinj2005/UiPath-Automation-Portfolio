# Log Analyzer

UiPath Studio Windows workflow using only System activities. It reads an application log, extracts ERROR lines, counts INFO/WARNING/ERROR records, and writes text and CSV reports. It does not use PowerPoint, Excel, or Office.

Input: `Template/application.log`.
Output: `Output/ErrorReport.txt` and `Output/LogSummary.csv`.

Validation: replacement package `2.0.3` executed successfully through UiPath Robot. `ErrorReport.txt` contains the two ERROR lines and `LogSummary.csv` contains INFO=3, WARNING=1, ERROR=2.
