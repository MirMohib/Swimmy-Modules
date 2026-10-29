# swimmy-stories-intro — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the intro section on the Partners' Stories page. Combines page intro and dynamic blog post jump index in one module to preserve Figma 180px/76px spacing.

| # | Type      | HubL Variable Name | Default Value |
|---|-----------|--------------------|---------------|
| 1 | Text      | top_label          | PARTNERS’ STORIES / REAL STORIES OF WORKING TOGETHER |
| 2 | Text      | heading            | Partners’ Stories |
| 3 | Rich text | intro              | (see default copy below) |
| 4 | Boolean   | newest_first       | OFF (keep same as Stories list) |

## Default Content for intro
Paste with Ctrl + Shift + V then format (Shift + Enter for line breaks, Enter for paragraph breaks):
- Paragraph 1: 事業は、思った通りには進まない。
- Paragraph 2: 構想を現実に落とし込むとき、必ず摩擦が生まれる。 ⇧Enter Swimmyは、その摩擦を引き受け実行可能な形に変えるパートナーです。 ⇧Enter 4つの現場から、私たちの関わり方をご覧ください。

## How the Jump Index Works
- Dynamically iterates over blog posts in the same order as `swimmy-stories`.
- Identifies the Japanese tag on each post (e.g. `中国撤退`, `海外事業`, `会計・税務`, `資産評価`). If no Japanese tag exists, falls back to the first 14 characters of `post.name`.
- Renders anchor link: `#story-{{ post.id }}` with label `01 [Tag] ↓`.
- The navigation container has `id="story-index"` so the "Back to stories ↑" button in `swimmy-stories-page` smoothly jumps back up here.

## Notes
- Module label in HubSpot: "Swimmy Stories Intro"
- Section settings in page editor: Padding `0px`, Full width.
