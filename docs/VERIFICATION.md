# Maily 1.3.10 verification

The release's standalone VERIFICATION.md asset records the final full-suite and exact-package checks. Use its SHA256 sidecar to verify your download. Do not treat historical results as a new physical installation test.

This release adds native Windows Installer coverage:

- Synthetic lifecycle tests exercise preparation, staging, repair, configuration, removal, rollback and repeated recovery. Office/Graph/COM, certificate stores, process control and real installed state are mocked. They cover missing prerequisites, ownership conflicts, preserved settings and independent verification diagnostics.
- A separate tiny native MSI fixture exercises the real Windows Installer engine: install, repair, failed upgrade rollback, successful major upgrade, downgrade rejection, recovery before initialization, and uninstall while retaining synthetic user data. The fixture uses distinct product identities and an isolated workspace directory; it never installs Maily or touches Outlook. It also checks the production managed custom action's per-user child-process context.
- Read-only MSI checks cover product identity/version, per-user scope, embedded cabinet bounds, file ownership and native action ordering. A successful fixture is not proof of a physical Maily install on every Windows/Outlook configuration.
- Updater tests cover consent, official release discovery, complete download hashes, MSI identity/version/size validation, fixed Windows Installer launch, cancellation, failure and restart outcomes. API/browser tests use synthetic feeds and installer boundaries.
- Existing reply, summary, attachment, language, pinned-pane refresh, signature, navigation and privacy regressions remain in the local gate. Mailbox interactions use synthetic data and mocks.

No hosted CI or paid service is used. Fresh Microsoft/tenant consent, all Outlook variants and complete accessibility are not certified. One earlier model HTTP400 remains unexplained despite successful historical follow-ups. The installer is unsigned; checksums are not independent publisher authentication. Windows and Microsoft can still require interactive approval.

[Install, repair and remove](INSTALLER.md) · [Release notes and limitations](RELEASE_NOTES_1.3.10.md).
