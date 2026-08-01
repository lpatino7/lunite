# CERTUS

**An honest PC check-up.** Certus reads your Windows machine's real settings and hardware, scores what it actually verified, and says plainly what it could not read. It changes nothing without a yes, and every change the app itself applies is reversible with one button.

*Certus* is Latin for **certain, sure, settled** — that's the whole product: what it tells you about YOUR machine was checked on your machine, or it says so.

## Download

Grab the newest build from **[Releases](https://github.com/lpatino7/certus/releases/latest)** — download the `Certus-*-friend-kit.zip`, unzip to your Desktop, run `Certus.exe`.

- **Windows PCs only.** Open this page on your PC, not your phone.
- Windows will show a blue SmartScreen warning because the app is new and unsigned — hit **More info → Run anyway**. (A code-signing certificate is on the roadmap; until then the warning is Windows being properly cautious about new software, which we respect.)
- Every release lists its SHA-256 checksum. The app's built-in updater additionally verifies both the checksum and an RSA signature before any update can install.

## What it does

- Free check-up: ~23 verified checks across gaming / media / work, real measured numbers, and an honest "could not read" list instead of guesses.
- Flags factory-installed bloatware by name (detection only — removing stays in your hands, on Windows' own uninstall button).
- Never phones home. The only internet action is the update check, and only when you click it (or opt in to a launch check).
- Your reports stay on your PC. Nothing is uploaded, ever.

## Status

Private testing preview. Feedback that made every build so far came from real testers on real machines — if something confused you, that's a finding: say it.

---

© 2026 Luis. All rights reserved. This is a free testing preview; the binaries may not be redistributed, modified, or rehosted without permission.
