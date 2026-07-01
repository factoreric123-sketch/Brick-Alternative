# Scheduled Auto-Block — Lock Distracting Apps on a Timer

**A free Apple Shortcuts automation that turns Detach on automatically at set
times (e.g. every weekday 9–5) so you don't rely on willpower to start.** Works
on iOS 17+ with the free [Detach](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)
app.

> **Honest note:** Shortcuts can't force another app to block on its own. This
> automation turns on a **Focus** and opens **Detach** at a scheduled time; the
> actual blocking is enforced by Detach through Apple's Family Controls layer.
> Configure your blocked apps in Detach first.

## Build it

### 1. New Time-of-Day automation
Open **Shortcuts → Automation → +  → Create Personal Automation → Time of Day**.

### 2. Set the schedule
Pick a start time (e.g. **9:00 AM**), choose **Weekly** and select **Mon–Fri**.
Tap **Next**.

### 3. Add actions
1. **Set Focus → Do Not Disturb (or a custom "Focus" mode) → On**
2. **Open App → Detach**
   - Fallback if needed: **Open URLs** → `https://getdetach.app` (safe universal
     link — never invent a `detach://` scheme).
3. **Show Notification → "Focus time. Apps locked."**

Turn **off** "Ask Before Running", then **Done**.

### 4. Add the matching unlock (optional)
Make a second Time-of-Day automation at your end time (e.g. **5:00 PM**) that
turns the Focus **Off** and opens Detach so you can unblock. Leaving the actual
unlock inside Detach keeps it honest and harder to cheat.

## Tips
- Stack this with the [wind-down routine](./wind-down-routine.md) for evenings.
- Prefer a physical trigger instead of a timer? Use the
  [NFC "Detach on Tap" recipe](./README.md).

---

👉 **[Get Detach — free on iOS](https://getdetach.app/?utm_source=github&utm_medium=readme&utm_campaign=shell_repo)**
