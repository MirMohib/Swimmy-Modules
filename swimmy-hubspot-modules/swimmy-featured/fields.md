# swimmy-featured — Fields Reference
# HubSpot Design Manager → Module fields
# Featured story is selected dynamically via Page field (or falls back to latest/oldest blog post).
# Custom Image and Content fields allow overriding the dynamic blog post image and body!

| #  | Type       | HubL Variable Name | Default Value                                                              | Description |
|----|------------|--------------------|----------------------------------------------------------------------------|---|
| 1  | Text       | top_label_left     | 04 / FEATURED STORY                                                        | Top left label |
| 2  | Text       | top_label_right    | ひとつの仕事を、深く。                                                      | Top right label |
| 3  | **Page**   | **featured_story** | (leave blank — select from picker in page editor)                          | Selects blog post dynamically |
| 4  | Boolean    | newest_first       | OFF (must match swimmy-stories module setting)                              | Order calculation |
| 5  | **Image**  | **image**          | (leave empty to use blog post featured image; or upload custom image)      | **Custom Image field** (overrides dynamic image) |
| 6  | Text       | caption_prefix     | SHANGHAI, CHINA PARTNERS' STORIES                                          | Caption prefix before story number |
| 7  | Text       | aside_big          | 3Years                                                                     | Left column big stat |
| 8  | Text       | aside_text         | 一つずつ、//前に進めていく。                                                | Left column note |
| 9  | **Rich text** | **content**     | (leave blank to use blog post body; or enter custom 4-paragraph story text)| **Custom Story Content field** (overrides dynamic body) |
| 10 | Text       | end_heading        | 事業は、思った通りには進まない。//だからこそ、一緒に動く人間が必要になる。  | Closing heading |
| 11 | Text       | end_text           | 私たちは、その「動く部分」を担っています。                                  | Closing text |
| 12 | Text       | button_text        | Read Full Story ↗                                                          | Button text |
| 13 | Link       | stories_page_link  | (fill link to Partners' Stories page)                                      | Destination link (auto-appends #story-{id}) |

---

## Dynamic Data vs Field Overrides
| Element | Source |
|---|---|
| Category Tag (top centered) | **Dynamic** from selected blog post's first tag (`tag.name`) |
| Title (`<h2>`) | **Dynamic** from selected blog post's title (`featured.name`) |
| Subheading / Summary | **Dynamic** from selected blog post's meta description (`featured.meta_description`) |
| **Story Image** | **Field override** (`module.image`): If uploaded, uses this image; if blank, uses dynamic blog post image (`featured.featured_image`) |
| Story Number | **Dynamic** calculated from ordering (`/ 01`, `/ 02`...) |
| **Story Content (Prose)** | **Field override** (`module.content` or `module.excerpt`): If filled, uses this custom content; if blank, uses dynamic blog post body |
| Button Link | **Dynamic** `stories_page_link` + `#story-{featured.id}` |

---

## Content default text (Rich text field: `content`)
Agar custom text enter karna ho to is text ko rich text field mein daal sakte hain:

```html
<p>10年間、中国側パートナーに任せて続けてきた事業。<br>期待していたほどの拡大はなく、自社で立て直すための人材もいない。<br>そんな状況から、中国事業の整理が始まりました。</p>
<p>最初に必要だったのは、大きな戦略を描くことではありませんでした。<br>会計帳簿、契約書、印鑑、資産、税務、労務。<br>会社を普通に動かせる状態に戻すために、目の前の問題を一つずつ整理していくことでした。</p>
<p>持分譲渡や取引の清算、銀行口座の回復など、解決しなければならないことは数多くありました。<br>途中にはロックダウンもありました。それでも、一つずつ進めていきました。</p>
<p>すべての清算が終わるまでに、3年を要しました。</p>
```
