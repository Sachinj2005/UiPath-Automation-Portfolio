# UiPath Automation Portfolio

Seven beginner-friendly UiPath Windows projects with portable sample data, genuine Studio workflows, and Robot-tested outputs. Projects 1, 3, 4, 5, and 7 were rebuilt or corrected to process their current input files dynamically. Projects 2 and 6 were preserved because they already passed runtime testing.

| Project | Focus | Verified status |
|---|---|---|
| [01 CSV Data Processing](01-Excel-Data-Automation/README.md) | Filter, sort, and summarize student CSV records | PASS — Robot default and alternate datasets |
| [02 File Management](02-File-Management-Automation/README.md) | Categorize files, organize folders, and create a ZIP archive | PASS — preserved working workflow |
| [03 HTML Report Generator](03-Word-Report-Generator/README.md) | Generate a styled HTML report from CSV data | PASS — Robot default and alternate datasets |
| [04 Safe Local Email Automation](04-Email-Automation/README.md) | Classify local .eml fixtures, save attachments, and create drafts | PASS — Robot default and alternate fixtures; no live mail |
| [05 Log Analyzer](05-PowerPoint-Automation/README.md) | Analyze INFO, WARNING, and ERROR log entries | PASS — Robot default and alternate logs |
| [06 REST API & JSON Automation](06-REST-API-JSON-Automation/README.md) | GET, parse, validate, and report on JSON API data | PASS — live HTTP 200 test plus offline fallback |
| [07 Data Reconciliation](07-Data-Reconciliation-Duplicate-Detection/README.md) | Compare two employee datasets and detect duplicates | PASS — Robot default and alternate datasets |

## Implementation notes

- UiPath Studio Community 2026.0.180 STS, Windows projects, and Visual Basic expressions.
- Native UiPath System activities are used for file I/O, directories, iteration, and reporting.
- Invoke Code is used only for deterministic in-memory parsing and report construction; it receives the current input data at runtime.
- No project depends on Microsoft Excel, Word, PowerPoint, Office COM, credentials, or paid services.
- Project 6 uses the public JSONPlaceholder endpoint and retains its local JSON fixture fallback.
- Project 4 is intentionally offline: it never connects to a mailbox, sends mail, or deletes messages.
- Generated runtime outputs remain outside the repository; each project contains source workflow, project metadata, documentation, and safe fixtures.

## Verification

The corrected projects were published and executed through the installed UiPath Robot with two different input datasets each. Their READMEs record the package versions, output checks, and observed results. Projects 2 and 6 retain their previously verified runtime results.

