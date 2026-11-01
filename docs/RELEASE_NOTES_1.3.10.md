# Maily 1.3.10 — One Windows installer

For classic Outlook on 64-bit Windows 10/11, with a compatible ChatGPT/Codex desktop app already available.

- Download one MSI and open it. No ZIP extraction, separate developer tools or additional AI runtime installation.
- Windows Installer manages the application files, upgrades, repair, downgrade protection and removal through one Installed Apps entry.
- Setup preserves your settings, writing style, logs, ChatGPT sign-in and existing localhost certificate. Save Outlook drafts before continuing; Outlook closes cleanly before replacement.
- Maily keeps its local service ready so a pinned pane can load when Outlook opens. Setup checks the existing local registration before offering Microsoft connection.
- Repair and removal remain available when Outlook/ChatGPT is missing. Unknown or organization-managed Outlook bindings are preserved.
- Install, repair, removal and connection checks have separate diagnostic records. Local removal is distinguished from removal of an account-installed Outlook entry.

## Updating from 1.3.9 or earlier

Install this MSI once. Older versions only understand ZIP updates and cannot perform this format transition from their banner. Future versions can use the confirmed MSI update flow inside Maily.

## Outlook connection and removal

Local files and an Outlook account entry are separate. Setup reuses known Maily registration/cache metadata and refreshes only Maily's own entries while Outlook is closed. Microsoft or an organization may still require sign-in, consent or administrator deployment. Use the connection guide after installation; a completed file installation is not proof that Outlook loaded the add-in.

On uninstall, settings and logs are retained. If Maily still appears under Outlook's My add-ins, remove your user-installed entry there. An organization-managed entry must be handled by its administrator. Setup does not delete unrelated add-ins or claim it removed an unverified account entry.

The installer is unsigned. Approve only a package you initiated and recognize. Windows or Microsoft prompts may require attention. AI can be inaccurate: review all output and actions, and follow applicable data and organization policies. Maily never sends automatically. See [installation and removal](INSTALLER.md), [responsibility notice](DISCLAIMER.md), and the release's verification asset for tested scope and remaining limits.
