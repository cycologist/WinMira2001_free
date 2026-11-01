# WINMIRA 2001 — Free Full Version

Pre-built binaries for **WINMIRA 2001**, the free full version of the Free Pascal / Lazarus port.

Registration, the serial-number generator and demo mode have been removed. The program always runs with the full-version limits (100000 persons, 256 items, 30 categories, 199 latent classes) and does not access the Windows registry. Defaults are stored in a plain `winmira.ini` file.

## Download

Go to the [latest release](https://github.com/cycologist/WinMira2001_free/releases/latest) and download the file for your platform:

| Platform | File |
| --- | --- |
| Linux x86-64 | `winmira2001-linux-x86_64` |
| Windows x86-64 | `winmira2001-windows-x86_64.exe` |
| macOS Intel | `WINMIRA-2001-macos-x86_64.zip` or `winmira2001-macos-x86_64` |
| macOS Apple Silicon | `WINMIRA-2001-macos-arm64.zip` or `winmira2001-macos-arm64` |
| Documentation | `WINMIRA-2001-help.zip` |

`SHA256SUMS` contains the SHA-256 checksums for every asset.

## HTML help / user manual

`WINMIRA-2001-help.zip` contains the original HTML user manual plus the printable PDF version (`winmiramanual.pdf`). Extract it and open `help/index.html` in any web browser. The HTML pages are self-contained; no web server is needed.

On Windows and Linux, place the extracted `help` folder next to the WINMIRA executable. On macOS, place it next to **WINMIRA 2001.app**.

The in-app **Help → Contents** menu entry in the current binaries still shows the port's placeholder message; use `help/index.html` directly.

The macOS `.zip` files contain a ready-to-run **WINMIRA 2001.app** bundle. The raw Mach-O executables are provided for advanced users.

## macOS notes

The macOS bundles are ad-hoc signed but **not notarized**, so Gatekeeper warns on first launch. Right-click **WINMIRA 2001.app** and choose **Open**, or remove the quarantine flag from a terminal:

```sh
xattr -dr com.apple.quarantine "WINMIRA 2001.app"
```

The Apple Silicon build is native arm64; it does not need Rosetta. The Intel build is native x86-64.

Both macOS builds use the Cocoa widgetset and include the fixes for:

- showing the ASCII import dialog **before** the data window is created, and
- loading the imported data into the grid without relying on Cocoa's missing MDI implementation.

## Verifying downloads

```sh
sha256sum -c SHA256SUMS
```

On macOS the same command works with `shasum -a 256 -c SHA256SUMS`.

## Version

1.45 — free full version.
