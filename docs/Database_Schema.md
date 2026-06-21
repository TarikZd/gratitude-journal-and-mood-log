# 🗄️ Database Schema: Gratitude Journal & Mood Log

---

## Primary Database: Journal Entries

| Property Name | Type | Purpose |
| --- | --- | --- |
| **Entry Title** | `Title` | Auto-filled with today's date (e.g., "June 19, 2026"). |
| **Date** | `Date` | Date of the journal entry. |
| **Mood Score** | `Number` | Rate your mood from 1 (very low) to 10 (excellent). |
| **Mood Badge** | `Formula` | Converts Mood Score to an emoji badge. |
| **Energy Level** | `Select` | `⚡ High`, `😐 Medium`, `😴 Low`. |
| **3 Things Grateful For** | `Text` | Bullet list of three gratitudes. |
| **Daily Win** | `Text` | One thing you accomplished today. |
| **Intention for Tomorrow** | `Text` | One focus or goal for the next day. |
| **Affirmation** | `Text` | Today's positive affirmation. |
| **Stress Level** | `Number` | Rate stress from 1 (none) to 10 (extreme). |
| **Sleep (hrs)** | `Number` | Hours of sleep last night. |
| **Exercise** | `Checkbox` | Did you move your body today? |
| **Tags** | `Multi-select` | `Productivity`, `Relationships`, `Health`, `Creativity`, `Career`. |

## Formula 2.0 Logic — Mood Badge
```javascript
ifs(
  prop("Mood Score") >= 9, "🌟 Excellent",
  prop("Mood Score") >= 7, "😊 Good",
  prop("Mood Score") >= 5, "😐 Okay",
  prop("Mood Score") >= 3, "😔 Low",
  "💙 Tough Day"
)
```

## Formula 2.0 Logic — Mood Progress Bar
```javascript
slice("▓▓▓▓▓▓▓▓▓▓", 0, prop("Mood Score")) + slice("░░░░░░░░░░", 0, 10 - prop("Mood Score"))
```

## Architectural Notes
- **Vault Method:** Journal Entries database resides in `[DB] Backend`. Dashboard uses a Calendar Linked View for mood trend visualization.
- **Privacy:** This template is private by default. Never share the page URL publicly.
- **Recommended Views:** Calendar (by Date) for visual mood trends, Table for detailed log, Gallery for mood badges overview.
