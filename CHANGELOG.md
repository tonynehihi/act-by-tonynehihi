# Changelog

## 1.1.0

First release of Acrobat by Tonynehihi (AcT), a personal build based on PdfCraft 0.8.0 by storytold.

- **IN-APP AUTO-UPDATE:** the app checks GitHub on launch and pops up the release notes; **Download & Install** builds the new version inside the app with live progress (the running version is untouched until the build succeeds), then **Finish Install** swaps it in and relaunches. The old version is kept as a backup under `~/Library/Caches/Acrobat by Tony/updates/backup`. This replaces upstream's own update check, which pointed at the upstream repo. Also available any time via **Help → Check for Updates** or the About window.
- **RENAMED TO AcT:** Finder, Spotlight and the Dock now show the short name **AcT**, matching the rest of the suite (LrT, PsT, AiT); inside the app it is still "Acrobat by Tonynehihi". Settings and data folders are unchanged.
- **UPSTREAM LINKS REMOVED:** the Help menu keeps only Check for Updates, Keyboard Shortcuts and About — the Discord, website, GitHub and app-page entries are gone. The start screen's community card and the top bar's Discord button are gone too — nothing in the app points back to the upstream project anymore.
- **NEW ADOBE-STYLE ICON:** red #EC1C24 panel with white "Ac" lettering, matching the suite's identity.
- Everything else is PdfCraft 0.8.0 as released by storytold; AcT tracks the upstream project and folds its new features into future releases.

— tonynehihi
