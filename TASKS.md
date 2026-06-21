# 📋 Free Templates: Active Tasks — Gratitude Journal & Mood Log

This document tracks all development tasks for this template, strictly adhering to the `AGENTS.md` protocol.

- `[ ]` uncompleted | `[/]` in progress | `[x]` completed

---

## 🏃 Current Sprint

### Local Filesystem Initialization
- [x] **T0: [DESIGN] Create Local Directory Structure and Apply Logo** — *(completed 2026-06-18 by Antigravity)*
  - **Changed:** Created subdirectories and copied `moorish_dev_logo.png` into `assets/`.
  - **Gotchas/Next Steps:** Proceed to T0.01.

### 🛠️ Refactoring & Build
- [ ] **[REFACTOR] | T0.01 | ⚡CRITICAL — Build Gratitude Journal Notion Template**
  - **Impact:** `/Gratitude Journal and Mood Log/notion_screenshots/`, `/docs/`
  - **Details:**
    1. **[ARCHITECTURE]** Create `[DB] Backend`. Move `Journal Entries` database inside. Create Linked Views on dashboard (Calendar view for mood trends).
    2. **[FORMULA]** Add `Mood Badge` property: `ifs(prop("Mood Score") >= 8, "😊 Great", prop("Mood Score") >= 5, "😐 Okay", "😔 Low")`. Add `Gratitude Streak` formula using `dateBetween()` to count consecutive days with entries.
    3. **[NAVIGATION]** Synced Block at top for Navigation Menu.
    4. **[FOOTER]** Synced Block at bottom (Traffic Footer) with Moorish Dev brand mention.
    5. **[SEO]** Toggle titled `[Admin] SEO Metadata` with SEO Title, Meta Description, 10 Keywords.
    6. **[BUTTON]** Add Button: "✍️ New Daily Entry" that creates a new journal page with today's date.
    7. **[CALLOUT]** Gray Callout "How to Use": (1. Duplicate, 2. Write Daily, 3. Track Your Mood Over Time).
  - **Affiliate Check:** N/A

### 📄 Documentation
- [ ] **[CONTENT] | D8.01 | 🔴 HIGH — Populate `docs/Database_Schema.md`**
- [ ] **[CONTENT] | D8.02 | ⚠️ MEDIUM — Populate `marketing/Launch_Copy.md`**
- [ ] **[CONTENT] | D8.03 | ⚠️ MEDIUM — Populate `setup_guide/Setup_Guide.md`**

### 🚀 Launch
- [ ] **[MARKETING] | L8.01 | 🟢 LOW — Publish to Notion Template Gallery**

---

## Summary

| Phase | Tasks | Done | Remaining |
|-------|-------|------|-----------|
| Init & Structure | 1 | 1 | 0 |
| Build & Refactor | 1 | 0 | 1 |
| Documentation | 3 | 0 | 3 |
| Launch | 1 | 0 | 1 |
| **TOTAL** | **6** | **1** | **5** |

> **Priority Order**: T0.01 → D8.01 → D8.02 → D8.03 → L8.01
