# swimmy-term-rows — Fields Reference
# HubSpot Design Manager → Module fields
# Used on Our Story (Section 05 / OUR BELIEFS). Repeater group with hairline rule above each item.

| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 1 | Text | top_label          | 05 / OUR BELIEFS |
| 2 | Text | heading            | プロフェッショナルが//有機的に結びつく時代へ |

Repeater Group:
- Group Label: `Beliefs`
- HubL Variable Name: `beliefs`
- Repeater options: Min: 1, Default count: 3

Fields inside `beliefs` group:
| # | Type      | HubL Variable Name | Label     | Default Value |
|---|-----------|--------------------|-----------|---------------|
| 1 | Text      | row_term           | Term      | `Connected`   |
| 2 | Rich text | row_text           | Text      | (see example below) |

## Default Rows Content
Row 1:
- `row_term`: `Connected`
- `row_text`: リモートワーク環境やAIの普及により、大きな組織に依存せず実力のある個人が結びつく流れが加速するでしょう。 ⇧Enter 創業以来こういった方達を支援したいと思い続けてきました。 ⇧Enter Swimmyはプロフェッショナルを支える場であり続けます。

Row 2:
- `row_term`: `“Modern” Style`
- `row_text`: 昔ながらの顧問契約や「先生」と呼ばれるような関係ではなく、 ⇧Enter SaaSのように透明で、対等で、必要なときに頼れる関係。 ⇧Enter それが私たちの目指すプロフェッショナルのあり方です。

Row 3:
- `row_term`: `Fair Value`
- `row_text` (見出し4 = 18px): 手間や時間を売るのではなく、事業が前に進むことそのものに価値を置く。 ⇧Enter 成果に見合ったフェアな報酬設計を大切にしています。

## Rich Text Formatting:
- Normal paragraph: 20px, weight 600
- Heading 4 (見出し4): 18px, weight 600

## Notes
- Single-line line breaks: Use `//` in `heading` to insert `<br>`.
- Module label in HubSpot: "Swimmy Term Rows"
- Section settings in page editor: Padding `0px`, Full width.
