# eyes-ios-release

Builds the Eyes iPhone app as an ad hoc release from [ayaangazali/eyes](https://github.com/ayaangazali/eyes) (`apps/mobile`, `scripts/adhoc-release.ts`). Runs when the Eyes API reports a newly registered iPhone (`repository_dispatch: device-registered`), hourly as a backstop, or by hand (Actions → adhoc-release → Run workflow; dry run by default).

Secrets: `ASC_KEY_ID`, `ASC_ISSUER_ID`, `ASC_KEY_P8` (App Store Connect API key, Admin), `CERT_DEV_P12`, `CERT_DIST_P12`, `P12_PASSWORD` (Apple Development + Apple Distribution, created through the API), `INSFORGE_BASE_URL`, `INSFORGE_API_KEY`, `INKBOX_API_KEY`, `INKBOX_AGENT_HANDLE`.
