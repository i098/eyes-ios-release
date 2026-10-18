# eyes-ios-release

Builds the Eyes iPhone app as an ad hoc release from [ayaangazali/eyes](https://github.com/ayaangazali/eyes) (`apps/mobile`, `scripts/adhoc-release.ts`). Runs when the Eyes API reports a newly registered iPhone (`repository_dispatch: device-registered`), hourly as a backstop (a Linux job starts the macOS build only when an iPhone waits), or by hand (Actions → Ad hoc release → Run workflow; dry run by default).

Secrets: `RELEASE_ENV` (InsForge, Inkbox, App Store Connect key and issuer ids), `ASC_P8` (App Store Connect API key), `DIST_P12` + `P12_PASSWORD` (Apple Distribution certificate, created through the App Store Connect API). Logs show UDIDs cut to 6 characters and no phone numbers.
