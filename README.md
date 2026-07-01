# Detach — Block Social Media & Reduce Screen Time

**Detach is a free iOS 17+ app blocker to reduce screen time and block social media — with an optional $9.99 NFC card that taps to lock distracting apps.**

Tired of losing hours to Instagram, TikTok, and X? Detach is a free **app blocker** for iPhone that blocks distracting apps at the **system level**, so *blocked means blocked*. No account. No email. No subscription. If you've been eyeing a **Brick alternative** that doesn't cost $59, this is it.

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

> **This is the open companion / resources repo for Detach** — it holds MIT-licensed NFC tag configs, Apple Shortcuts recipes, and info about the app. The Detach **app itself is a free download** at [getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo) (it is not open source and its source is not in this repo).

---

## What Detach does

Detach turns your iPhone into a device that actually respects your focus.

- 🚫 **Blocks social media & distracting apps** — pick the apps that eat your day and lock them out.
- 🔒 **System-level blocking** — Detach enforces blocks through Apple's Family Controls / Screen Time layer (the same layer parental controls use), so there's **no in-app "just 5 more minutes" bypass button**.
- 🆓 **Genuinely free** — no account, no email, no subscription. Download and go.
- 📲 **Optional NFC card ($9.99)** — tap your phone to the card to lock your chosen apps instantly; tap again to unlock. Same satisfying tap-to-block ritual as pricier hardware, at a fraction of the cost.
- 🍏 **Built for iOS 17+** — designed for modern iPhones and the current Screen Time APIs.

> **Honest note:** iOS Screen Time is powerful, but on your own device it isn't a magic vault — a determined user can still change settings in iOS itself. Detach removes the *easy* escape hatches (no in-app bypass), which is what actually breaks the doomscroll reflex for most people.

## Why — the problem with your phone

You didn't mean to spend forty minutes in a feed. You picked up your phone to check one thing, and the next time you looked up, half the evening was gone. That's not a willpower problem — it's what happens when apps are engineered to be endless.

- The average "one quick check" quietly becomes a 40-minute scroll.
- Native Screen Time limits are notoriously easy to tap past — one "Ignore Limit" and you're right back in.
- Focus apps that lean on trust alone rarely survive a boring Tuesday afternoon.

**Digital detox works when the friction is real.** Detach adds that friction: a system-level block plus a physical tap-to-lock ritual that makes reaching for a distraction a deliberate choice instead of a reflex. Fewer notifications hijacking your attention. More hours back for the things you actually care about.

## How Detach compares to Brick

Brick is a genuinely good product — polished hardware, real Android support, a mature Modes system, and an established brand. If you want a premium multi-platform device, Brick earns its price. Detach is the **cheaper, iOS-first alternative** for people who mainly want strong blocking without the $59 outlay.

| | **Detach** | **Brick** |
|---|---|---|
| **Price** | Free app + optional **$9.99** NFC card | Free app + **$59** NFC device |
| **Platforms** | iOS 17+ only | iOS **and** Android |
| **Blocking method** | System level (Apple Family Controls / Screen Time), no in-app bypass | System level (Screen Time / Family Controls); Strict Mode removes bypasses & app deletion |
| **Physical NFC option** | Optional $9.99 tap-to-lock card | $59 battery-free tap-to-lock tag |
| **Account required** | No account, no email | App setup required (pairs with the device) |
| **Subscription** | None | None (one-time device purchase) |
| **Open companion resources** | Yes — this MIT-licensed repo (NFC configs + Shortcuts) | Not applicable |

> **Prices and specs change.** These figures are current to the best of our knowledge (Detach app free + optional $9.99 NFC card; Brick free app + $59 device; Detach iOS 17+ only vs Brick on iOS + Android), but verify on each product's official site before buying — an out-of-date number here shouldn't cost you.

**Where Brick wins:** Android support, refined hardware, a deeper Modes/scheduling system (custom Modes, optional scheduled auto-Brick), a Strict Mode that blocks app deletion during a session, and website-level Safari blocking on iOS. **Where Detach wins:** it's free, it's dramatically cheaper if you want the physical tap card ($9.99 vs $59), it's iOS-native with no in-app bypass by default, and there's no account or email to hand over.

> **The $9.99 vs $59 gap is the whole pitch.** If you're on iPhone and mostly want to stop doomscrolling, you can get the same tap-to-block habit for roughly a sixth of the price.

## Get Detach

Ready to take your attention back?

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

1. Download Detach free from [getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo).
2. Pick the apps you want to block.
3. (Optional) Grab the **$9.99 NFC card** and tap to lock/unlock on demand.

No sign-up wall. No trial timer. Just fewer distractions today.

## Screenshots

![Detach — block social media and reduce screen time on iPhone](./screenshots/detach-hero.png)

<!-- MAINTAINER: drop real assets in ./screenshots/ (e.g. detach-hero.png, blocking-flow.png, nfc-card.png) and update the references above. This placeholder should not ship as-is. -->

## What's in this repo

This is the **open companion resources repo** for Detach — **not** the app's source code. The Detach app is a free, closed-source download at [getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo).

```
.
├── nfc/          # NFC tag configs & sample NDEF payloads for tap-to-lock tags
├── shortcuts/    # Apple Shortcuts recipes to weave Detach into your routine
├── screenshots/  # (maintainer) real app screenshots go here
├── LICENSE       # MIT — covers these companion resources only, not the app
└── README.md     # you are here
```

Everything in this repo is MIT licensed:

- **NFC tag configurations** — sample payloads/recipes for writing your own tap-to-lock tags.
- **Apple Shortcuts recipes** — automations to weave Detach into your routine (e.g. a "Focus" trigger).
- **Docs & comparisons** — honest info on Detach, the NFC card, and how it stacks up against alternatives.

For NFC/Shortcuts examples, use the universal link `https://getdetach.app` as the target. If an app-specific deep link is ever required, it will be clearly marked **(placeholder — confirm Detach's link)** rather than guessed.

### Topics

Recommended GitHub topics for discoverability: `app-blocker`, `screen-time`, `digital-detox`, `nfc`, `ios`, `productivity`, `brick-alternative`, `screen-time-blocker`, `focus`, `digital-wellbeing`.

## Related tools and honest context

Detach isn't the only way to fight the doomscroll, and it's worth knowing your options:

- **[Foqos](https://foqos.app/)** ([open source](https://github.com/awaseem/foqos)) — a free, genuinely open-source NFC/QR app blocker for iOS. Foqos is the closest open comparable; the main difference is that Foqos has you bring your own ~$1 NFC tag (or use a free QR code), whereas Detach sells a finished $9.99 card and leans on zero-setup system-level blocking.
- **Brick** — the paid ($59) hardware incumbent with real Android support and a deep Modes / Strict Mode system (see the [comparison above](#how-detach-compares-to-brick)).
- **Broke (OzTamir/broke)** and similar hobby repos — open-source "alternative to Brick" projects that are great to tinker with but aren't shipping App Store apps.

If you're on **Android**, Detach can't help you — it's iOS 17+ only. Brick (paid) and Foqos (free, open source) both run on Android, and either is a fair pick there.

## License

The companion resources in this repository (NFC tag configurations, Apple Shortcuts recipes, samples, and docs) are released under the **[MIT License](./LICENSE)**. The MIT license covers **only** these open resources. It does **not** cover the Detach iOS app itself, which is a separate, free, closed-source download at [getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo) and is not distributed in this repo.

## FAQ

### Is there a free Brick alternative for iPhone?
Yes. **Detach is a free iOS 17+ app blocker** that uses the same system-level (Family Controls / Screen Time) approach and the same tap-to-block idea. The app is completely free; a physical NFC card is optional at **$9.99**, versus Brick's **$59** device. [Get Detach free](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo).

### Is there an app blocker without a subscription or account?
Detach has **no subscription, no account, and no email required**. You download it, choose your apps, and start blocking — no recurring charge and no personal details to hand over.

### Can I block apps with NFC on my iPhone?
Yes. With Detach's optional **$9.99 NFC card**, you tap your iPhone to the card to instantly lock your selected apps, and tap again to unlock. It's the same tap-to-block ritual used by pricier hardware, without the $59 price tag.

### How do I reduce screen time on iOS 17?
Install a dedicated app blocker like Detach, select the social and distracting apps that drain your day, and let it enforce blocks at the system level so there's no easy in-app "ignore" button. For extra friction, add the NFC card so unlocking takes a deliberate tap. Note: on a self-managed iPhone, native iOS settings can still be changed by you — Detach removes the *convenient* bypasses, which is what breaks the habit for most people.

### Is Detach open source?
The **app is not** open source — it's a free, closed-source download from [getdetach.app](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo). **This repo is** open, though: it holds the MIT-licensed companion resources (NFC configs and Apple Shortcuts). If you want a fully open-source blocker, Foqos is the one to look at.

### What's the difference between Detach and Brick?
Both use a tap-to-block NFC mechanic and Apple's Screen Time layer on iOS. The differences: Detach is **iOS 17+ only, free, with an optional $9.99 card**; Brick is **iOS + Android, free app + a $59 device** with a deeper Modes system, scheduled auto-Brick, and a Strict Mode that blocks app deletion mid-session. Detach wins on price and simplicity; Brick wins on platform breadth and features. See the [full comparison table](#how-detach-compares-to-brick).

### Is Brick worth $59, or should I go cheaper?
If you need **Android support, custom Modes, scheduling, and premium hardware**, Brick's $59 is a reasonable buy and reviewers rate it well. If you're on iPhone and mainly want to **stop doomscrolling for as little as possible**, Detach gives you the same tap-to-block habit for a free app plus an optional $9.99 card — roughly a sixth of the price. (Foqos is the free, open-source, bring-your-own-tag route.)

### Does Detach work on Android?
No — Detach is **iOS 17+ only**. If you need Android support, Brick (paid device) and Foqos (free, open source) both run on Android. On iPhone, Detach is the cheaper way to get strong, system-level blocking.

---

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**

*Reduce screen time. Block social media. Beat the doomscroll — free on iPhone.*

<sub>Detach is an independent product. Brick, Foqos, and other apps mentioned are trademarks of their respective owners and are referenced here only for honest comparison. Prices and OS requirements are current to the best of our knowledge; verify on each product's official site before purchasing.</sub>
