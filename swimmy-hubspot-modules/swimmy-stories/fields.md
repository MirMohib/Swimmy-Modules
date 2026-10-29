# swimmy-stories — Fields Reference
# HubSpot Design Manager → Module fields
# Stories are automatically pulled from HubSpot Blog (published posts only).
# Post order: oldest published = 01 (newest_first OFF). Turn ON to show newest as 01.

| #  | Type    | HubL Variable Name  | Default Value                                                              |
|----|---------|---------------------|----------------------------------------------------------------------------|
| 1  | Text    | top_label_left      | 02 / REAL STORIES                                                          |
| 2  | Text    | top_label_right     | ともに向き合った、その現場から。                                            |
| 3  | Text    | heading             | From Our Work.                                                             |
| 4  | Text    | intro               | これまでの仕事を振り返ると、最初から答えが用意されていた案件は、ほとんどありません。//異なる国の制度や商習慣、事業を取り巻く環境、//そして一緒に働く人たち。//それぞれの事情に向き合いながら、必要なことを一つずつ進めてきました。//ここでは、その一部をご紹介します。 |
| 5  | Text    | read_text           | 詳しく読む ↗                                                               |
| 6  | Text    | all_text            | Explore All Stories ↑                                                      |
| 7  | Link    | stories_page_link   | (leave blank, fill when Partners' Stories page is published)               |
| 8  | Number  | max_posts           | 50                                                                         |
| 9  | Boolean | newest_first        | OFF (oldest post = Story 01)                                               |

## Blog post setup (for each story)
Each story = one HubSpot Blog post. Fill these fields in the blog editor:
- Title (ブログのタイトル): full story title shown in the home card
- Featured image (キービジュアル): story photo
- Meta description (メタディスクリプション): 1–2 line summary shown under the title
- Tags (タグ): Add 2 tags per story:
  1. English category tag: e.g. "CHINA / BUSINESS OPERATIONS" (used in home list and story header)
  2. Japanese short tag: e.g. "中国撤退" (used in Partners' Stories jump index)
- URL slug (コンテンツスラッグ): short English slug e.g. "china-withdrawal"
- Author (執筆者): required to publish

## Story content (publish in this order — numbering is by publish date)
Story 01 — slug: china-withdrawal         category tag: CHINA / BUSINESS OPERATIONS    japanese tag: 中国撤退
Story 02 — slug: cross-border-business    category tag: CROSS-BORDER BUSINESS          japanese tag: 海外事業
Story 03 — slug: accounting-tax           category tag: ACCOUNTING & TAX               japanese tag: 会計・税務
Story 04 — slug: valuation-partnership    category tag: VALUATION / PARTNERSHIP        japanese tag: 資産評価

## Notes
- Links: read_text links go to stories_page_link + "#story-{post.id}" (auto anchor).
- Module label in HubSpot: "Swimmy Stories"
- stories_page_link: fill this after Partners' Stories page is published.
