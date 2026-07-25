# Streemrz Dojo 1.0.0-alpha.2

## Release status

- Channel: **Internal/public preview alpha**
- Public version: **1.0.0-alpha.2**
- Dojo frontend lineage: **p4e306ra / p4e306rb installer foundation**
- Required Dojo backend: **p4e305c12**
- Required Streemrz.com authority: **p4e630a**
- Nexus reference: **NX-2026-015B**
- Signing: **Unsigned test build**

## Summary

This release is the first installable Windows build of Streemrz Dojo. It is intended for installer, packaged OAuth, session persistence and full desktop application UAT before automatic updates and production signing are enabled.

## Highlights

- Native Windows x64 installer.
- Desktop and Start Menu shortcuts.
- Packaged `com.streemrz.dojo://` OAuth callback.
- Encrypted desktop session storage.
- Contextual custom title bar.
- Centred error notifications.
- Voice, camera and screen sharing.
- Protected image, audio and video attachments.
- Dojo and Streemrz reaction synchronisation.
- Monthly and yearly Streemrz Tier support through the wider Streemrz authority.

## Installer warning

This alpha build is unsigned. Windows may display **Unknown Publisher** or a Microsoft Defender SmartScreen warning.

Do not redistribute this alpha as a final public production build.

## Download

Download:

```text
StreemrzDojoSetup.exe
```

## Verify

```powershell
Get-FileHash .\StreemrzDojoSetup.exe -Algorithm SHA256
```

Compare the result against `SHA256SUMS.txt`.

## UAT focus

- Installation without administrator elevation.
- Installed launch without VS Code or Vite.
- Warm and cold OAuth callback handling.
- Login-session restoration.
- Persistent logout.
- Voice, camera and screen sharing.
- Microphone test meters.
- Attachments and media playback.
- Reactions in both directions.
- Apps & Features registration.
- Uninstall and protocol cleanup.

## Known limitations

- Automatic updates are not yet enabled.
- The build is not code-signed.
- Windows x64 is the only supported installer target.
- Additional Dojo Kai regions and cross-Kai federation are not included in this release.

## Required compatibility

| Component | Required version |
|---|---|
| Dojo frontend | p4e306ra/p4e306rb lineage |
| Dojo backend | p4e305c12 |
| Streemrz.com | p4e630a |
| Windows | Windows 10/11 x64 |

## Security

Report security issues privately according to [SECURITY.md](SECURITY.md).
