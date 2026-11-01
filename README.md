# Maily 1.3.10

An AI writing assistant for **classic Outlook on Windows**. Summarize an email and supported attachments, prepare a reply, review it, then apply it when ready. Maily never sends mail automatically.

**[Download the single MSI installer](https://github.com/madmike30/maily-releases/releases/latest/download/MailyOutlookAddin-1.3.10.0.msi)** · [Release files and checksum](https://github.com/madmike30/maily-releases/releases/latest)

Only the current installer and user documentation are public. Development code, history and older releases are kept privately.

## Install

1. Download `MailyOutlookAddin-1.3.10.0.msi`. No extraction is needed.
2. Save Outlook drafts and finish inline replies. Double-click the MSI, read the responsibility notice, then Install.
3. Allow setup to close Outlook normally. Keep the connection-guide option selected on the final screen.
4. The guide checks existing registration first. Use **Check connection** to open Outlook. Start **Sign in and connect** only if connection is needed, and handle Microsoft consent yourself.

You need Windows x64, classic Outlook, internet access and a compatible ChatGPT/Codex desktop app already installed and signed in. Maily does not install ChatGPT or a second AI runtime. No SDK, separate .NET application runtime, Node.js, Codex CLI or developer tools are required. Windows' standard .NET Framework 4.8 component is required.

The installer is unsigned. Windows may show an unknown-publisher or first-time localhost-certificate trust prompt. Approve only an installation you initiated and recognize. Microsoft and organization policies can require consent or administrator deployment. [Full install, repair and removal guide](docs/INSTALLER.md).

## In this version

- One native Windows Installer package, with per-user upgrade, repair, rollback, downgrade protection and removal.
- Keep settings, writing style, sign-in, logs and the existing localhost certificate across normal reinstall.
- Reuse compatible local Outlook registration; distinguish local installation from account-installed add-in availability.
- Keep the local server ready before a pinned Outlook pane opens.
- Preserve installation diagnostics when checking connection, and keep repair/removal available when Outlook or ChatGPT is missing.
- Future updates use a verified MSI after explicit confirmation. **Install this MSI manually once when moving from 1.3.9 or earlier**; older update clients only understand ZIP releases.

Reply, Summary, Search, Settings, attachment contents, email-language detection, action-item handoff and signature/draft safeguards remain. Images, scans, password-protected files and cloud links are not interpreted. Read per-file coverage before relying on a summary. [Release notes](docs/RELEASE_NOTES_1.3.10.md) · [Verification and limits](docs/VERIFICATION.md).

## Use, repair and remove

Review replies before choosing **Apply reply**. Settings > **Show quick tour** explains the workflow; learning your style is optional.

Rerun the MSI to repair or remove Maily, or open **Maily Outlook Add-in** from Start and choose **Repair or remove Maily**. Windows Settings > Apps also provides Uninstall. Run one installer at a time; do not start an older ZIP setup during an MSI transaction.

Settings and logs are retained. An account-installed Outlook entry can remain after local uninstall: remove your own copy through Outlook's My add-ins, or ask the administrator about managed copies. Local cache cleanup does not remove an account deployment.

AI can be inaccurate. Review every result and use only data you are authorized to process. Use is your responsibility. Maily is not affiliated with Microsoft or OpenAI. [Responsibility disclaimer](docs/DISCLAIMER.md) · [Privacy](PRIVACY.md) · [Security](SECURITY.md).

Maily is distributed under the MIT license. Bundled third-party components retain their own licenses and notices.
