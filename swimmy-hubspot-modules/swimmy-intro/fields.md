# swimmy-intro — Fields Reference
# HubSpot Design Manager → Module fields
# Use "//" in text fields to create a line break (handled by the br_lines macro in HTML).

| #  | Type  | HubL Variable Name | Default Value                                                              |
|----|-------|--------------------|----------------------------------------------------------------------------|
| 1  | Text  | top_label_left     | 01 / WORKING TOGETHER                                                      |
| 2  | Text  | top_label_right    | 私たちの関わり方                                                            |
| 3  | Text  | intro_heading      | それぞれの強みを持ち寄り、//事業を前に進める。                              |
| 4  | Text  | intro_lead         | Swimmyは、特定のサービスだけを提供する会社ではありません。//事業のフェーズや課題に応じて、実務を支えることもあれば、事業の当事者として関わることもあります。 |
| 5  | Text  | intro_note         | 関わり方は一つではありません。//大切なのは、その時々に必要な役割を担い、パートナーとともに進んでいくことです。 |
| 6  | Text  | svc_label          | WHAT WE DO                                                                 |
| 7  | Text  | svc_heading        | 事業に合わせて、//関わり方を変える。                                        |
| 8  | Text  | svc_items          | 01 Stabilize Operations//02 Build & Commit//03 Design & Structure          |
| 9  | Text  | svc_text           | 日々の業務を安定させることから、新たな事業への参画、国や分野を横断した事業構造の設計まで。//それぞれの課題に応じた形で、必要な役割を担います。 |
| 10 | Text  | svc_link_text      | Explore What We Do ↗                                                       |
| 11 | Link  | svc_link           | (leave blank)                                                              |
| 12 | Text  | spot_label         | PARTNERS' STORIES                                                          |
| 13 | Image | spot_image         | (upload city/partners preview photo from Figma layer iStock-600384474)     |
| 14 | Text  | spot_heading       | 中国撤退を、//3年かけて終えた。                                             |
| 15 | Text  | spot_text          | 任せていた中国事業は、思うようには伸びなかった。//その後始末から、すべてが始まった。 |
| 16 | Text  | spot_link_text     | Read Full Story ↗                                                          |
| 17 | Link  | spot_link          | (leave blank, fill when Partners' Stories page is ready)                   |
| 18 | Text  | story_label        | OUR STORY                                                                  |
| 19 | Text  | story_heading      | Real Stories//of Working//Together                                         |
| 20 | Text  | story_text         | 人と人の間にあるビジネスで、//誰かの役に立つことが好きなようです。          |
| 21 | Text  | story_link_text    | Discover Our Story ↗                                                       |
| 22 | Link  | story_link         | (leave blank, fill when Our Story page is ready)                           |

## Notes
- svc_items uses "//" to split the 3 service lines. The HTML loops over them to build a <ul>.
- spot_image: export from Figma at 2x, compress, upload to File Manager.
- Module label in HubSpot: "Swimmy Intro"
