# LUNITE

**An honest PC check-up for Windows.** Lunite reads your machine's real settings and hardware, scores only what it actually verified, and says plainly what it could not read. It changes nothing without a yes, and every change the app itself applies is reversible with one button.

> **Certus is now Lunite.** Same app, same records, same checks — the old name was shared with several other software companies, so people searching for us found them instead. Copies already installed keep updating through the same signed channel; the old address still reaches us. Older releases below still carry the Certus name, because that is who published them.

## Download and run

1. Download **`Lunite.exe`** from **[Releases](https://github.com/lpatino7/lunite/releases/latest)** (under *Assets*). There is no zip and no installer — the app is one portable exe.
2. **Windows 10/11 PCs only** — open the link on your PC, not your phone. Save it anywhere; the Desktop is fine.
3. Run it. Windows will show a blue SmartScreen warning — click **More info → Run anyway**.
4. Click **RUN CHECK-UP**. The check-up itself is read-only: it changes nothing on your PC. Changes happen only later, on the FIX screen, one tick at a time, and every one of them has its own UNDO.

You don't need administrator access. Three measurements — memory speed, drive speed, startup time — come from Windows' built-in benchmark and do need it; the report says when they were skipped and why, and offers a restart-with-access button.

### About that SmartScreen warning

It is Windows being properly cautious, and it will happen. The app is not code-signed yet, so Windows has no publisher name to show you and no download history to judge it by. The rename reset what little reputation the old name had earned, so expect the warning to stick around for a while. A signing certificate is on the roadmap.

That warning means *"I don't know who made this"* — not *"I found something bad."* If that distinction isn't enough for you, don't run it. That's a reasonable call, and the next section is there so you don't have to take anyone's word for it.

### Verify what you downloaded

Every release publishes the SHA-256 of its exe in the release notes. To check yours matches, in PowerShell:

```
Get-FileHash .\Lunite.exe -Algorithm SHA256
```

Compare it to the hash in the [release notes](https://github.com/lpatino7/lunite/releases/latest). If they differ, don't run it — tell me.

## What a check-up covers

Roughly two dozen verified checks, reported in plain words:

- **Settings that cost you performance** — power plan, monitor refresh rate, mouse acceleration, background game recording, startup load (including programs set to start twice), screen sleep, network adapter power saving, graphics driver age.
- **Hardware truths** — RAM running below the speed the sticks themselves report as their rating, single-channel memory, old motherboard firmware, drive health and real free space, fast USB devices linked below their tier, damaged-cable tells on wired links (only after the adapter itself is verified capable of more).
- **Factory-installed extras** — trialware, adware, and fake "speed-up" tools, named exactly. Manufacturer utilities (fan control, RGB) are listed, never accused, and your active antivirus can never be called bloat, whatever the brand.
- **Health first** — antivirus state, drive health warnings, the CPU speed-limit log (the quiet slowdowns firmware applies when a machine runs hot), unexpected power-loss history. Protect-before-optimize items never sell you a one-click fix.
- **Network reality** — double-router paths, who answers your DNS lookups, measured round-trip time to your router.
- **Sound** — the default microphone pick (Windows loves to quietly switch you back to a webcam mic).

Every check ends one of three ways: verified on this machine, flagged with the evidence, or honestly marked *could not read*. Unreadable checks are excluded from the scoring math and listed — never guessed.

## Scores

Three scores — Gaming, Media, Work — plus an overall, computed only from checks that were actually read on your machine. The report states what the number was computed from, including what it failed to read. Measured numbers come with verdicts judged against your actual hardware's class, not a generic ideal.

## Fixes — and the undo rule

The report separates what the app can fix with one click from what needs guided steps or a screwdriver. For one-click fixes: each one is listed with its own consent tick before anything runs, every applied change records its exact before-value, and the **WHAT CHANGED** screen lists every change with its own UNDO button. Guided and hardware items (BIOS settings, cables, dust) are explained step by step — the app never touches those itself.

**Removing unwanted programs is different, and it is walled off from the rest.** It lives in its own room, behind its own separate consent tick, and it says so plainly: **this one cannot be undone.** When you approve a removal, the app runs that program's *own* uninstaller — the vendor's window and any prompts it raises are theirs, stay visible, and are yours to answer. Say no in that window and nothing is removed. Afterwards the app re-checks whether the program's entry is actually gone and tells you either way, including when it can't tell the difference between "you declined" and "it wants a reboot."

## Your rulings

Any finding can be marked **"I know about this."** It stops counting against your score, stays listed, and stays watched: it comes back on its own if the evidence gets worse, and once a marked item reads clean the mark retires — so if that thing ever breaks again, you get told fresh instead of silence.

## Privacy

**Your reports stay on your PC. Nothing is uploaded, ever.** No server, no account, no telemetry, no analytics, no crash reporting. Your files, settings, hardware details and scores are not sent anywhere — a report card only ever leaves this machine if you send it yourself.

The app does make a small number of outbound calls, and it is worth naming all of them rather than claiming there are none. The complete list, also shown on the app's About screen:

1. **The update check** — when you press CHECK FOR UPDATES, or once at launch if you tick that box. It asks the channel what the newest version is.
2. **Name-server timing, during every check-up** — the same three names (`example.com`, `microsoft.com`, `wikipedia.org`) are asked of your own name server and of two public ones (Cloudflare and Google), to see which answers fastest. Nothing of yours is in the question.
3. **Name-server timing again, if you press FIX** — only when a faster name server is on the plan, and on a fresh set of everyday names, because re-using the first three would hand your router a race it had just warmed its cache for.
4. **One proof that a new name server answers** — only if you approve that change. If it can't answer, your old setting goes straight back.
5. **The connection load test** — only when you tick its consent before a check-up. It downloads about 50 MB from Cloudflare's public speed test, times it, and throws the data away.

6. **The program-updates listing, during every check-up** — Windows' own package manager (winget) is asked, read-only, which of your installed programs have a newer version. To answer, winget fetches its public catalog from Microsoft. winget is Microsoft's program, not ours, and follows your Windows diagnostic-data setting.
7. **Eight small pings to your own router, during every check-up** — to read how quickly the path to it answers. They stay inside your home network.

That is the complete list, and it is the same list the app shows on its About screen. The shareable report copy masks your router's addresses; crash notes mask your user folder name.

## Updates

**CHECK FOR UPDATES** lives on the About screen. A new build installs only after passing two gates: its SHA-256 checksum matches the published manifest, and its RSA signature verifies against the maker's key — a tampered or rehosted file cannot pass. The old build stays beside the new one as a fallback, and an interrupted update puts the original back exactly as it was.

## Status

Free testing preview, under active development. Every release lists its SHA-256 checksum. If something confused you, that's a finding — say it.

---

© 2026 Luis. All rights reserved. This is a free testing preview; the binaries may not be redistributed, modified, or rehosted without permission.
