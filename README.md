# Streemrz Dojo Releases

Official Windows release repository for **Streemrz Dojo**.

> This repository distributes compiled installer and update artifacts only.  
> The proprietary Streemrz Dojo application source code is not published here.

## Download

### Current pre-release

The current prepared Production beta build is:

- **Streemrz Dojo 1.0.0-beta.20260805.1422.1**
- Windows 10/11 x64
- Per-user Squirrel.Windows installer
- Unsigned beta/test build

Open the [Releases](https://github.com/streemrzdotcom/dojo-releases/releases) page and download:

```text
StreemrzDojoSetup.exe
```

Unsigned preview installers may show a Windows **Unknown Publisher** or Microsoft Defender SmartScreen warning. Public stable releases are intended to be code-signed.

### Stable release

After Streemrz Dojo 1.0.0 is published as a stable release, the latest installer will be available at:

```text
https://github.com/streemrzdotcom/dojo-releases/releases/latest/download/StreemrzDojoSetup.exe
```

## What is Streemrz Dojo?

Streemrz Dojo is a Windows desktop community, messaging, voice, video, screen-sharing and media application powered by the wider Streemrz ecosystem.

A Dojo can contain:

- categories and text channels;
- voice channels;
- Showcase theatres;
- roles and role-based channel access;
- Direct Tegami conversations;
- media, soundboards, emotes and attachments;
- resident management and moderation tools;
- Support and Suggestions ticketing.

Streemrz.com remains the authority for:

- account identity and secure sign-in;
- Tier Memberships and capability entitlements;
- Direct Tegami authority and account integration;
- Marketplace, billing and connected Streemrz services;
- Production and Development environment separation.

## Latest beta highlights

### Messaging and chat

- Safe Markdown rendering for:
  - bold, italic, strikethrough and inline code;
  - fenced code blocks;
  - blockquotes;
  - compact headings;
  - lists and horizontally scrolling tables;
  - safe HTTP, HTTPS, mail and telephone links.
- Raw HTML execution is disabled.
- Unsafe link protocols and external Markdown images are blocked.
- Messages remain stored as plain Markdown text rather than pre-rendered HTML.
- `Enter` sends a message.
- `Shift+Enter` inserts a new line.
- Message length is limited to 8,000 characters.
- Direct Tegami, native Dojo messages and channel chat are kept separate between Development and Production environments.
- Active Direct Tegami conversations use a faster bounded refresh cycle.
- Visible and background message refresh intervals have been reduced.
- Duplicate and replayed notifications are suppressed.

### Native Windows notifications

- Native Windows toast notifications.
- Resident avatars and Dojo fallback artwork.
- Safe plain-text message previews.
- Click-to-open Direct Tegami and Dojo channels.
- Notification Center and cold-start activation support.
- Inline reply support for Direct Tegami notifications.
- Selectable Windows notification sounds.
- Bundled Dojo notification sounds.
- Optional imported local notification sound.
- Per-user notification preferences and preview privacy controls.

A custom local sound is played by the Dojo application while the associated Windows toast is submitted silently. Windows-native sound selections continue to use the Windows notification audio system.

### Voice, video and devices

- Microphone, speaker and camera selections persist between sessions.
- Input-device changes replace the active microphone track during a call.
- Output-device changes are applied to existing and newly created call audio elements.
- Push to Talk input mode with configurable multi-key shortcuts.
- Voice Activity remains available.
- Voice-channel capacity can follow the Sensei's current Tier or Dojo allowance automatically.
- Custom per-channel limits remain available up to the permitted maximum.
- Voice-channel titles show current and maximum occupancy, for example:

```text
General Voice                                      (2/10)
```

- Capacity is shown in green while places remain and red when full.
- Full-channel admission is enforced by the backend.
- Voice-join acknowledgement no longer waits on remote entitlement refresh.

Push to Talk currently uses keyboard input received by the Dojo application. System-wide background keyboard capture may depend on the installed build and operating-system permissions.

### Roles and Dojo management

- Consolidated **Edit Channel** workflow.
- Category and text-channel editing includes:
  - change name;
  - role access.
- Voice and Showcase editing includes:
  - change name;
  - role access;
  - user limit.
- Resident roles can be managed from resident and Dojo-message context menus.
- Selecting the Sensei role starts the protected ownership-transfer process.
- Ownership transfer uses a Dojo-styled confirmation dialog.
- Sensei and Students retain immutable backend identities but can have editable frontend display aliases.
- Role aliases are used throughout the visible Dojo interface without changing permissions or ownership rules.

### Staff Area, Support and Suggestions

- **Staff Moderation** has been renamed to **Staff Area**.
- User Settings includes:
  - **Support**;
  - **Suggestions**.
- Support and Suggestion submissions receive numbered tickets.
- Ticket status and history are retained.
- Staff can review and update tickets through Staff Area.
- Users receive in-app and Windows notification updates when a ticket changes.
- Staff inspection remains controlled, audited and read-only where required.

### Showcase improvements

- Showcase participant lists now display only residents currently present in the selected theatre.
- Dojo residents who are not in the theatre are no longer incorrectly listed as participants.

### Security and environment isolation

- Development and Production Dojo installations use separate:
  - backend domains;
  - OAuth clients and callback protocols;
  - service credentials;
  - application identities;
  - Windows notification identities;
  - local storage and user-data paths;
  - Direct Tegami environment boundaries.
- Raw HTML, script execution and unsafe Markdown links are blocked.
- Notification payloads do not contain authentication tokens.
- Custom audio is copied into Dojo-controlled local storage rather than depending on the original source file.
- Production and Development data are not intentionally interchangeable.

## System requirements

- Windows 10 or Windows 11
- 64-bit x64 processor
- Internet connection
- Microphone for voice features
- Camera for webcam features
- Current Windows media, audio and graphics drivers
- Windows notifications enabled for Streemrz Dojo when desktop alerts are required

## Installation

1. Download `StreemrzDojoSetup.exe` from the required GitHub Release.
2. Close any currently running Streemrz Dojo instance, including its tray process.
3. Run the installer.
4. Launch **Streemrz Dojo** from the desktop or Start Menu.
5. Sign in through the secure Streemrz.com browser flow.

The installer uses a per-user installation and normally does not require administrator elevation.

Ordinary upgrades are designed to preserve the local encrypted session and application preferences. A release note may request a fresh sign-in when authentication or account-integration changes are included.

## Verify a download

Each release includes `SHA256SUMS.txt`.

From PowerShell:

```powershell
Get-FileHash .\StreemrzDojoSetup.exe -Algorithm SHA256
```

Compare the output with the matching entry in `SHA256SUMS.txt`.

Do not install a file whose hash does not match.

## Release assets

A Windows release may contain:

| Asset | Purpose |
|---|---|
| `StreemrzDojoSetup.exe` | Windows installer |
| `StreemrzDojo-<version>-full.nupkg` | Squirrel.Windows application/update package |
| `RELEASES` | Squirrel.Windows update metadata |
| `SHA256SUMS.txt` | SHA-256 verification manifest |
| `release-manifest.json` | Application and component release metadata |
| `installer-artifacts.json` | Machine-readable artifact inventory |
| `packaged-runtime-audit.json` | Packaged application integrity summary |

Users normally need only `StreemrzDojoSetup.exe`.

## Updates

Automatic application updates are being introduced during the beta release cycle.

Until a release note explicitly states that the Production updater is active:

1. Close Streemrz Dojo, including its tray process.
2. Download the newer installer.
3. Run it over the existing installation.
4. Launch Dojo and confirm the version shown in the application.

Do not install Development builds over the Production application. Development and Production use separate application identities and should remain installed side by side only when explicitly required for testing.

## Preview limitations

Alpha, beta and release-candidate builds are provided for testing. They may contain defects, incomplete behaviour or temporary operational limits.

Known preview considerations include:

- Direct Tegami depends on the active Streemrz OAuth session.
- A long-running session may require signing in again when its messaging access expires.
- User-imported notification sounds are application-played and may not follow Windows Focus Assist exactly like native Windows sounds.
- Push to Talk background behaviour may vary according to focus and operating-system keyboard permissions.
- Unsigned installers may trigger Windows reputation warnings.
- Automatic Production updates may remain disabled until announced in the release notes.

## Support and issue reporting

Use **User Settings → Support** inside Streemrz Dojo for ordinary product problems.

Use **User Settings → Suggestions** for ideas and enhancement requests.

When reporting a problem, include:

- Streemrz Dojo version;
- Windows version;
- whether the build is installed or running in development mode;
- steps to reproduce;
- sanitised error output;
- whether messaging, notifications, voice, camera, screen sharing or attachments were involved.

Never publish:

- OAuth or access tokens;
- private messages;
- `.env` contents;
- cookies;
- service credentials;
- billing information;
- private keys or certificates.

For security vulnerabilities, follow [SECURITY.md](SECURITY.md) and do **not** disclose the issue publicly.

## Privacy

Streemrz Dojo may process account, messaging, voice, video, media, support and suggestion information as required to provide its features.

Windows notification previews may display sender and message information according to the user's notification privacy settings.

Refer to the privacy and account controls published by Streemrz.com.

## Licensing

The installer and binaries are proprietary software owned by Streemrz.

Downloading or installing Streemrz Dojo does not grant permission to copy, modify, reverse engineer, redistribute, resell or publish the application except where applicable law expressly provides otherwise.

Third-party notices included with the installed application remain subject to their respective licences.

## Repository contents

This repository intentionally contains only:

- public release information;
- security and support guidance;
- GitHub Release metadata;
- compiled release assets;
- release verification manifests.

It does not contain the Streemrz Dojo source tree, service credentials, private infrastructure configuration or database content.
