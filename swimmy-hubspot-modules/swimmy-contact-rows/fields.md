# swimmy-contact-rows — Fields Reference
# HubSpot Design Manager → Module fields
# Used on Company page (Section 05 / CONTACT) to display purposeful contact options with hairlines and underline links on the right.
# NOTE: Do NOT use "label" or "link" as HubL variable names as they trigger reserved keyword errors. Use "row_label" and "row_link".

| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 1 | Text | top_label          | 05 / CONTACT  |
| 2 | Text | heading_line1      | ひとりで抱えず、 |
| 3 | Text | heading_line2      | まず話してください。 |

Repeater Group:
- Group Label: `Rows`
- HubL Variable Name: `rows`
- Repeater options: Min: 1, Default count: 3

Fields inside `rows` group:
| # | Type | HubL Variable Name | Label     | Default Value |
|---|------|--------------------|-----------|---------------|
| 1 | Text | row_label          | Label     | (see items below) |
| 2 | Text | link_text          | Link Text | (see items below) |
| 3 | Link | row_link           | Link      | (link to Contact page) |

## Default Rows Content:
- Row 1:
  - `row_label`: `業務のご相談`
  - `link_text`: `BPO / 日中の進出支援など ↗`
- Row 2:
  - `row_label`: `パートナー・専門家として参加したい`
  - `link_text`: `それぞれの強みを持ち寄って ↗`
- Row 3:
  - `row_label`: `その他`
  - `link_text`: `どのようなご相談でも構いません。 ↗`

## Layout & Design Specifications:
- Desktop dimensions: 1440 × 1188px, `#FFFFFF` background.
- Padding: `180px 100px`, `76px` gap between items and hairlines.
- Hairline: 1px `#DCE5E7` placed above each row (no line below the last row).
- Row split: Left label 640px / Right link 480px with 120px gap.
- Typography: Heading 38px bold (`line-height: 175%`), row text 22px regular (`line-height: 200%`).
- Module label in HubSpot: "Swimmy Contact Rows"
- Section settings in page editor: Padding `0px`, Full width.
