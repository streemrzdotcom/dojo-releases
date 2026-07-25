# Release Checklist

Use this checklist when publishing a Streemrz Dojo GitHub Release.

## Repository

- [ ] Repository is `streemrzdotcom/dojo-releases`.
- [ ] Repository visibility is Public.
- [ ] No proprietary source files are staged.
- [ ] No `.env`, token, secret, certificate private key or user-data file is staged.
- [ ] `README.md`, `SECURITY.md` and `SUPPORT.md` are current.

## Build

- [ ] Correct accepted frontend patch is checked out/applied.
- [ ] Required backend version is healthy.
- [ ] Required Streemrz.com authority version is healthy.
- [ ] Production `.env` values are validated without printing secrets.
- [ ] `npm ci` completed from `package-lock.json`.
- [ ] Renderer TypeScript passed.
- [ ] Electron TypeScript passed.
- [ ] Combined build passed.
- [ ] Installer build passed.
- [ ] Packaged runtime audit passed.
- [ ] `app.asar` contains only approved runtime roots.
- [ ] Installer and NUPKG size thresholds passed.

## Artifacts

- [ ] `StreemrzDojoSetup.exe`
- [ ] `StreemrzDojo-<version>-full.nupkg`
- [ ] `RELEASES`
- [ ] `SHA256SUMS.txt`
- [ ] `release-manifest.json`
- [ ] `installer-artifacts.json`
- [ ] Release notes prepared from `RELEASE_TEMPLATE.md`
- [ ] Every SHA-256 value was regenerated from the final immutable artifact.

## UAT

- [ ] Clean installation passed.
- [ ] No unexpected UAC request.
- [ ] Start Menu shortcut passed.
- [ ] Desktop shortcut passed.
- [ ] Warm OAuth passed.
- [ ] Cold-start OAuth passed.
- [ ] Single-instance behaviour passed.
- [ ] Session restoration passed.
- [ ] Logout persistence passed.
- [ ] Voice passed.
- [ ] Camera passed.
- [ ] Screen sharing passed.
- [ ] Attachments passed.
- [ ] Reactions passed.
- [ ] Custom title bar passed.
- [ ] Error notification policy passed.
- [ ] Apps & Features registration passed.
- [ ] Uninstall passed.
- [ ] Protocol removal after uninstall passed.

## Signing

- [ ] Internal alpha is explicitly marked unsigned, or:
- [ ] Executable is signed.
- [ ] Installer is signed.
- [ ] Signature verification passed.
- [ ] Timestamping passed.
- [ ] Publisher name is correct.

## GitHub release

- [ ] Tag uses `v<version>`.
- [ ] Release title is `Streemrz Dojo <version>`.
- [ ] Alpha/beta/RC is marked as a pre-release.
- [ ] Draft release created before assets are uploaded.
- [ ] All required assets uploaded.
- [ ] Release notes reviewed.
- [ ] Security warning and known limitations included.
- [ ] Downloaded assets were re-hashed after upload.
- [ ] Release published only after final approval.

## Automatic-update releases

- [ ] Previous installed version was tested.
- [ ] Update feed includes matching `RELEASES` and `.nupkg`.
- [ ] Background download passed.
- [ ] Restart and install passed.
- [ ] Update does not force restart during a call.
- [ ] Mandatory-update behaviour tested when applicable.
- [ ] Rollback/recovery route documented.

## Records

- [ ] Component patch notes appended.
- [ ] Conversation handover appended.
- [ ] Deployed patch record appended.
- [ ] Nexus build record appended.
- [ ] UAT acceptance date recorded.
- [ ] Rollback instructions retained.
