# swimmy-services — Fields Reference
# HubSpot Design Manager → Module fields
# Used on What We Do page. Each service is an item in the repeater group "sections".
# Odd items (01, 03) render White background with Image on the Right.
# Even items (02) render Grey (#f8f9f7) background with Image on the Left.

## Fields Configuration

Repeater Group:
- Group Label: `Sections`
- HubL Variable Name: `sections`
- Repeater options: Min: 1, Default count: 3

Fields inside `sections` group:
| # | Type      | HubL Variable Name | Label       | Default / Description |
|---|-----------|--------------------|-------------|-----------------------|
| 1 | Text      | sec_name           | Section Name | `Stabilize Operations` |
| 2 | Image     | sec_icon           | Section Icon | Upload SVG icon (exported from Figma, stroke #55798F) |
| 3 | Text      | sec_heading        | Heading     | `構想を、//摩擦なく実装する。` |
| 4 | Rich text | sec_copy           | Copy        | (see formatting conventions below) |
| 5 | Image     | sec_image          | Image       | Photo (560x600, JPG 2x) |

## Rich Text (`sec_copy`) Formatting Conventions
- **Normal paragraph:** 18px bold
- **Heading 4 (見出し4):** 20px bold
- **Heading 3 (見出し3):** 22px bold (closing statement)
- **Bullet list:** Renders without bullet points as 18px underline story links
- **Shift + Enter:** Line break within paragraph

## Section 01 Example Content
- `sec_name`: `Stabilize Operations`
- `sec_heading`: `構想を、//摩擦なく実装する。`
- `sec_copy`:
  1. Normal: 事業家は、すでに理想のオペレーション像を持っています。 ⇧Enter AIを使い、最適な業務フローを描くこともできる時代です。
  2. Normal: しかし、それを現実に落とし込むには、制度・言語・実務といった壁が存在します。
  3. 見出し4: Swimmyは、そのギャップを埋めます。 ⇧Enter 会計・税務・登記・ビザなどのバックオフィス機能を、単に代行するのではなく、“構想されたオペレーション”を、 ⇧Enter 現地で実行可能な形に変換し、実装します。
  4. 見出し3: 理想を描くことと、実行することの間にある摩擦をなくす。それが、私たちの役割です。
  5. Bullet list:
     - (a) 中国BPO / Allastarsea China →
     - (c) 外資系企業の日本会計・税務 →

## Notes
- Single-line line breaks: Use `//` in `sec_heading` to insert `<br>`.
- Module label in HubSpot: "Swimmy Services"
- Section settings in page editor: Padding `0px`, Full width.
