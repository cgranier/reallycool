Read the most recent weekly roundup file in the workspace (the one with the latest date in its filename), extract the INFOGRAPHIC DATA section, then output the image generation prompt below with all [[...]] placeholders replaced with the actual data. Map each data point as follows: the VALUE is the oversized stat, the LABEL is the bold descriptor, and the CONTEXT is the short description line.

---

Create a simple, modern, editorial-style infographic for a tech blog. Landscape 16:9 layout, 1920×1080px, clean white or very light grey background (#F7F9F6 or similar), green and near-black accent palette. Minimal, premium sans-serif typography throughout. Polished and readable, not busy.

**Header:**
- Title: **RCTV Weekly Roundup** (large bold)
- Subtitle: **6 Key Numbers** (lighter weight, smaller)
- Date line: **[[Week ending date]]** (small, muted, placed near subtitle)

**Body:**
Present the six data points in a 3×2 grid of equal-sized cards. Each card contains:
1. A large bold **value** (top-left, dominant — this is the visual anchor of the card)
2. A small **category icon** (top-right, simple line icon, green tint, consistent weight across all cards — use contextually appropriate icons: e.g. film camera for video, chip for hardware, trend arrow for cost/growth, calendar for dates, gavel for regulation; avoid using the same icon on more than one card)
3. A **bold label line** directly below the value (this is the stat name)
4. A **short context line** in lighter weight beneath the label (one sentence maximum)

Cards should have a white background with a very subtle shadow or light border. Generous internal padding and whitespace. Values that are text milestones (e.g. "Fall 2026") rather than numbers are acceptable — size them to fill the card the same way a number would.

**Data:**
1. Value: [[Stat 1 value]] | Label: [[Stat 1 label]] | Context: [[Stat 1 context]]
2. Value: [[Stat 2 value]] | Label: [[Stat 2 label]] | Context: [[Stat 2 context]]
3. Value: [[Stat 3 value]] | Label: [[Stat 3 label]] | Context: [[Stat 3 context]]
4. Value: [[Stat 4 value]] | Label: [[Stat 4 label]] | Context: [[Stat 4 context]]
5. Value: [[Stat 5 value]] | Label: [[Stat 5 label]] | Context: [[Stat 5 context]]
6. Value: [[Stat 6 value]] | Label: [[Stat 6 label]] | Context: [[Stat 6 context]]

**Design rules:**
- No logos, no watermarks, no photorealistic scenes
- No bar charts or charts implying comparative scale beyond the given values
- Avoid clutter — if a card has a long context line, reduce font size rather than overflow
- The value should be immediately legible at 600px wide (blog thumbnail size)
- Readable on both desktop and mobile when embedded in a blog post
