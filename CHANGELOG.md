# Maily 1.3.10

- Replace the ZIP with one native per-user MSI. No extraction or separate AI runtime installation.
- Add Windows Installer repair, file ownership, upgrade/rollback and downgrade protection.
- Keep local server readiness ahead of pinned Outlook pane startup.
- Reuse existing compatible local registration; distinguish local uninstall from account add-in removal.
- Preserve user settings, sign-in, logs and certificate state. Keep independent installation and connection-check diagnostics.
- Move future confirmed in-app updates to verified MSI packages. Older versions need this one manual MSI installation.

Existing reply/summary, supported attachment contents, email language, signature and draft safeguards remain. Maily never sends automatically.

[Release notes](docs/RELEASE_NOTES_1.3.10.md) · [Verification](docs/VERIFICATION.md).
