# Template Audit & Friction Points — Gratitude Journal & Mood Log

## 1. Logo Hosting Issue (Notion API)
- **Problem:** The Notion API does not support local file uploads for page icons.
- **Resolution:** Distribute `moorish_dev_logo.png` to `assets/`. User sets it as page icon manually.

## 2. Mood Score vs. Emoji Selection
- **Problem:** A numeric `Mood Score` property (1–10) is optimal for formula-based trend calculations, but some users prefer selecting emoji moods. These are incompatible in a single property.
- **Resolution:** Use a `Mood Score` Number property (1–10) as the source of truth. Add a separate `Mood Badge` Formula property that converts the number to an emoji badge. This gives both numeric analysis AND visual clarity.

## 3. Gratitude Streak Formula Complexity
- **Problem:** Calculating a true consecutive-days streak requires checking if there's an entry for each of the past N days — this is computationally expensive and complex in Notion Formulas 2.0.
- **Resolution:** Provide a simplified "Days Since Last Entry" formula using `dateBetween(now(), prop("Date"), "days")` on the most recent entry. Document the limitation in `setup_guide/Setup_Guide.md`.

## 4. Privacy Consideration
- **Problem:** The Gratitude Journal contains personal, private content. Users may accidentally share their journal page publicly.
- **Resolution:** Add a prominent gray callout at the top of the template: "⚠️ Privacy: This page is private by default. Do NOT share the page URL publicly." This is documented in `setup_guide/Setup_Guide.md`.

## 5. Button Block API Limitation
- **Problem:** Notion's native Button blocks cannot be created via the public Notion API.
- **Resolution:** User must manually create the `✍️ New Daily Entry` button block.
