# swimmy-contact-form — Fields Reference
# HubSpot Design Manager → Module fields
# Embeds a standard HubSpot form and applies custom Figma-spec minimal styling:
# Borderless underline-only fields, 64px vertical gap, custom dropdown chevron, and a full-width navy button.

| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 1 | Form | contact_form       | (select form in page editor) |
| 2 | Text | required_note      | ＊必須項目   |

## HubSpot Form Setup Instructions (Old Form Editor)
In HubSpot **Marketing → Lead Capture → Forms**:
1. Create a **Regular embedded form** using the **Old form editor** from scratch.
2. Add the following 5 fields:
   - **Inquiry Type / お問い合わせ種別:** Dropdown select (Options: `業務のご相談`, `パートナー・専門家として参加したい`, `その他`). Required. Placeholder: `選択してください`.
   - **Name / お名前:** First name. Required. Placeholder: `お名前`.
   - **Email / メールアドレス:** Email. Required. Placeholder: `email@example.com`.
   - **Company / 会社名（任意）:** Company name. Optional. Placeholder: `貴社名`.
   - **Message / ご相談内容:** Message (existing property set to multi-line text). Required. Placeholder: `ご相談内容をご記入ください`.
3. Submit button text: `Send Message ↗`.
4. In Options tab, set styling to default / inherit from theme (no HubSpot form theme).
5. Set Thank-you message: `お問い合わせありがとうございます。`

## Design & CSS Notes
- Container max-width: 860px centered.
- Input styling: All inputs/selects/textareas render without border boxes, with only a 1px `#DCE5E7` bottom hairline (`padding: 0 0 36px`). Focus color: `#233E55`.
- Textarea height: 217px min-height matching Figma specification.
- Required note ("＊必須項目"): Injected above the submit button via CSS pseudo-element `--sw-note`.
- Submit button: Full-width navy `#233E55` button with white text and 400 weight.
- Module label in HubSpot: "Swimmy Contact Form"
- Section settings in page editor: Padding `0px`, Full width.
