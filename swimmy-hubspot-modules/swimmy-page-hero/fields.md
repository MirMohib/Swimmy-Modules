# swimmy-page-hero — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the top hero on subpages (What We Do, Our Story, Company, Contact).
# NOTE: Do NOT use "label" or "body" as HubL variable names as they are reserved in HubSpot. Use "top_label".

| # | Type      | HubL Variable Name | Default Value |
|---|-----------|--------------------|---------------|
| 1 | Text      | top_label          | WHAT WE DO / 私たちの関わり方 |
| 2 | Text      | heading            | We engage, adapt, and grow//with our partners. |
| 3 | Rich text | intro              | (see default copy below) |

## Default Content for intro (What We Do example)
Paste with Ctrl + Shift + V then format:
- Paragraph 1: 私たちは、特定のサービスを提供する会社ではありません。 ⇧Enter 事業のフェーズや課題に応じて、最適な形で関わり方を変えながら、パートナーと共に価値を高めていきます。
- Paragraph 2: アウトソーシング、事業へのコミット、ストラクチャーのデザイン。 ⇧Enter 関わり方の手段は異なっても、目的は一つ。事業の進化に、継続的に関わり続けることです。
- Paragraph 3: ただし、その関わり方は常に選択可能であるべきだと考えています。 ⇧Enter 業務単位でのご依頼から始めていただくこともできますし、 ⇧Enter 必要以上に関係を固定することはありません。

## Notes
- Single-line line breaks: Use `//` in the `heading` text field to insert `<br>`.
- Inside rich text paragraphs: Use **Shift + Enter** for line breaks within a paragraph, **Enter** for paragraph spacing.
- Module label in HubSpot: "Swimmy Page Hero"
- Section settings in page editor: Padding `0px`, Full width.
