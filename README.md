# 💪 PUSHUP Tracker

A fully self-contained, offline-capable pushup tracking web application built as a single HTML file. No installation, no accounts, no internet required — just open the file in any modern browser and start tracking.

---

## Getting Started

1. Download `pushup-tracker.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. That's it — your data is saved automatically to your browser's local storage

---

## Features Overview

### 💪 Workout Tab

The primary screen for logging your daily pushup activity.

#### Daily Stats Bar
Three at-a-glance metrics at the top of the screen:
- **Today** — total reps logged so far today
- **Sets** — number of sets completed today
- **This Week** — cumulative reps for the current Sun–Sat week

#### Set Timer
A stopwatch you can run during your set to track duration.
- **Start / Pause / Resume** — tap to toggle mid-set
- **Reset** — clears the timer back to zero
- The elapsed time automatically populates the **Duration** field in Log a Set when paused or stopped

#### Log a Set
The form for recording each completed set.

| Field | Description |
|---|---|
| **Reps** | Number of pushups completed in this set |
| **Set #** | Auto-filled with the next set number based on today's history; editable if needed |
| **Duration (s)** | Auto-filled from the timer above; can also be edited manually |
| **Time of Set** | Leave blank to stamp the current time, or enter a past time (e.g. `09:30`) to backfill a set you forgot to log |

Tap **✓ Log This Set** to save. The timer resets and the Set # advances automatically.

#### Daily Goal
Set a rep target for the day. The completion percentage updates live as you log sets and exceeds 100% if you surpass your goal. When you hit your goal for the first time each day, a **confetti celebration** and **fanfare sound** play automatically.

---

### 📊 History Tab

Review your pushup history across different time ranges.

#### Chart View
An interactive chart with toggleable type and time range.

**Chart Type**
- **▬ Bar** — vertical bar chart
- **╱ Line** — SVG line chart with area fill, gridlines, and data point markers (default)

**Time Range**
- **Week** — current Sun–Sat week, one bar/point per day
- **MTD** — month to date, one bar/point per day
- **YTD** — year to date, grouped by month
- **Custom** — pick any From/To date range; auto-groups into days (≤31), weeks (32–90 days), or months (90+ days)

Today's data point is always highlighted in green.

#### Summary Stats
- **Daily Avg** — average reps across all days with recorded activity
- **Best Day** — highest single-day rep count on record
- **All Time** — total reps ever logged

#### Export & Import

**⬇ Export CSV** — downloads all logged data as a `.csv` file named `pushups_YYYY-MM-DD.csv`.

**⬆ Import CSV** — merge data from a CSV file into your existing records. Duplicate entries (matched by `id`) are automatically skipped.

**📄 Template** — downloads a pre-formatted starter CSV with the correct headers and example rows, ready to edit.

---

### ⏰ Reminders Tab

Configure recurring reminders to prompt you to do pushups throughout the day.

#### Reminder Toggle
Enable or disable reminders with the on/off switch. When active, the app will alert you at your configured interval.

#### Configuration Options
- **Interval** — choose from preset intervals (15 min, 30 min, 1 hr, 1.5 hrs, 2 hrs, 3 hrs) or set a custom number of minutes
- **Start Time** — reminders won't fire before this time (default: 7:00 AM)
- **End Time** — reminders won't fire after this time (default: 9:00 PM)
- **Next Reminder** — live countdown showing exactly when the next reminder will fire

#### Reminder Alerts
When a reminder fires:
- An **audible chime** plays
- A **sticky notification banner** appears on screen — it stays visible until you tap it to dismiss
- A **browser notification** appears if you've granted notification permission

---

## Data & Privacy

All data is stored exclusively in your browser's **localStorage** — nothing is sent to any server. Data persists across page refreshes and browser restarts on the same device and browser.

> **Note:** Clearing your browser's site data or localStorage will erase your history. Use the **Export CSV** feature regularly to back up your data.

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome / Edge | ✅ Full support |
| Firefox | ✅ Full support |
| Safari | ✅ Full support |
| Mobile browsers | ✅ Responsive layout |
