# REST API & JSON Automation

This Studio Windows workflow uses UiPath System activities to read a JSONPlaceholder-compatible user response fixture, extract user fields, validate required values, and generate `Output/UsersReport.csv` plus `Output/Summary.txt`. The fixture supports deterministic offline execution without API keys.

Input: `Input/users-sample.json`. Output: `Output/UsersReport.csv` and `Output/Summary.txt`.

Runtime validation: package `1.0.0` executed successfully through UiPath Robot. Verified `UsersReport.csv` contains two valid records and one incomplete record; `Summary.txt` reports the same counts. The checked-in fixture enables deterministic offline testing without API keys.
