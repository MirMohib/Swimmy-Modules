# swimmy-featured — Fields Reference
# HubSpot Design Manager → Module fields
# Static / Direct Fields (No dynamic blog post fetch)
# Use "//" in text fields to create a line break.

| #  | Type       | HubL Variable Name | Default Value                                                              |
|----|------------|--------------------|----------------------------------------------------------------------------|
| 1  | Text       | top_label_left     | 04 / FEATURED STORY                                                        |
| 2  | Text       | top_label_right    | ひとつの仕事を、深く。                                                      |
| 3  | Text       | category_tag       | CHINA / BUSINESS WITHDRAWAL                                                |
| 4  | Text       | heading            | 中国撤退を、//3年かけて終えた。                                             |
| 5  | Text       | subheading         | 任せていた中国事業は、思うようには伸びなかった。//その後始末から、すべてが始まった。 |
| 6  | **Image**  | **image**          | (Upload featured story photograph)                                         |
| 7  | Text       | image_caption      | SHANGHAI, CHINA PARTNERS' STORIES / 01                                     |
| 8  | Text       | aside_big          | 3Years                                                                     |
| 9  | Text       | aside_text         | 一つずつ、//前に進めていく。                                                |
| 10 | **Rich text** | **content**     | (see default content below)                                                |
| 11 | Text       | end_heading        | 事業は、思った通りには進まない。//だからこそ、一緒に動く人間が必要になる。  |
| 12 | Text       | end_text           | 私たちは、その「動く部分」を担っています。                                  |
| 13 | Text       | button_text        | Read Full Story ↗                                                          |
| 14 | Link       | button_link        | (select Partners' Stories page or enter URL)                               |

---

## Content default text (Rich text field: `content`)
Paste into the rich text field (or HTML source):

```html
<p>10年間、中国側パートナーに任せて続けてきた事業。<br>期待していたほどの拡大はなく、自社で立て直すための人材もいない。<br>そんな状況から、中国事業の整理が始まりました。</p>
<p>最初に必要だったのは、大きな戦略を描くことではありませんでした。<br>会計帳簿、契約書、印鑑、資産、税務、労務。<br>会社を普通に動かせる状態に戻すために、目の前の問題を一つずつ整理していくことでした。</p>
<p>持分譲渡や取引の清算、銀行口座の回復など、解決しなければならないことは数多くありました。<br>途中にはロックダウンもありました。それでも、一つずつ進めていきました。</p>
<p>すべての清算が終わるまでに、3年を要しました。</p>
```

---

## Notes
- Module label in HubSpot: "Swimmy Featured"
- All dynamic `blog_recent_posts` queries have been removed. Content is now directly editable from the page editor.
- Fallback variable names are also supported for backward-compatibility (`prose`/`excerpt` for content, `featured_image` for image, `caption_prefix` for image caption, `stories_page_link` for button link).
