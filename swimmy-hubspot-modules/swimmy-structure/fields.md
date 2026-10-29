# swimmy-structure — Fields Reference
# HubSpot Design Manager → Module fields
# Used on Company page (Section 01 / STRUCTURE) to display organizational structure and related business entities.

| # | Type   | HubL Variable Name | Label       | Setup / Default Value |
|---|--------|--------------------|-------------|-----------------------|
| 1 | Text   | top_label          | Top Label   | `01 / STRUCTURE` |
| 2 | Text   | heading            | Heading     | `Swimmy` |
| 3 | Text   | intro              | Sub-heading | `ブランドの核として、各事業体と有機的に結びつきます。` |
| 4 | Choice | bg_color           | Background  | Choices: `White` = `white`, `Grey` = `grey`, `Blue-grey` = `blue`. Default: `grey` |

Repeater Group:
- Group Label: `Rows`
- HubL Variable Name: `rows`
- Repeater options: Min: 1, Default count: 3

Fields inside `rows` group:
| # | Type      | HubL Variable Name | Label | Default Value |
|---|-----------|--------------------|-------|---------------|
| 1 | Text      | row_term           | Term  | (e.g. `Core Business`, `Joint Venture`) |
| 2 | Rich text | row_value          | Value | (e.g. entity name + bullet story link) |

## Rich Text (`row_value`) Formatting Conventions:
- **Normal paragraph:** 22px regular
- **Bullet list:** Renders as 18px underline link to a story
- **Heading 4 (見出し4):** 16px (e.g. "—" placeholder)

## Default Rows Content
Row 1:
- `row_term`: `Core Business`
- `row_value`:
  - Normal: Allastarsea China.
  - Bullet: 中国BPO / (a) Partners’ Story →
  - Normal: Allastarsea Accounting firm.
  - Bullet: 日本の会計・税務 / (c) Partners’ Story →

Row 2:
- `row_term`: `Joint Venture`
- `row_value`: 見出し4: —

Row 3:
- `row_term`: `Investment / Partnership`
- `row_value`:
  - Normal: Mirai Partner (Japan).
  - Bullet: 日本ブランドと海外事業の橋渡し / (b) →
  - Normal: HIC/CIV (China) Japan Desk.
  - Bullet: 資産評価 / (d) Partners’ Story →

## Notes
- Single-line line breaks: Use `//` in `heading` and `intro` to insert `<br>`.
- Module label in HubSpot: "Swimmy Structure"
- Section settings in page editor: Padding `0px`, Full width.
