# eyes-ios-release

Builds the Eyes iPhone app as an ad hoc release from [ayaangazali/eyes](https://github.com/ayaangazali/eyes) (`apps/mobile`, `scripts/adhoc-release.ts`). Runs every 5 minutes (a Linux job starts the macOS build only when an iPhone waits), on `repository_dispatch: device-registered`, or by hand (Actions → Ad hoc release → Run workflow; dry run by default). Set the repository variable `DRY_RUN` to `true` to make every run a dry run (nothing registered, uploaded or texted).

Secrets: `RELEASE_ENV` (InsForge, Inkbox, App Store Connect key and issuer ids), `ASC_P8` (App Store Connect API key), `DIST_P12` + `P12_PASSWORD` (Apple Distribution certificate, created through the App Store Connect API). Logs show UDIDs cut to 6 characters and no phone numbers.
