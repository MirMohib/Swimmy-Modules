# swimmy-text-section — Fields Reference
# HubSpot Design Manager → Module fields
# Used across the Our Story page (Sections 01, 02, 03, 04).
# A versatile multi-mode editorial section supporting text-only, split with image (left/right), and wide mode (64px heading + full-width 1240px image).

| # | Type   | HubL Variable Name | Label        | Setup / Default Value |
|---|--------|--------------------|--------------|-----------------------|
| 1 | Text   | top_label          | Top Label    | `01 / BEGINNINGS` |
| 2 | Text   | heading            | Heading      | `「自分の力で生活する」//というスタイルを求めて` |
| 3 | Rich text | prose           | Prose        | (see default copy below) |
| 4 | Choice | bg_color           | Background   | Choices: `White` = `white`, `Grey` = `grey`, `Blue-grey` = `blue`. Default: `white` |
| 5 | Image  | image              | Image        | Optional. If empty, renders text-only layout |
| 6 | Choice | image_side         | Image Side   | Choices: `Left` = `left`, `Right` = `right`. Default: `left` |
| 7 | Text   | big_heading        | Big Heading  | Optional. If filled, switches module into "wide" mode (64px heading + full width 1240x520 image) |

## Layout Modes (Automatic based on fields):
1. **Text-only:** `image` is empty and `big_heading` is empty. Renders 440px heading left / 680px prose right.
2. **Split Image + Copy:** `image` is uploaded. Renders 560x560 image on the `image_side` (left or right) and copy vertically centered on the other side.
3. **Wide:** `big_heading` is populated. Renders 64px `big_heading` across top, full-width 1240x520 image, then 38px grey sub-heading left and prose right.

## Rich Text (`prose`) Conventions:
- **Normal paragraph:** 20px, `font-weight: 600`
- **Heading 4 (見出し4):** 18px, `font-weight: 600` (smaller contextual paragraph)
- **Heading 3 (見出し3):** 22px, `font-weight: 600` (closing statement in wide layout)

## Default Content for 01 / BEGINNINGS
- `top_label`: `01 / BEGINNINGS`
- `heading`: `「自分の力で生活する」//というスタイルを求めて`
- `prose`:
  1. Normal: 20代の頃、いわゆる自分探しの延長だったのかもしれませんが、キャリアの変遷を重ねる中で、「自分の力で生活する」というスタイルを志向するようになりました。
  2. 見出し4: 一時はシンガポールでファンド会社の立ち上げに関わり、ファンドマネージャー業務に携わっていたこともあります。
  3. Normal: 群れるタイプでも、外向的な性格でもありませんが、どうも人と人の間にあるビジネスで、誰かの役に立つことが好きなようです。

## Notes
- Single-line line breaks: Use `//` in `heading` and `big_heading` to insert `<br>`.
- Module label in HubSpot: "Swimmy Text Section"
- Section settings in page editor: Padding `0px`, Full width.
