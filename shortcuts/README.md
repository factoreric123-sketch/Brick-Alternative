# Detach "Detach on Tap" — Block Social Media & Reduce Screen Time With an NFC Shortcut

**A free Apple Shortcuts NFC automation that turns any tag into a tap-to-block ritual for Detach — the free iOS 17+ app blocker that helps you reduce screen time and block social media.**

This is an Apple Shortcuts *recipe*, not a downloadable file. Apple does not let anyone ship a signed binary `.shortcut` that other people can trust blindly, so instead this page walks you through rebuilding a **"Detach on Tap" NFC Personal Automation** by hand in about two minutes. You tap an NFC tag, the automation fires, Detach comes forward, and your chosen apps are blocked.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

> **Honesty first (read this):** This Shortcut does **not** block apps by itself. iOS does not let one app (or a Shortcut) reach into another and force it to lock. The actual blocking is done entirely by the **Detach app** using Apple's Family Controls / Screen Time layer — the same system layer parental controls use, with no bypass button. This automation is a **convenience trigger and a ritual**: tap → Detach opens / a Focus turns on → the block you already configured in Detach takes effect. Set Detach up first; the tag just fires it faster.

---

## What you'll need

- **iPhone with iOS 17+** (NFC is built into iPhone 7 and newer).
- **Detach** installed and configured — pick the apps you want blocked *inside Detach first*. [Download Detach, free](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo).
- **One NFC tag.** Either the official [$9.99 Detach NFC card](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo) or a generic ~$0.30 NTAG213/215 sticker. Any NFC tag works — Personal Automations recognize the tag itself, so it doesn't even need data written to it.
- The **Shortcuts** app (preinstalled on iOS). No third-party app required for this part.

---

## Build it: step by step

### 1. Open Shortcuts → Automation

Open the **Shortcuts** app and tap the **Automation** tab at the bottom.

### 2. New → NFC

Tap **+** (top right) → **Create Personal Automation** → scroll down and choose **NFC**.

### 3. Scan the tag

Tap **Scan**. Hold the **top edge** of your iPhone against the NFC tag until it registers (that's where the NFC antenna is). When prompted, give the tag a name like **`Detach Tag`** so you can tell it apart from other automations. Tap **Next**.

### 4. Add actions

Tap **Add Action** and build the ordered list below. Add each action in order; you can search for each one by name in the action picker.

---

## The action list (honest and ordered)

Add these actions, top to bottom. Every one is real, and none of them pretends to do the blocking itself — that's Detach's job.

1. **Set Focus → Do Not Disturb → On**
   Turns on a Focus so notifications stop pulling you back in. If you've made a custom "Detach" or "Focus" mode that also hides distracting Home Screen pages, choose that instead — it's a nice extra layer, but remember it is *cosmetic* next to Detach's system-level block.

2. **Open App → Detach**
   Brings Detach to the foreground so you (or Detach's own flow) can confirm the lock.
   - If "Open App → Detach" doesn't resolve on your device, use **Open URLs** with the universal link `https://getdetach.app` as a fallback. On a phone with Detach installed, iOS opens the app; on any other phone it opens the website. This is a safe universal link — **not** a made-up scheme.
   - *If* Detach later publishes a dedicated deep link that jumps straight to "lock now" — something like `https://getdetach.app/lock` **(placeholder — confirm Detach's link before relying on it)** — you can swap it in here for a true one-tap lock. Until you've verified it, use the plain `https://getdetach.app` universal link. **Do not** invent a `detach://` scheme; this recipe will never give you one because we can't verify it exists.

3. **Show Notification → "Blocked. Go touch grass."**
   A little confirmation banner so the tap feels finished. Change the text to whatever keeps you honest.

Tap **Next** when your actions are in place.

### 5. Turn off "Ask Before Running"

On the final screen, turn **OFF** "Ask Before Running" (and confirm "Don't Ask") so a tap fires instantly instead of nagging you each time. iOS may still show a brief banner at the top — that's a platform behavior, not something this recipe can remove. Tap **Done**.

### 6. Test it

Lock your phone, wake it, and tap the tag to the top edge. The Focus should switch on, Detach should come forward, and you should see your notification. If your apps are blocked in Detach, you're done.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

---

## Reverse it (unlock)

The same NFC tag can toggle *off* in Detach — tap again to unlock, exactly like the paid cards from Brick or the official Detach card. The unlock still happens inside Detach; the tag just re-triggers it. If you want the friction of a *separate* "unblock" step, make a second automation on a different tag that turns your Focus off and opens Detach — but leaving the real unlock inside Detach is what keeps it honest and hard to cheat.

---

## What iOS will and won't do here (so nobody feels misled)

- iOS **will** let this automation turn on a Focus, open an app, and show a notification from a single tap with no per-tap confirmation (once you've turned off "Ask Before Running").
- iOS **will not** let a Shortcut force another app to block on its behalf. The block is enforced by Detach through Family Controls. That's an Apple platform rule, not a limitation of this recipe — and it's the same rule every NFC blocker (including Brick) lives under.

---

## Screenshots

![Detach on Tap automation — placeholder](./screenshots/detach-on-tap.png)

<!-- MAINTAINER: drop a real screenshot of the finished Shortcuts automation here at ./screenshots/detach-on-tap.png (and a shared hero at ../screenshots/detach-hero.png). Show the NFC trigger + the three actions. -->

---

## Share this shortcut

Once you've built and tested the automation, you can export it as an iCloud link so others can import it and just point it at their own tag:

**Share link: (add your iCloud shortcut link here)**

To generate one: open the shortcut → **Share** → **Copy iCloud Link**, then paste it above. Note that iCloud-shared automations still require the recipient to scan *their own* NFC tag and to have Detach installed and configured — the link shares the actions, not your tag or your blocking setup.

---

## FAQ

**Is this a free Brick alternative?**
Yes. Detach is a free iOS 17+ app blocker, and this NFC Shortcut recipe is free too. Brick is a great, polished product with Android support and its Modes system — this is simply the cheaper, iOS-only, "rebuild it yourself" route. We're not knocking Brick; we're giving you a no-cost way to get the same tap-to-block ritual.

**Can I block apps with NFC on iPhone without paying for a card?**
Yes — any generic NTAG213/215 sticker works with this Personal Automation. The official $9.99 Detach card is just a tuned, wallet-friendly version. The blocking power is identical because both only *trigger* Detach.

**Does the Shortcut actually do the blocking?**
No. The Shortcut turns on a Focus, opens Detach, and shows a banner. Detach does the real blocking via Family Controls. Anyone claiming an NFC tag alone "locks your phone" is skipping this step.

**Do I need a subscription or an account?**
No. Detach is completely free — no account, no email, no subscription. This is an app blocker without a subscription, which is a big part of the point.

**Will this reduce my screen time on iOS 17?**
It helps by adding physical friction: a deliberate tap to block, and a deliberate step to unblock. The friction is the feature. Combined with Detach's no-bypass system block, it's a practical digital-detox ritual.

---

## About this repo

This `shortcuts/` folder is part of the **open companion / resources repo** for Detach. It holds MIT-licensed Apple Shortcuts recipes and NFC configs. **The Detach app itself is a free, closed-source download — it is not in this repo and is not open source.** Get the app at **[getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**.

See also: [`../nfc/README.md`](../nfc/README.md) for writing your own cheap NFC tags.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

---

*Recommended GitHub topics for this repo: `app-blocker`, `screen-time`, `digital-detox`, `nfc`, `ios`, `productivity`, `brick-alternative`, `screen-time-blocker`, `focus`, `digital-wellbeing`.*
