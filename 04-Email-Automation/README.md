# Email Automation

Safe local-mailbox demonstration. The workflow uses sample `.eml` files only, identifies unread test messages by keyword, copies declared attachments to `Output/Attachments`, and writes reply drafts to `Output/Drafts`. It never connects to Outlook/IMAP, sends mail, or deletes messages.

This design keeps portfolio testing safe while preserving the classification, attachment, draft, and processed-message organization pattern. Replace the local mailbox adapter with `Get Outlook Mail Messages` in Studio only when a controlled test account is available.

Validation: sample inputs and project metadata are included. Runtime is pending because the source workflow is intentionally local-test-only and does not access a live mailbox.
