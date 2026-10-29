# swimmy-about — Fields Reference
# HubSpot Design Manager → Module fields
# Use "//" in text fields to create a line break.
# NOTE: "body" is reserved in HubSpot — prose field is named "prose".

| #  | Type       | HubL Variable Name | Default Value                                      |
|----|------------|--------------------|----------------------------------------------------|
| 1  | Text       | top_label_left     | 03 / OUR STORY                                     |
| 2  | Text       | top_label_right    | Why Swimmy Exists                                  |
| 3  | Text       | heading            | 人と人の間にあるビジネスで、//誰かの役に立つことが//好きなようです。 |
| 4  | Text       | big_word           | Together.                                          |
| 5  | Rich text  | prose              | (see content below)                                |
| 6  | Text       | link_text          | Read Our Story ↗                                   |
| 7  | Link       | link               | (leave blank, fill when Our Story page is ready)   |

## prose default content (Rich text field)
Paste as plain text (Ctrl+Shift+V), then apply heading levels from toolbar:

1. [Normal] Swimmyは、それぞれの強みを持つ人が、自分らしさを失わずに集まり、事業家とともに歩むためのプラットフォームです。
2. [Normal] 私たちはこれまで、中国をはじめとするさまざまな現場で、会計・税務などの専門業務から、事業の立ち上げ、パートナーシップの構築まで、幅広い仕事に携わってきました。
3. [見出し4 / Heading 4] その中で出会ったのは、異なる経験や専門性を持ちながら、目の前の仕事に真剣に向き合う人たちでした。
4. [Normal — use Shift+Enter between lines]
   Swimmyという名前は、絵本「スイミー」に由来します。
   小さな魚たちが力を合わせ、大きな海を泳ぐ。
   それぞれの得意を持つ人が集まることで、ひとりではできないことができる。
   その姿が、私たちの目指すあり方と重なっています。
5. [見出し3 / Heading 3 — use Shift+Enter between lines]
   海図なき航海に、
   あなたひとりで出なくていい。

## Rich text heading convention (tell the client)
| In rich text editor | Appears on page          |
|---------------------|--------------------------|
| Normal paragraph    | 20px, semi-bold          |
| 見出し4 (Heading 4) | 16px, smaller paragraph  |
| 見出し3 (Heading 3) | 22px bold, closing quote |
| Shift + Enter       | Line break, no new para  |

## Notes
- Module label in HubSpot: "Swimmy About"
- big_word can include a period: "Together." — Figma layer shows "Together." with full stop.
