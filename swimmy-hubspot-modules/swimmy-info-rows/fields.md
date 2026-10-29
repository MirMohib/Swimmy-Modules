# swimmy-info-rows — Fields Reference
# HubSpot Design Manager → Module fields
# Used on Company page (Company Overview, 03 / PRESENCE, and other key-value structured blocks).
# Supports configurable background colors, heading scales (64px H1 vs 38px H2), and row gaps (60px normal vs 76px wide).

| # | Type   | HubL Variable Name | Label        | Choices / Default Value |
|---|--------|--------------------|--------------|-------------------------|
| 1 | Text   | top_label          | Top Label    | `COMPANY / OVERVIEW` (or `03 / PRESENCE`) |
| 2 | Text   | heading            | Heading      | `それぞれの強みを持つ人が集まり、//事業家とともに//進むプラットフォーム` |
| 3 | Choice | bg_color           | Background   | Choices: `White` = `white`, `Grey` = `grey`, `Blue-grey` = `blue`. Default: `white` |
| 4 | Choice | heading_size       | Heading Size | Choices: `Large 64px` = `large`, `Medium 38px` = `medium`. Default: `large` |
| 5 | Choice | row_gap            | Row Gap      | Choices: `Normal 60px` = `normal`, `Wide 76px` = `wide`. Default: `normal` |

Repeater Group:
- Group Label: `Rows`
- HubL Variable Name: `rows`
- Repeater options: Min: 1, Default count: 4

Fields inside `rows` group:
| # | Type      | HubL Variable Name | Label | Default Value |
|---|-----------|--------------------|-------|---------------|
| 1 | Text      | row_term           | Term  | (e.g. `NAME`, `FOUNDED`, `CHINA`) |
| 2 | Rich text | row_value          | Value | (e.g. company details or location text) |

## Example Configurations:
### 1. Company Overview
- `top_label`: `COMPANY / OVERVIEW`
- `heading`: `それぞれの強みを持つ人が集まり、//事業家とともに//進むプラットフォーム`
- `bg_color`: `White`
- `heading_size`: `Large 64px`
- `row_gap`: `Normal 60px`
- Rows:
  - NAME: `Swimmy株式会社 / Swimmy Inc.`
  - FOUNDED: `2013年4月`
  - BASE: `Shanghai / Hong Kong / Osaka / Yokohama`
  - SHAREHOLDERS: `Founder & Management`

### 2. 03 / PRESENCE
- `top_label`: `03 / PRESENCE`
- `heading`: `地域を越えて、つながる。`
- `bg_color`: `Grey`
- `heading_size`: `Medium 38px`
- `row_gap`: `Wide 76px`
- Rows:
  - CHINA: `Shanghai / Hong Kong / Guangdong ⇧Enter Jiangsu / Macau`
  - JAPAN: `Osaka / Yokohama`

## Notes
- Empty rows (where both term and value are blank) are automatically hidden in the template.
- Links inside `row_value` automatically receive standard underline styles.
- Module label in HubSpot: "Swimmy Info Rows"
- Section settings in page editor: Padding `0px`, Full width.
