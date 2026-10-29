# swimmy-letter — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the closing narrative block on the Our Story page (Grey #f8f9f7 background).
# Features a two-column layout (320px heading / 800px letter), signature, hairline border, profile block, and "Read Partners' Stories ↗" link.

| # | Type      | HubL Variable Name | Default Value |
|---|-----------|--------------------|---------------|
| 1 | Text      | heading            | これからも、//共に。 |
| 2 | Rich text | letter             | (see default copy below) |
| 3 | Rich text | profile            | (see default copy below) |
| 4 | Text      | link_text          | Read Partners’ Stories ↗ |
| 5 | Link      | link               | (link to Partners' Stories page) |

## Default Content for `letter`:
Paste with Ctrl + Shift + V then format:
1. **見出し4:** 私たちは、いわゆる“引き出し”の数は多い方だと思います。 ⇧Enter ただ、それは最初からあったものではなく、一つ一つの現場でお客様に鍛えられて増えてきたものです。
2. Normal: これからも、その引き出しは増え続けていくはずです。
3. Normal: こうした積み重ねの中で、私たちの関わり方は、少しずつ他にはない形になってきているのかもしれません。
4. Normal: これからも、目の前の環境に向き合いながら、皆さまの海図なき航海に寄り添ってまいります。
5. Normal: 海図なき航海に、あなたひとりで出なくていい。 ⇧Enter 皆さまのビジネスの成功を願って。
6. **見出し3:** 2026年4月 ⇧Enter 星野 海 / Hoshino Kai

## Default Content for `profile`:
Normal paragraph with Shift + Enter for lines:
PROFILE / 星野海（日本国税理士） ⇧Enter 三井物産株式会社、KPMG（現あずさ監査法人）、みずほ証券等 ⇧Enter 東京大学卒

## Rich Text Hierarchy:
- Paragraph (Normal): 18px, weight 600
- Heading 4 (見出し4): 20px, weight 600
- Heading 3 (見出し3): 22px, weight 600 (used for date & founder signature)
- Profile text: 20px, weight 600

## Notes
- Single-line line breaks: Use `//` in `heading` to insert `<br>`.
- Module label in HubSpot: "Swimmy Letter"
- Section settings in page editor: Padding `0px`, Full width.
