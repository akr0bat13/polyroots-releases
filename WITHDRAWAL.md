# Withdrawing a release

1. `polyroots-admin release-withdraw --release <id>` (dry run) then `--confirm`: the release disappears from the bot, the app's update check and the download redirect immediately; pending notifications for it are not sent; cached Telegram file references stop being delivered.
2. Then, if appropriate, edit the GitHub release (mark as pre-release / add a warning) or delete the asset. A changed binary is never an edit: publish a new version.
3. Limits: files users already downloaded or received in Telegram cannot be recalled; deleting the hosted asset does not delete Telegram's copies. Say so in the release page if the reason is security.
