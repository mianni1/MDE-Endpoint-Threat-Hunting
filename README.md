# MDE Endpoint Threat Hunting

KQL queries for threat hunting with Microsoft Defender for Endpoint (MDE).

### How to Use the macOS Queries

1. **Suspicious Terminal Commands**
   - **What it does:** Tracks sketchy terminal commands like `rm -rf`, `curl`, etc.
   - **Tweak it:** Add or remove commands in the `has_any` part.

2. **Unusual Network Connections**
   - **What it does:** Hunts for weird outbound connections on sensitive ports.
   - **Tweak it:** Change the `LocalPort` values.

3. **Suspicious Applications Execution**
   - **What it does:** Detects running of apps like AnyDesk, TeamViewer, etc.
   - **Tweak it:** Add or remove app names in `FileName`.

4. **New User Creation**
   - **What it does:** Spots new local user accounts being created.
   - **Tweak it:** Mostly good to go as is.

5. **Sensitive File Changes**
   - **What it does:** Monitors changes in critical directories like `/etc` and `/var`.
   - **Tweak it:** Add other sensitive directories in `FolderPath`.

6. **Script Executions in User Directories**
   - **What it does:** Detects scripts executed from user directories.
   - **Tweak it:** Adjust `FolderPath` and script file extensions in `FileName`.

7. **Sudo Command Usage**
   - **What it does:** Tracks usage of `sudo` commands.
   - **Tweak it:** Adjust command keywords in `ProcessCommandLine`.

8. **Suspicious Browser Activity**
   - **What it does:** Looks for suspicious browsing activity.
   - **Tweak it:** Add/remove URLs in `RemoteUrl`.

9. **New Profile Installations**
   - **What it does:** Monitors new profile installations.
   - **Tweak it:** This one’s ready to go.

10. **App Permission Changes**
    - **What it does:** Detects changes in app permissions.
    - **Tweak it:** This one’s good as is.

11. **Suspicious Processes**
    - **What it does:** Spots suspicious processes running on the device.
    - **Tweak it:** Add/remove process names in `ProcessName`.

12. **Security Breaches**
    - **What it does:** Flags security breaches.
    - **Tweak it:** Ready to use.

13. **Suspicious Domains**
    - **What it does:** Tracks visits to suspicious domains.
    - **Tweak it:** Add/remove domains in `RemoteUrl`.

14. **Private Folder Changes**
    - **What it does:** Monitors changes in private directories.
    - **Tweak it:** Adjust the `FolderPath` as needed.

15. **Scheduled Task Creations**
    - **What it does:** Detects creation of scheduled tasks.
    - **Tweak it:** Add/remove task managers in `FileName`.

Happy hunting! 🕵️‍♂️🔍