# swimmy-legal-page — Fields Reference
# HubSpot Design Manager → Module fields
# Used for Privacy Policy and Terms of Use pages.
# NOTE: Do NOT use "label" or "body" as HubL variable names as they are reserved in HubSpot. Use "top_label".

| # | Type      | HubL Variable Name | Default Value |
|---|-----------|--------------------|---------------|
| 1 | Text      | top_label          | LEGAL |
| 2 | Text      | heading            | プライバシーポリシー |
| 3 | Text      | updated_text       | 最終更新日：2026年【　】月【　】日 |
| 4 | Rich text | content_body       | (empty) |

## Notes
- Module label in HubSpot: "Swimmy Legal Page"
- Section settings in page editor: Padding `0px`, Full width.
- `updated_text` is optional — if left blank the date line is hidden.
- `content_body`: In the rich text editor, open **Source** (`<>` icon) and paste the raw HTML from Part 3 of the review doc.

## Page setup
| Page           | Title              | URL slug        | heading              |
|----------------|--------------------|-----------------|----------------------|
| Privacy Policy | プライバシーポリシー | `privacy-policy` | プライバシーポリシー |
| Terms of Use   | 利用規約           | `terms`          | 利用規約             |

## Client confirmations required before publishing
- 【会社名】, 【所在地】, 【代表者名】, 【メールアドレス】, 【担当部署】
- Section 5 【要確認】: confirm data flows to Shanghai / Hong Kong and HubSpot (USA)
- Section 7: confirm whether Google Analytics or other analytics tools are in use
- 制定日 (effective date) and 管轄裁判所 (jurisdiction court)
- Lawyer review before publishing

