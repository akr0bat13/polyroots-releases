# Publication checklist (one release, one platform)

1. Source commit approved and tagged in the private repository; tests green.
2. Artifact built **by the release workflow** (never a local or debug build) and verified: macOS = Developer ID + hardened runtime + notarization + Gatekeeper; Android = release-signed APK, package `app.lpr.wallpaper`, versionCode higher than the last release.
3. `scripts/release/prepare_hosting.py` ran without `REFUSED` (it re-checks the evidence against the file hash). Review the generated folder.
4. Create the **draft** GitHub release in this repository with the generated files (command printed by the script). Do not publish yet.
5. Register the draft in the backend (`polyroots-admin release-create` / `release-attach` with the hosted file URL) and run `release-validate` (production re-verifies the downloaded bytes with the real tools).
6. Review `release-show`; check the notes in English and Russian.
7. Publish the GitHub release (so the URL is public), then `release-publish` (dry run first) and `--confirm`.
8. Verify: the bot's Download section shows the version, the link downloads the same SHA-256, "Get file in Telegram" delivers it.
9. Separately and only with explicit approval: `campaign-preview` → review recipients and text → `campaign-create --confirm`.
