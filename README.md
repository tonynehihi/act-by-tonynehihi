<p align="center">
  <img src="assets/app-icon/act-icon-1024.png" width="128" alt="AcT icon">
</p>

<h1 align="center">Acrobat by Tonynehihi</h1>

<p align="center">
  <b>A PDF workbench — a personal fork of PdfCraft, rebuilt in pure Rust.</b><br>
  Runs natively on macOS, Windows and Linux, and in the browser via WebAssembly.
</p>

## Origin

This is a personal fork of [PdfCraft](https://github.com/storytold/pdfcraft) by the storytold (ArtCraft) team — an open-source, clean-room reimplementation of the Adobe Acrobat workflow. All credit for the application itself goes to the upstream authors; this fork only rebrands it and adds a self-update flow for one person's machines.

"Acrobat" is a trademark of Adobe Inc. This project is not affiliated with or endorsed by Adobe.

## What Tony changed

- **Name:** "Acrobat by Tonynehihi" inside the app; the macOS bundle is **AcT.app** (bundle id `com.tony.acrobat`) so Finder/Spotlight show the short name like the rest of the suite (LrT, PsT, AiT, …). Settings/data folders are unchanged from the upstream layout.
- **In-app auto-update:** on launch the app checks this repo's GitHub releases, shows the changelog in a pop-up, and — on macOS — downloads the source and builds the new version inside the app with live progress, then swaps it in and relaunches (the old version is kept as a backup). Also available any time via **Help → Check for Updates** or the About window. This replaces upstream's own update check, which pointed at the upstream repo.
- **Cleaned-up info surfaces:** the Help menu, the start screen and the top bar no longer link to the upstream project's Discord, website or GitHub.
- **Icon:** Adobe-style suite icon (red #EC1C24 panel, white "Ac").

## Installing on macOS

See the step-by-step guide (Vietnamese): [packaging/macos/HUONG-DAN.md](packaging/macos/HUONG-DAN.md). In short: build from source with `cargo build --release -p pdfcraft`, then `packaging/macos/package.sh --arch aarch64`, open the DMG in `dist/release/` and drag **AcT.app** into Applications. The 1.1.0 release is a one-time manual install; later versions update themselves from inside the app.

## License

MIT OR Apache-2.0, same as upstream.
