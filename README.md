# CERTUS

**An honest PC check-up for Windows.** Certus reads your machine's real settings and hardware, scores only what it actually verified, and says plainly what it could not read. It changes nothing without a yes, and every change the app itself applies is reversible with one button.

## Download and run

1. Get the newest Certus zip from **[Releases](https://github.com/lpatino7/certus/releases/latest)** (under *Assets*).
2. **Windows 10/11 PCs only** — open the link on your PC, not your phone. Unzip anywhere; the Desktop is fine.
3. Run `Certus.exe`. Windows will show a blue SmartScreen warning because the app is new and unsigned — click **More info → Run anyway**. (A code-signing certificate is on the roadmap; until then that warning is Windows being properly cautious about software it hasn't seen before.)
4. Click **RUN CHECK-UP**. The scan is read-only — nothing on your PC changes.

There is no installer. The app is one portable exe. It keeps its records beside itself and in your PC's local app data, everything it writes is listed on its About screen, and a wipe button there clears all of it.

You don't need administrator access. Three measurements — memory speed, drive speed, startup time — come from Windows' built-in benchmark and do need it; the report says when they were skipped and why, and offers a restart-with-access button.

## What a check-up covers

Roughly two dozen verified checks, reported in plain words:

- **Settings that cost you performance** — power plan, monitor refresh rate, mouse acceleration, background game recording, startup load (including programs set to start twice), screen sleep, network adapter power saving, graphics driver age.
- **Hardware truths** — RAM running below the speed the sticks themselves report as their rating, single-channel memory, old motherboard firmware, drive health and real free space, fast USB devices linked below their tier, damaged-cable tells on wired links (only after the adapter itself is verified capable of more).
- **Factory-installed extras** — trialware, adware, and fake "speed-up" tools, named exactly. Manufacturer utilities (fan control, RGB) are listed, never accused, and your active antivirus can never be called bloat, whatever the brand. Flagged items get a one-click assist that opens Windows' own uninstall list with the names copied to your clipboard — the removal click itself always stays yours.
- **Health first** — antivirus state, drive health warnings, the CPU speed-limit log (the quiet slowdowns firmware applies when a machine runs hot), unexpected power-loss history. Protect-before-optimize items never sell you a one-click fix.
- **Network reality** — double-router paths, who answers your DNS lookups, measured round-trip time to your router.
- **Sound** — the default microphone pick (Windows loves to quietly switch you back to a webcam mic).

Every check ends one of three ways: verified on this machine, flagged with the evidence, or honestly marked *could not read*. Unreadable checks are excluded from the scoring math and listed — never guessed.

## Scores

Three scores — Gaming, Media, Work — plus an overall, computed only from checks that were actually read on your machine. The report states what the number was computed from, including what it failed to read. Measured numbers come with verdicts judged against your actual hardware's class, not a generic ideal.

## Fixes — and the undo rule

The report separates what the app can fix with one click from what needs guided steps or a screwdriver. For one-click fixes: each one is listed with its own consent tick before anything runs, every applied change records its exact before-value, and the **WHAT CHANGED** screen lists every change with its own UNDO button. Guided and hardware items (BIOS settings, cables, dust) are explained step by step — the app never touches those itself.

## Your rulings

Any finding can be marked **"I know about this."** It stops counting against your score, stays listed, and stays watched: it comes back on its own if the evidence gets worse, and once a marked item reads clean the mark retires — so if that thing ever breaks again, you get told fresh instead of silence.

## Privacy

- Reports stay on your PC. **Nothing is uploaded, ever.** No server, no account, no telemetry.
- The app's only internet action is the update check — and only when you click it (or once at launch if you opt in; off by default, one untick turns it off).
- The shareable report copy masks your router's addresses. Crash notes mask your user folder name.

## Updates

**CHECK FOR UPDATES** lives on the About screen. A new build installs only after passing two gates: its SHA-256 checksum matches the published manifest, and its RSA signature verifies against the maker's key — a tampered or rehosted file cannot pass. The old build stays beside the new one as a fallback.

## Status

Free testing preview, under active development. Every release lists its SHA-256 checksum. If something confused you, that's a finding — say it.

---

© 2026 Luis. All rights reserved. This is a free testing preview; the binaries may not be redistributed, modified, or rehosted without permission.
