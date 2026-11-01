# Privacy and data flow

Optional update checks request public GitHub release metadata. Mailbox contents and AI credentials are never included. Downloads start only after confirmation. Software packages and operational update logs are staged under the per-user Maily/Updates folder for recovery; these are retained by default and contain application files, not mailbox data.

Maily runs a local Outlook add-in and local backend; its AI model is not offline. Text required for a requested reply, summary, search or style-learning operation is sent through the existing signed-in desktop AI runtime. Provider account policies govern processing and retention. Maily does not promise zero retention by the provider.

Depending on the requested feature, context can include message text, subject, participants, current draft, selected search results and readable attachment text. Use only authorized data. Do not process organization data with a personal AI account without permission.

Supported attachments are read through the selected Outlook item. Raw file bytes are held in pane memory and passed to the local extraction endpoint; bounded extracted text informs AI summaries. File contents are not saved to settings, browser storage or telemetry. File identity checks remain in memory. Images/scans, protected files and cloud links are not interpreted.

Settings and learned writing-style information are stored in the per-user application data directory. Undo/comparison text remains in active-pane memory. The quick tour stores only a non-sensitive completion flag. Review and redact logs locally before sharing them; do not post mailbox contents or credentials in public issues.

Style learning is optional and reads sent messages only after an explicit start. Uninstall preserves settings/logs by default and does not remove shared desktop AI sign-in. Deleting retained user data must be a deliberate user action.

Downloads contain application files, templates, synthetic fixtures and required third-party notices, not the maintainer's account state or mailbox data. The public repository contains only the current distribution documentation; development code/history and older releases remain private.
