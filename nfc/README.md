# DIY NFC Tags for Detach — Block Apps With a Tap for ~$0.30

**Skip the pricey card: use your own cheap NFC tags as a physical trigger to open Detach and block social media — a free, DIY way to reduce screen time on iOS 17+ with NFC.**

This guide shows you how to buy generic NFC stickers for pennies and set them up so a single tap on your iPhone launches Detach. It is 100% optional. The Detach app is free, and if you'd rather not tinker, the official [$9.99 NFC card](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo) does the same thing out of the box with zero setup.

> **Honesty first:** An NFC tag by itself cannot silently block apps. iOS does not allow a bare tag to lock your phone. The tag is only a *trigger* — the actual app blocking is done by the Detach app. This guide explains exactly how that works and never asks you to trust anything magic.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

---

## How this actually works (the honest version)

Here is the real mechanism, with no hand-waving:

1. **iOS 17+ has a feature called Shortcuts "Personal Automations."** One of the available triggers is **"NFC" → scan a specific tag.** When you tap that tag, iOS runs whatever actions you told it to.
2. **A blank NFC tag holds a tiny bit of data** — most commonly a URL (an "NDEF URI record"). On its own, that URL just opens a link. It has **no power to block apps.**
3. **The blocking is done entirely by the Detach app.** Detach uses Apple's Family Controls / Screen Time layer (the same system layer parental controls use) to block your selected apps. There is no bypass button — blocked means blocked. The tag's only job is to *launch or signal Detach*.

So the flow is: **tap tag → iOS Shortcuts automation fires → Detach opens / a Focus toggles → your chosen apps get blocked.**

That's it. No private "magic" URL scheme, no silent background lock. Any product — including the official card — relies on this same Apple plumbing. The difference is just convenience and polish.

---

## What you'll need

| Item | Cost | Notes |
|---|---|---|
| **NTAG213 or NTAG215 NFC stickers** | ~$0.20–$0.40 each | Sold in packs of 10–50 on Amazon/AliExpress. NTAG213 is plenty; NTAG215 has more memory (only matters for big payloads). Battery-free, last for years. |
| **iPhone with iOS 17+** | You have it | Needs NFC (iPhone 7 and newer all have it). |
| **NFC Tools app** (free) | Free | The standard free app for writing tags. App Store search: *"NFC Tools" by wakdev*. |
| **Detach app** (free) | Free | [Download here](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo). Set up which apps you want blocked first. |

**Buying tip:** search for `NTAG213 stickers` or `NTAG215 NFC tags`. Look for "waterproof" or "on-metal" variants if you plan to stick one on a laptop, fridge, or nightstand. Round 25mm stickers are the most convenient size.

---

## Step 1 — Set up Detach first

Before you touch a tag, open Detach and configure the apps you want to block (social media, games, whatever your distractions are). Confirm blocking works by toggling it in the app. The tag is just a faster way to fire something you've already set up.

---

## Step 2 — Choose what the tag should do

You have two honest, working options:

### Option A (simplest & recommended): Tag opens Detach
The tag stores a **universal link** to Detach. Tapping it opens the app, where a single control locks your apps. This is the most reliable approach because universal links are safe and well-supported.

- **NDEF record type:** URI
- **Value to write:**
  ```
  https://getdetach.app
  ```
  This is a universal link. On a phone with Detach installed, iOS opens the app; on any other phone it opens the website. No custom URL scheme, nothing to break.

### Option B (fewer taps): Tag runs a Shortcuts automation
Instead of storing a link, you store nothing meaningful on the tag and let **iOS Shortcuts** recognize the tag itself, then run actions like "Open Detach" and/or "Turn on a Focus" (e.g. a Do Not Disturb / custom Focus that hides distracting apps as a belt-and-suspenders layer). See Step 4 for this.

> **About Detach-specific deep links:** If Detach publishes a dedicated deep link that jumps straight to "lock now" (something like `https://getdetach.app/lock` **— placeholder, confirm with Detach before relying on it**), you can write that instead of the plain link for a one-tap lock. Until you've verified it in the app, use the plain `https://getdetach.app` universal link above. **Do not** invent an `detach://` scheme — this guide will not give you one because we can't verify it exists.

---

## Step 3 — Write the tag with NFC Tools (Option A)

1. Open **NFC Tools** → **Write** tab.
2. Tap **Add a record** → **URL / URI**.
3. Paste:
   ```
   https://getdetach.app
   ```
4. Tap **OK**, then **Write / Write (X Bytes)**.
5. Hold the top of your iPhone against the sticker until you see **"Write complete!"**
6. **Test it:** lock your phone, wake it, and tap the tag near the top edge. iOS should offer to open Detach (or open it directly).

That's a fully working tap-to-open tag for well under a dollar.

---

## Step 4 — (Optional) One-tap lock with a Personal Automation

This is the closest DIY experience to the paid card: tap → apps blocked, no extra confirmation. It uses Apple's own Shortcuts app.

1. Open the **Shortcuts** app → **Automation** tab → **+** → **Create Personal Automation**.
2. Scroll to and choose **NFC**.
3. Tap **Scan**, then hold your iPhone to the sticker to register it. Give it a name like "Detach Tag."
4. Tap **Next**, then **Add Action**. Add:
   - **Open App → Detach** (so the app comes forward), and/or
   - **Set Focus → On** (turn on a custom Focus that hides your distracting apps — a nice extra layer, though Detach's system-level block is the real enforcement).
5. Tap **Next**. **Turn OFF "Ask Before Running"** so the tap is instant (iOS may still show a small banner).
6. **Done.** Now tapping the tag runs the automation with a single tap.

> **What iOS will and won't do here:** iOS *will* let the automation open apps and toggle Focus with no per-tap confirmation. iOS *will not* let a Shortcut reach into another app and force it to block on its behalf — the blocking still happens inside Detach using Family Controls. That's a platform rule, not a limitation of this guide.

---

## Where to stick your tags

- **Nightstand** — tap before bed to lock social media for the night.
- **Desk / laptop lid** — "work mode" on arrival.
- **Fridge or front door** — tap on your way out.
- **Car dashboard / phone mount** — block distractions while driving.
- **Wallet card slot** — a cheap paper/PVC card tag mimics carrying the official card.

Buy a 10-pack and put one everywhere you want a friction point. That's the whole point of physical triggers: making the *un*blocking take deliberate effort.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Nothing happens on tap | Tap the **top edge** of the phone to the tag; that's where the NFC antenna is. Make sure the screen is on. |
| "Tag not writable" | Some tags ship read-only or were locked by another app. Use a fresh NTAG213/215 sticker. |
| Automation asks for confirmation every time | In Shortcuts, open the automation and turn **off "Ask Before Running."** |
| Tag opens the website, not the app | Detach isn't installed, or the universal link isn't associated yet — install Detach and re-tap. |
| Want to reuse a tag | NFC Tools → **Other** → **Erase tag**, then rewrite. |

---

## Honest comparison: DIY tag vs. the official $9.99 card

| | DIY NFC sticker | Official Detach NFC card |
|---|---|---|
| **Cost** | ~$0.30 + your time | $9.99, ready to go |
| **Setup** | Buy tags, write them, maybe build an automation | None — tap and go |
| **Reliability** | Depends on your setup | Tuned by the Detach team |
| **Form factor** | Whatever sticker you buy | Durable wallet-sized card |
| **Blocking power** | **Identical** — both just trigger Detach | **Identical** |

Neither is "better" at blocking; the block always comes from the Detach app. Pick DIY if you like tinkering and saving a few dollars; pick the card if you want zero fuss and to support the app.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

---

## About this repo

This is the **open companion / resources repo** for Detach. It contains MIT-licensed NFC configs, Apple Shortcuts notes, and setup guides like this one. **The Detach app itself is a free, closed-source download** — it is not in this repo. Get it at **[getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**.

Contributions welcome: better tag recipes, tested deep links (once confirmed with Detach), and Shortcuts templates.
