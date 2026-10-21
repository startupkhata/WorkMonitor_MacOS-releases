# WorkMonitor for macOS — releases

This repository hosts the public build artifacts (`.dmg`, `.zip`, `appcast.xml`) for [WorkMonitor](https://github.com/startupkhata/WorkMonitor_MacOS). The source code lives in that private repo.

## Install

Download the latest `.dmg` from the [Releases](../../releases) page, open it, and drag **WorkMonitor** into Applications.

## Auto-update

The app checks this repository hourly via Sparkle and installs new versions in place; no action needed after the first install.

## Verify a download

Every DMG is signed by **TEAMLIO PRIVATE LIMITED** (Apple Developer Team `KX786762M5`) and notarized by Apple:

```bash
codesign --verify --deep --strict --verbose=2 /Applications/mac-workflow.app
spctl --assess --type execute --verbose /Applications/mac-workflow.app
```

Both commands should report `accepted` / `source=Notarized Developer ID`.
