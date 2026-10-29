# swimmy-contact-hero — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the top hero section on the Contact page.
# Uses rich text for `copy` to provide effortless line breaks and editorial flexibility.

| # | Type      | HubL Variable Name | Default Value |
|---|-----------|--------------------|---------------|
| 1 | Text      | top_label          | CONTACT / GET IN TOUCH |
| 2 | Text      | heading            | Contact       |
| 3 | Rich text | copy               | (see default HTML below) |

## Default Content for `copy`:
In the rich text editor toolbar, open **Source code (<>)** and paste:
```html
<p>どのようなご相談でも構いません。<br>内容に応じて、適切なメンバーが対応いたします。</p>
```

## Layout & Design Specifications:
- Desktop dimensions: 1440 × 720px, `#FFFFFF` background.
- Padding: `180px 100px`, `76px` gap between elements.
- Typography:
  - Eyebrow: 16px, `font-weight: 600`, color `#55798F`
  - Heading: 64px, `font-weight: 700`, line-height 145%, color `#24313B`
  - Copy: 22px, `font-weight: 400`, line-height 200%, max-width 820px, color `#24313B`
- Module label in HubSpot: "Swimmy Contact Hero"
- Section settings in page editor: Padding `0px`, Full width.
