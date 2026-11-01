# Security and support boundaries

In-app updates accept only the official stable Maily release and fixed versioned assets, require explicit confirmation and verify SHA256, package identity and bounded native MSI media/files before setup (legacy ZIP support also verifies inventory and archive paths). These checks establish consistency with the GitHub release, not independent publisher authentication if that release account is compromised. No arbitrary download URL or shell command is accepted from the pane. Hosted/custom layouts use manual or administrator updates.

Maily supports classic Outlook on Windows. It has not been independently certified and does not promise freedom from vulnerabilities.

Report security concerns privately through GitHub private vulnerability reporting when available. If unavailable, open a minimal issue asking for a private channel. Never post credentials, mailbox contents, exploit details containing private data or unredacted logs in public issues.

The supported package serves its pane over loopback HTTPS. Hostname/origin checks and configured API-key protections do not protect against malware or another process running as the same Windows user. Credentials are not included in downloads or stored in pane browser storage.

Generation uses a restricted runtime configuration without shell, browser, computer or plugin tools. Email and attachment contents are untrusted evidence. Prompt injection can still affect generated text and conclusions; review output before using it. Item/body/file checks protect draft changes, and Undo refuses later edits or ambiguous writes. Maily never sends automatically.

Document extraction has file/text/expansion/page/sheet/slide limits. These are managed parser safeguards, not an operating-system sandbox or a hard parser deadline. Unsupported or unreadable content is disclosed rather than inferred.

The installer is unsigned. Package checksums establish artifact consistency, not publisher identity or a guarantee of safety. Windows trust and Microsoft consent remain controlled by those platforms. Open the single MSI installer without extracting it and follow [installation guidance](docs/INSTALLER.md).
