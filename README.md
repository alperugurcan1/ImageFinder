# ImageFinder

Minimal Windows app: type a word (e.g., "horse"), press Enter, and the image appears on your desktop. Ctrl+Q to show/hide.

## Features

- Type a keyword and press Enter to download a matching image
- Images saved to your Desktop
- Ctrl+Q global shortcut to show/hide the window
- Simple, minimalist interface

## Prerequisites

- [Node.js](https://nodejs.org/)
- [Rust](https://rustup.rs/)
- [Visual Studio Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) (Windows)

## Run

```bash
npm install
npm run tauri dev
```

## Build

```bash
npm run tauri build
```

Output: `src-tauri/target/release/bundle/msi/` (MSI installer)

## Code Signing

**No certificate?** Run the included script—it creates a self-signed cert and signs the build:

```bash
npm run tauri build
.\sign.ps1
```

For Microsoft Store, you need a paid certificate. See [CODE_SIGNING.md](CODE_SIGNING.md) for details.

## Microsoft Store Build

```bash
npm run tauri:store
```

Or manually:

```bash
npm run tauri build -- --no-bundle
npm run tauri bundle -- --config src-tauri/tauri.microsoftstore.conf.json
```

## Links

- [Privacy Policy](PRIVACY_POLICY.md)
- [Code Signing Guide](CODE_SIGNING.md)
