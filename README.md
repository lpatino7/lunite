# LUNITE

Questions, a confusing screen, a report that looks wrong: luniteapp@gmail.com. Or open SETTINGS > SEND A REPORT inside the app.

**An honest PC check-up for Windows.** Lunite reads your machine's real settings and hardware, scores only what it actually verified, and says plainly what it could not read. It changes nothing without a yes, and every setting the app itself changes is reversible with one button. The one thing that is not, removing a program, is walled off and marked permanent.

> **Certus is now Lunite.** Same app, same records, same checks — the old name was shared with several other software companies, so people searching for us found them instead. Copies already installed keep updating through the same signed channel; the old address still reaches us. Older releases below still carry the Certus name, because that is who published them.

Free to use. A paid license for the one-click fixes is planned and not on sale yet — see [Free, paid, and refunds](#free-paid-and-refunds).

## Download and run

1. Download **`Lunite.exe`** from **[Releases](https://github.com/lpatino7/lunite/releases/latest)** (under *Assets*). There is no zip and no installer — the app is one portable exe.
2. **Windows 10/11 PCs only** — open the link on your PC, not your phone. Save it anywhere; the Desktop is fine.
3. Run it. Windows will show a blue SmartScreen warning — click **More info → Run anyway**.
4. Click **RUN CHECK-UP**. The check-up itself is read-only: it changes nothing on your PC. Changes happen only later, on the FIX screen, where every fix has its own tick box (the safe, instantly undoable ones start ticked, so untick any you do not want), and every setting change has its own UNDO. Removing a program, in its own room, is the one exception and is marked permanent.

You don't need administrator access. Three measurements — memory speed, drive speed, startup time — come from Windows' built-in benchmark and do need it; the report says when they were skipped and why, and offers a restart-with-access button.

### About that SmartScreen warning

It is Windows being properly cautious, and it will happen. The app is not code-signed yet, so Windows has no publisher name to show you and no download history to judge it by. The rename reset what little reputation the old name had earned, so expect the warning to stick around for a while. A signing certificate is on the roadmap.

That warning means *"I don't know who made this"* — not *"I found something bad."* If that distinction isn't enough for you, don't run it. That's a reasonable call, and the next section is there so you don't have to take anyone's word for it.

### Verify what you downloaded

Every release publishes the SHA-256 of its exe in the release notes. To check yours matches, in PowerShell:

```
Get-FileHash .\Lunite.exe -Algorithm SHA256
```

Compare it to the hash in the [release notes](https://github.com/lpatino7/lunite/releases/latest). If they differ, don't run it — email luniteapp@gmail.com.

## What a check-up covers

Roughly two dozen verified checks, reported in plain words:

- **Settings that cost you performance** — power plan, monitor refresh rate, mouse acceleration, background game recording, startup load (including programs set to start twice), screen sleep, network adapter power saving, graphics driver age.
- **Hardware truths** — RAM running below the speed the sticks themselves report as their rating, single-channel memory, old motherboard firmware, drive health and real free space, fast USB devices linked below their tier, damaged-cable tells on wired links (only after the adapter itself is verified capable of more).
- **Factory-installed extras** — trialware, adware, and fake "speed-up" tools, named exactly. Manufacturer utilities (fan control, RGB) are listed, never accused, and your active antivirus can never be called bloat, whatever the brand.
- **Health first** — antivirus state, drive health warnings, the CPU speed-limit log (the quiet slowdowns firmware applies when a machine runs hot), unexpected power-loss history. Protect-before-optimize items never offer you a one-click fix.
- **Network reality** — double-router paths, who answers your DNS lookups, measured round-trip time to your router.
- **Sound** — the default microphone pick (Windows loves to quietly switch you back to a webcam mic).

Every check ends one of three ways: verified on this machine, flagged with the evidence, or honestly marked *could not read*. Unreadable checks are excluded from the scoring math and listed — never guessed.

## Scores

Three scores — Gaming, Media, Work — plus an overall, computed only from checks that were actually read on your machine. The report states what the number was computed from, including what it failed to read. Measured numbers come with verdicts judged against your actual hardware's class, not a generic ideal.

## Fixes — and the undo rule

The report separates what the app can fix with one click from what needs guided steps or a screwdriver. For one-click fixes: each one is listed with its own consent tick before anything runs, every applied change records its exact before-value, and the **WHAT CHANGED** screen lists every change with its own UNDO button. Guided and hardware items (BIOS settings, cables, dust) are explained step by step — the app never touches those itself.

**Removing unwanted programs is different, and it is walled off from the rest.** It lives in its own room, behind its own separate consent tick, and it says so plainly: **this one cannot be undone.** When you approve a removal, the app runs that program's *own* uninstaller — the vendor's window and any prompts it raises are theirs, stay visible, and are yours to answer. Say no in that window and nothing is removed. Afterwards the app re-checks whether the program's entry is actually gone and tells you either way, including when it can't tell the difference between "you declined" and "it wants a reboot."

## Free, paid, and refunds

**Lunite is free to download and use.** The check-up, every score, every explanation, the full report and its written how-to steps cost nothing, and that stays true. Today the one-click fixes are free too, only because the license is not on sale yet: the app has no paywall, no license screen and no buy button. The plan below is the one thing that will change, and only for the one-click fixes.

**What is planned.** A paid license, **$19.99 in US dollars, paid once**, not a subscription, that lets the app *apply* the one-click fixes for you instead of you making the changes by hand. Once it is on sale, the app will apply one-click fixes only with a license. There is no free trial fix, and the written how-to steps stay free. They would work the way they work now: a tick box for each one, and an UNDO for each one. UNDO and the WHAT CHANGED screen will keep working with or without a license, including after a refund, so none of the one-click fixes is ever locked in. Removing programs is separate. It is the one thing that cannot be undone (see above), and it stays free. Depending on where you live, the checkout may add sales tax or VAT, and it may show the price in your local currency. Checkout is not offered in every country.

**What a license covers.** One license covers one person, on the PCs they own or use themselves. The app does not count machines and has no activation limit: on each PC, you paste the same key. It stays valid for every future version of Lunite, so you never pay again when the app updates. The key works offline, so the app never contacts anyone to accept it. It does not cover other people's PCs, such as friends' or clients', and it does not give anyone the right to redistribute the app. A license lets the app apply fixes for you. Lunite is provided as is: every setting it changes has an UNDO, but it does not promise any particular speed-up, because results depend on your PC.

**It is not on sale yet.** There is nothing to buy today. When it goes on sale, this section will say so and link to the checkout. The version of the app that adds the license will say so in its release notes, and updates only install after you say yes.

**How the key will reach you.** The plan is that your license key is emailed to you automatically from luniteapp@gmail.com, with the subject “Your Lunite license key”, usually within minutes of your payment going through. It is made for the email address you bought with, and the app checks it on your PC without contacting anyone. You will need the version of Lunite that adds the license: CHECK FOR UPDATES on SETTINGS gets it. If your payment method takes days to clear, the key is sent as soon as it does. Not there after 10 minutes? Check your spam folder. Still nothing after an hour? Email me and I will send it again or refund you in full, even if that is after the 30 days.

**Refunds: 30 days.** The one-click fixes all have an UNDO, and so does the purchase. Ask within 30 days of buying and I will refund you in full. You do not need a reason. Email **luniteapp@gmail.com**, say you want a refund, and tell me the email address you bought with. I aim to answer within a few days. The money goes back the way you paid, including any tax, and can take 5 to 10 business days to show on your statement. You can also ask Link, the name Stripe sells under at checkout (more below), for a refund from your receipt. Link's terms and your local consumer rights apply as well.

**What a refund does to your key.** A refund ends your license. Because the app checks keys on your PC without contacting anyone, it cannot switch a refunded key off, so I am trusting you to stop using it. I would rather trust you than build a check that phones home. The same goes for sharing it with other people: I cannot stop a shared key from working, so I am asking you not to. After a refund, remove the license in the app (the license screen will have a button for it). Fixes you already applied stay applied, and UNDO keeps working.

**Who you are buying from.** Lunite is made by one person, Luis, a sole proprietor in the United States, not a company. The sale itself will be made by Stripe, shown to you as Link: you will see “Sold through Link”, your receipt comes from Link, and your card statement shows a line starting with LINK.COM*. The key and support come from me. I use your email address to send your key and to answer you. I do not sell it, and the only others who handle it are Stripe (as Link, at checkout) and Google, which runs my email and keeps my sales log: your email address, the date and the purchase reference, so a key is not sent twice and a send that fails is retried while I am alerted. Once the 30 days are over, you can ask me to remove your email address from that log; Stripe and Link keep their own records, and so does the email I sent you. Your key contains your email address, so do not post it publicly. Your payment details go to Stripe's checkout, never to me or to the app.

## Your rulings

Any finding can be marked **"I know about this."** It stops counting against your score, stays listed, and stays watched: it comes back on its own if the evidence gets worse, and once a marked item reads clean the mark retires — so if that thing ever breaks again, you get told fresh instead of silence.

## Privacy

**Your reports stay on your PC. Nothing is uploaded unless you press SEND on the SEND A REPORT screen in SETTINGS.** No account, no telemetry, no analytics, no automatic crash reporting. Your files, settings, hardware details and scores are not sent anywhere on their own — a report card only ever leaves this machine if you send it yourself.

The app does make a small number of outbound calls, and it is worth naming all of them rather than claiming there are none. The complete list, also shown on the app's About screen:

1. **The update check** — when you press CHECK FOR UPDATES on SETTINGS, or once at launch if you tick the box there. It asks the channel what the newest version is. If there is a newer one, it downloads it and checks it, then asks you before installing anything.
2. **Name-server timing, during every check-up** — the same three names (`example.com`, `microsoft.com`, `wikipedia.org`) are asked of your own name server and of two public ones (Cloudflare and Google), to see which answers fastest. Nothing of yours is in the question.
3. **Name-server timing again, if you press FIX** — only when a faster name server is on the plan, and on a fresh set of everyday names, because re-using the first three would hand your router a race it had just warmed its cache for.
4. **One proof that a new name server answers** — only if you approve that change. If it can't answer, your old setting goes straight back.
5. **The connection load test** — only when you tick its consent before a check-up. It downloads from Cloudflare's public speed test at full speed for about six to eight seconds, pings Cloudflare (1.1.1.1) about twenty times to measure how much your lag rises, and throws the data away. How much data that pulls depends on how fast your line is — roughly 1 MB for every 1 Mbps, so about 100 MB on a 100 Mbps line and close to 1 GB on gigabit.

6. **The program-updates listing, during every check-up** — Windows' own package manager (winget) is asked, read-only, which of your installed programs have a newer version. To answer, winget fetches its public catalog from Microsoft. winget is Microsoft's program, not ours — depending on your Windows diagnostic-data setting, it may send Microsoft its own usage data.
7. **About a dozen small pings to your own router, during every check-up** — to read how quickly the path to it answers. They go to your router (your PC's gateway) and no further.
8. **Send a report** — only when you press SEND on the SEND A REPORT screen in SETTINGS. It sends your report card with this PC's name replaced by a short code (the same code each time you send from this PC), the app and Windows versions, the newest crash note if there is one, the time you sent it, and whatever you typed, to luniteapp@gmail.com. The screen lists all of it and can open the exact card for you to read before you press SEND, and nothing goes on its own.

That is the complete list, and it is the same list the app shows on its About screen. The shareable report copy masks your router's addresses; crash notes mask your user folder name.

## Updates

**CHECK FOR UPDATES** lives on the SETTINGS screen. A new build installs only after passing two gates: its SHA-256 checksum matches the published manifest, and its RSA signature verifies against the maker's key — a tampered or rehosted file cannot pass. If the swap fails, the app puts your old build back, and the old build is also kept beside the new one as a fallback.

## Status

Under active development. Every release lists its SHA-256 checksum. If something confused you, that's a finding — email luniteapp@gmail.com or use SETTINGS > SEND A REPORT.

---

© 2026 Luis. All rights reserved. The binaries may not be redistributed, modified, or rehosted without permission.
