# Streemrz Dojo Releases

Official Windows release repository for **Streemrz Dojo**.

> This repository distributes compiled installer and update artifacts only.  
> The proprietary Streemrz Dojo application source code is not published here.

## Download

### Current pre-release

The current internal/public-preview build is:

- **Streemrz Dojo 1.0.0-alpha.2**
- Windows 10/11 x64
- Unsigned test build

Open the [Releases](https://github.com/streemrzdotcom/dojo-releases/releases) page and download:

```text
StreemrzDojoSetup.exe
```

The unsigned alpha installer may show a Windows **Unknown Publisher** or Microsoft Defender SmartScreen warning. Public production releases will be code-signed.

### Stable release

After Streemrz Dojo 1.0.0 is published as a stable release, the latest installer will be available at:

```text
https://github.com/streemrzdotcom/dojo-releases/releases/latest/download/StreemrzDojoSetup.exe
```

## What is Streemrz Dojo?

Streemrz Dojo is a desktop community, messaging, voice, video, screen-sharing and media application powered by the wider Streemrz ecosystem.

Streemrz.com remains the authority for:

- account identity and sign-in;
- Tier Memberships and capability entitlements;
- Direct Tegami conversations;
- Marketplace and billing;
- Dojo account and service integration.

## System requirements

- Windows 10 or Windows 11
- 64-bit x64 processor
- Internet connection
- Microphone for voice features
- Camera for webcam features
- Current Windows media and graphics drivers

## Installation

1. Download `StreemrzDojoSetup.exe` from the required GitHub Release.
2. Close any currently running Streemrz Dojo instance.
3. Run the installer.
4. Launch **Streemrz Dojo** from the desktop or Start Menu.
5. Sign in through the secure Streemrz.com browser flow.

The installer uses a per-user installation and normally does not require administrator elevation.

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

Users normally need only `StreemrzDojoSetup.exe`.

## Updates

Automatic application updates are being introduced during the alpha release cycle.

Until the updater is marked active in the release notes:

1. Close Streemrz Dojo.
2. Download the newer installer.
3. Run it over the existing installation.

Ordinary upgrades preserve the local encrypted session and application preferences.

## Pre-release warning

Alpha, beta and release-candidate builds are provided for testing. They may contain defects or incomplete behaviour.

Before reporting a problem, include:

- Streemrz Dojo version;
- Windows version;
- whether the build is installed or running in development mode;
- steps to reproduce;
- sanitised error output;
- whether voice, camera, screen sharing or attachments were involved.

Never publish access tokens, private messages, `.env` contents, cookies or billing information.

## Support and issue reporting

For ordinary product problems, use the support method published by Streemrz.

For security vulnerabilities, follow [SECURITY.md](SECURITY.md) and do **not** disclose the issue publicly.

## Privacy

Streemrz Dojo may process account, messaging, voice, video and media information as required to provide its features. Refer to the privacy and account controls published by Streemrz.com.

## Licensing

The installer and binaries are proprietary software owned by Streemrz.

Downloading or installing Streemrz Dojo does not grant permission to copy, modify, reverse engineer, redistribute, resell or publish the application except where applicable law expressly provides otherwise.

Third-party notices included with the installed application remain subject to their respective licences.

## Repository contents

This repository intentionally contains only:

- public release information;
- security and support guidance;
- GitHub Release metadata;
- compiled release assets.

It does not contain the Streemrz Dojo source tree.
