# REST API & JSON Automation

This Windows-targeted UiPath workflow performs a real HTTP GET request to the public JSONPlaceholder users endpoint, parses the JSON array, validates required fields, and generates CSV and summary reports. No API key or credential is required.

## Workflow

1. Read the checked-in `Input/users-sample.json` fixture.
2. Use the `NetHttpRequest` activity from `UiPath.WebAPI.Activities` to call `https://jsonplaceholder.typicode.com/users`.
3. Use `DeserializeJsonArray` to parse the response and extract `id`, `name`, `username`, and `email`.
4. Mark records with missing required values as incomplete.
5. Write the response snapshot, CSV report, and execution summary to `Output`.
6. If the request fails, returns a non-success response, or contains invalid JSON, continue with the local fixture and record the fallback source in `Summary.txt`.

## Project files

- `Main.xaml` — runnable UiPath workflow.
- `project.json` — Windows project metadata and package dependencies.
- `Input/users-sample.json` — offline JSON fallback fixture.
- `Output/` — generated locally at runtime and excluded from Git.

## Dependencies

- `UiPath.System.Activities` `25.10.3`
- `UiPath.WebAPI.Activities` `2.4.0`

## Runtime verification

Package `1.2.0` was executed through UiPath Robot on 2026-11-07. The Robot log records a clean start and end in approximately two seconds. The generated `LiveApiResponse.json` contained 10 live API records, and `Summary.txt` reported:

```text
Records: 10
Valid records: 10
Incomplete records: 0
Source: Live API response (HTTP 200)
```

`UsersReport.csv` was verified to contain the header plus 10 records from the live response. The offline fixture and recovery branch remain included for deterministic testing when the endpoint is unavailable.

The recovery path was also executed through Robot in an isolated test copy with the endpoint intentionally unavailable. It produced the fixture's expected three records, two valid records, one incomplete record, and `Source: Offline fixture fallback` without failing the process.
