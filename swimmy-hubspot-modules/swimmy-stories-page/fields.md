# swimmy-stories-page — Fields Reference
# HubSpot Design Manager → Module fields
# Used on the Partners' Stories page to display full story sections dynamically populated from HubSpot blog posts.

| # | Type    | HubL Variable Name | Default Value      |
|---|---------|--------------------|--------------------|
| 1 | Text    | kicker             | PARTNERS’ STORIES  |
| 2 | Text    | back_text          | Back to stories ↑  |
| 3 | Boolean | newest_first       | OFF                |

## Post Formatting Guide for Editors
Each blog post renders as a complete full-width story section:
- **Header:** Label (`01 / CATEGORY`), Featured image (`1240 x 480`), Story title (`post.name`, 38px bold).
- **Context Column (left):** "PARTNERS’ STORIES" kicker + Large 64px blue story index number (`01`).
- **Story Body (right):**
  - Normal paragraph: 20px bold. Single blank line between paragraphs.
  - Subheadings: **見出し3 (Heading 3)** — 25px bold subheadings.
  - Bullet items: Render automatically with "・" bullet prefix.
  - Closing Quote: Add a standard HubSpot **Quote block** at the end of the post — styled automatically with a top hairline border `#dce5e7` and 22px bold text.
- **Back link:** "Back to stories ↑" links to `#story-index` on the intro module.

## Notes
- Module label in HubSpot: "Swimmy Stories Page"
- Section settings in page editor: Padding `0px`, Full width.
