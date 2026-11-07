# Project 4 — Safe Local Email Automation

## Overview

A safe, offline UiPath demonstration of an email-processing pattern. It reads local `.eml` fixtures only, treats files named `Unread_*.eml` with `X-Test-Mailbox: true` as unread test messages, classifies subjects using keywords, saves declared attachments, creates reply drafts, and copies processed messages for organization.

It never connects to Outlook, IMAP, or another mailbox. It never sends or deletes messages.

## Inputs and outputs

- Default fixtures: `Input/Unread_Invoice_Approval.eml`, `Input/Unread_Student_Report.eml`, and `Input/Invoice_Sample.pdf`
- Alternate fixtures: `TestData/Unread_Change_Request.eml`, `TestData/Unread_Invoice_Review.eml`, and `TestData/Invoice_Alternate.pdf`
- Outputs: `Output/Attachments`, `Output/Drafts`, `Output/Processed`, and `Output/EmailSummary.txt`

Keywords include invoice, approval, student, report, and request. The local adapter requires the explicit `X-Test-Mailbox: true` marker so ordinary files are not treated as mail.

## Activities and implementation

- Create Directory
- For Each File (X)
- Read Text File
- Invoke Code (header parsing, keyword classification, safe local file copies, and counters)
- Write Text File

All email addresses and attachments are synthetic test data. To use a real mailbox in the future, replace the local adapter only in a separately controlled project and obtain the required authorization.

## Verified runtime tests

- Robot package 3.0.0 with the default fixtures: PASS. Processed 2 messages, matched 2, saved 1 attachment, and created 2 reply drafts.
- Robot package 3.0.1 with the alternate fixtures: PASS. Processed 2 alternate messages, matched 2, saved `Invoice_Alternate.pdf`, and created 2 alternate reply drafts.
- Both runs completed through the installed UiPath Robot with exit code 0. No live mailbox was accessed and no message was sent or deleted.
