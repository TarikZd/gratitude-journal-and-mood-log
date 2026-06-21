# 📖 Start Here: Gratitude Journal & Mood Log

Welcome to the **Gratitude Journal & Mood Log** by **Moorish Dev**. Write your first entry in under 60 seconds.

> ⚠️ **Privacy Notice:** This journal is private by default. Keep your personal Notion page URL private — do NOT share it publicly.

---

## ⚡ Quick Start (60 Seconds)

1. **Duplicate this template** → Click `Duplicate` in the top-right corner.
2. **Write today's entry** → Click "✍️ New Daily Entry". The date auto-fills.
3. **Rate your mood** → Enter a number from 1 (very low) to 10 (excellent) in `Mood Score`. The badge auto-updates.
4. **Fill in your gratitudes** → Write 3 things you're grateful for today.
5. **Set your intention** → Write one focus for tomorrow.

---

## 🏗️ Architecture Overview

| Location | What's Here |
| --- | --- |
| **Main Dashboard** | Mood Calendar + Linked Views + Daily Entry Button |
| **`[DB] Backend`** | Raw `Journal Entries` database |

---

## ✍️ Manual Setup Steps (Required)

### Step 1: Verify the Mood Badge Formula
1. Open `[DB] Backend` → `Journal Entries`.
2. Click `Mood Badge` → **Edit Property** → Verify type is `Formula`. Paste if needed:
```javascript
ifs(
  prop("Mood Score") >= 9, "🌟 Excellent",
  prop("Mood Score") >= 7, "😊 Good",
  prop("Mood Score") >= 5, "😐 Okay",
  prop("Mood Score") >= 3, "😔 Low",
  "💙 Tough Day"
)
```

### Step 2: Set Up the Mood Calendar View
1. On the dashboard's Linked View → `+ Add a view` → `Calendar`.
2. Set date to `Date`. Name it `📅 Mood Calendar`.

### Step 3: Create the Daily Entry Button
1. Type `/button` → Label: `✍️ New Daily Entry`.
2. Configure: Add page in Journal Entries database with today's date auto-filled.

---

## 🎨 Customization Tips
- **Morning or Evening?** Use the Entry Title (date) to establish a consistent journaling habit — morning pages are great for intention-setting, evening pages for reflection.
- **Weekly Review**: Filter entries by `Last 7 days` and review your mood trends every Sunday.
- **Affirmation Rotation**: Keep a separate Notion page of favorite affirmations to pull from daily.

---

*Built by Moorish Dev | Last Updated: June 2026*
