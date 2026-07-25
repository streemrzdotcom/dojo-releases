# Streemrz Dojo <VERSION>

> Replace every placeholder before publishing this release.

## Release status

- Channel: `<alpha | beta | rc | stable>`
- Public version: `<VERSION>`
- Dojo frontend patch: `<p4e...>`
- Required Dojo backend: `<p4e...>`
- Required Streemrz.com authority: `<p4e...>`
- Nexus reference: `<NX-...>`
- Released: `<YYYY-MM-DD>`

## Summary

<One-paragraph customer-facing summary.>

## Highlights

- <Highlight>
- <Highlight>
- <Highlight>

## Fixes

- <Fix>
- <Fix>

## Known limitations

- <Limitation or “None currently documented.”>

## Windows download

Download:

```text
StreemrzDojoSetup.exe
```

System:

```text
Windows 10/11 x64
```

## Verify the installer

```powershell
Get-FileHash .\StreemrzDojoSetup.exe -Algorithm SHA256
```

Compare the value against `SHA256SUMS.txt`.

## Upgrade notes

- Close Streemrz Dojo before running the installer.
- Ordinary upgrades preserve the encrypted session and local preferences.
- <Any version-specific upgrade note.>

## Compatibility

| Component | Required version |
|---|---|
| Streemrz Dojo frontend | `<p4e...>` |
| Dojo backend | `<p4e...>` |
| Streemrz.com | `<p4e...>` |
| Windows | Windows 10/11 x64 |

## Release assets

- `StreemrzDojoSetup.exe`
- `StreemrzDojo-<VERSION>-full.nupkg`
- `RELEASES`
- `SHA256SUMS.txt`
- `release-manifest.json`
- `installer-artifacts.json`

## Security

Report vulnerabilities privately according to [SECURITY.md](SECURITY.md).

Do not publish access tokens, private messages, `.env` values or personal information in release comments.
