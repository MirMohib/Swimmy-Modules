# swimmy-contact-cta — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the simplified dark navy contact banner on subpages (What We Do, Partners' Stories, Our Story).
# Different from the homepage `swimmy-contact` banner (160px padding, no eyebrow split label, single button).

| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 1 | Text | big_word           | Contact       |
| 2 | Text | message            | どのようなご相談でも構いません。//内容に応じて、//適切なメンバーが対応いたします。 |
| 3 | Text | button_text        | Talk to Us ↗  |
| 4 | Link | button_link        | (fill with link to Contact page) |

## Notes
- Single-line line breaks: Use `//` in `message` to insert `<br>`.
- Arrow `↗`: Rendered below `big_word`. Links to `button_link` URL if set, otherwise renders as a plain decorative span.
- Module label in HubSpot: "Swimmy Contact CTA"
- Section settings in page editor: Padding `0px`, Full width.
