# Maily 1.3.10 installation, repair and removal

## Before you start

Use Windows x64 and classic Outlook desktop. New Outlook, macOS and Outlook on the web are not supported. Maily reuses a compatible, signed-in ChatGPT desktop app with Codex features; it does not install ChatGPT or a second AI runtime. Obtain organizational permission before processing work email.

Download **MailyOutlookAddin-1.3.10.0.msi** from the official Releases page. It is one installer: double-click it without extracting anything. The optional SHA256 file lets you check download consistency with `Get-FileHash <download.msi> -Algorithm SHA256`. This release is unsigned; a matching checksum does not independently authenticate the publisher.

## Install or upgrade

1. Save drafts and finish inline replies. Read and accept the responsibility notice in the MSI, then choose Install.
2. Setup checks the existing installation, closes Maily's services and closes Outlook normally before replacing files. Answer any Outlook save prompts. Setup stops safely if Outlook cannot close; it never force-kills Outlook.
3. Setup installs for your Windows account, preserves settings and existing sign-in, configures Maily's local service, and refreshes only Maily-owned Outlook registration/cache entries. Windows may require approval to trust Maily's localhost HTTPS certificate on first installation. Windows and Microsoft security prompts remain under your control.
4. Leave **Open Maily's Outlook connection guide** selected on the final screen. The guide checks existing local Outlook registration first. Use **Check connection** to open Outlook and verify readiness. If connection is still required, choose **Sign in and connect** explicitly and handle Microsoft's account selection, consent or administrator requirements.
5. Open Maily in Outlook. In Settings, choose **Show quick tour**. Style learning is optional and starts only when you request it.

An existing compatible local registration is reused. You should not need to remove and add Maily after an ordinary version update. A mailbox-installed or organization-managed add-in is separate from the local installation; setup reports ownership conflicts rather than deleting another registration. Local cache cleanup cannot establish mailbox registration or pane visibility.

The default directory is `%LOCALAPPDATA%\Maily\OutlookAddin`. Maily includes its own .NET application runtime and Microsoft connection tooling. The MSI uses the standard .NET Framework 4.8 Windows component; update Windows if it is missing. No SDK, Node, developer tools, separate Codex installation or archive extraction is required.

## Repair and updates

Run the **same MSI again** and choose Repair. You can also open **Maily Outlook Add-in** from Start and choose **Repair or remove Maily**. Windows Settings provides Uninstall; its Repair option is not available on every Windows version. Repair restores the installed version's files and local configuration. It does not automatically start Microsoft consent or require ChatGPT sign-in merely to recover local files.

Install a newer MSI to upgrade. Windows Installer owns file replacement and rollback. If setup fails or is cancelled, keep the installer and diagnostics; the transaction attempts to restore the previous files and local integration. A newer installed version cannot be replaced by an older MSI. Run one setup or removal at a time. Windows Installer serializes native MSI maintenance; do not start an older extracted ZIP setup while an MSI transaction is running.

**Moving from 1.3.9 or earlier:** install this MSI manually once. The older updater understands ZIP packages and cannot install an MSI-only release. From 1.3.10 onward, Maily's update banner verifies the new MSI and launches Windows Installer after your confirmation. Save drafts before confirming. A launch alone is not reported as completed installation; cancellation, failure and a required restart are shown separately.

## Uninstall and reinstall

Save drafts, then use **Windows Settings > Apps > Installed apps > Maily Outlook Add-in > Uninstall**, or run the MSI again and choose Remove. Outlook closes normally before Maily's local components are removed. Missing ChatGPT, Outlook or optional Maily metadata does not block local removal. Maily removes only its own local startup and registration entries; foreign or administrator-managed entries are left intact.

Normal removal retains your settings, logs, Maily's Microsoft session and its already trusted private localhost certificate for reinstall. Shared ChatGPT/Codex sign-in is retained. The user-data directory can therefore remain after uninstall; this does not mean the application is still installed. Uninstall does not undo sent mail or previous edits to drafts.

An account-installed Outlook copy can remain visible after local removal. Remove that copy through Outlook's add-in management if you want it removed; organization-managed copies require the administrator. Setup does not claim that deleting a local cache removed an account deployment. Reinstall by double-clicking the MSI, then check the existing connection before signing in again.

## Troubleshooting

- **Outlook will not close:** finish inline replies, answer save prompts and close other setup windows, then retry. Do not force-terminate Outlook to bypass this guard.
- **Maily is missing:** open the Maily Start-menu guide and Check connection. Local file installation and mailbox registration have separate results. Use the supported connection or administrator route if needed.
- **A connection check failed after installation:** check again in the guide instead of reinstalling. Verification has its own diagnostic record and preserves the original installation result.
- **Sign-in or models unavailable:** open/update ChatGPT and sign in there. Refresh the model list in Maily Settings. Availability depends on your account; prefer Automatic unless you need a specific supported model.
- **Setup failed:** retain the MSI log and `%LOCALAPPDATA%\Maily\MsiTransactions` diagnostics. Share only redacted error codes and synthetic reproduction steps. Do not post configuration, credentials or mailbox contents.

AI can be inaccurate. You are responsible for reviewing all output and actions before use and following your organization's data and AI policies. Maily never sends automatically. See [the responsibility notice](DISCLAIMER.md).
