# Wind-Down Routine — Block Social Media Every Night

**A free Apple Shortcuts automation that blocks distracting apps and calms your
phone every evening, so you actually put it down before bed.** For iOS 17+ with
the free [Detach](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)
app.

> **Honest note:** the Shortcut triggers the ritual — turns on a Focus, opens
> Detach, dims things down. Detach does the real app blocking via Apple's Family
> Controls layer. Set your blocked apps in Detach first.

## Build it

### 1. New Time-of-Day automation
**Shortcuts → Automation → + → Create Personal Automation → Time of Day** →
choose your bedtime hour (e.g. **10:30 PM**), **Daily**. Tap **Next**.

### 2. Add actions (a calm-down stack)
1. **Set Focus → Sleep (or Do Not Disturb) → On**
2. **Open App → Detach** (fallback: **Open URLs** → `https://getdetach.app`)
3. **Set Appearance → Dark** *(optional)*
4. **Set Brightness → 20%** *(optional)*
5. **Set Playback Destination / Play "wind-down" playlist** *(optional)*
6. **Show Notification → "Phone's done for the day. Night. 🌙"**

Turn **off** "Ask Before Running", then **Done**.

### 3. Morning release (optional)
Add a second automation in the morning that turns the Focus **Off**, restores
brightness, and opens Detach so you can unblock intentionally.

## Why this works
Nighttime is when doomscrolling does the most damage to sleep. Automating the
block removes the nightly decision — the phone quiets itself, and unblocking
takes a deliberate step.

Pair with the [scheduled auto-block](./scheduled-auto-block.md) for daytime and
the [NFC tap recipe](./README.md) for on-demand blocking.

---

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**
