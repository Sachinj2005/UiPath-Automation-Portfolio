# Email Automation

Safe local-mailbox demonstration. The workflow uses sample `.eml` files only, identifies unread test messages by keyword, copies declared attachments to `Output/Attachments`, and writes reply drafts to `Output/Drafts`. It never connects to Outlook/IMAP, sends mail, or deletes messages.

This design keeps portfolio testing safe while preserving the classification, attachment, draft, and processed-message organization pattern. Replace the local mailbox adapter with `Get Outlook Mail Messages` in Studio only when a controlled test account is available.

Validation: package `1.0.2` executed successfully through UiPath Robot using only local sample files. The Robot log records a start and end event in about three seconds. No live mailbox was accessed and no messages were sent or deleted.
