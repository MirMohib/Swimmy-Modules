# swimmy-contact — Fields Reference
# HubSpot Design Manager → Module fields (Swimmy Contact Banner)
# Used globally across almost every page on the site.
# Use "//" in text fields to create line breaks.

## Fields Configuration Table

| #  | Type    | Label             | HubL Variable Name | Default Value                                                                                                                                           |
|----|---------|-------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Text    | Top Label Left    | `top_label`   | `06 / LET’S CONNECT`                                                                                                                                    |
| 2  | Text    | Top Label Right   | `top_text`  | `まずは、お話ししませんか。`                                                                                                                              |
| 3  | Text    | Big Title         | `title`        | `Contact`                                                                                                                   
| 4  | Text    | Heading           | `heading`          | `どのようなご相談でも構いません。//内容に応じて、//適切なメンバーが対応いたします。`                                                                   |
| 5  | Text    | Description       | `description`      | `日々の業務に関するご相談、新たな事業やパートナーシップについてのお話、専門家としての参画など、まずはお問い合わせください。//ご相談の内容に合わせて、必要な関わり方を一緒に考えていきます。` |
| 6  | Text    | Button 1 Text     | `button_text`    | `Talk to Us ↗`                                                                                                                                          |
| 7  | Link    | Button 1 Link     | `button_link`    | *(URL/Page to inquiry or booking, e.g. HubSpot meetings link)*                                                                                         |
| 8  | Text    | Button 2 Text     | `link_text`    | `Contact ↗`                                                                                                                                             |
| 9  | Link    | Button 2 Link     | `link_link`    | *(URL/Page to contact page, e.g. /contact)*                                                                                                            |

---

## HubSpot Design Manager mein kaise banayein (Step-by-step)

1. **Naya Module banayein:**
   - HubSpot Design Manager mein jao.
   - **File** → **New file** → **Module** chuno.
   - Kahan use hoga: **Pages (サイトページ)** tick karo.
   - Module content scope: **Local module** (ya Global if you want to edit it once for all pages).
   - File name: `swimmy-contact`.

2. **Code paste karein:**
   - `module.html` tab mein `module.html` ka pura code paste karo.
   - `module.css` tab mein `module.css` ka pura code paste karo.

3. **Fields add karein:**
   - Left sidebar mein **Add field (フィールドを追加)** se upar wali table ke 10 fields banayein.
   - Variable names bilkul exact match hone chahiye (`top_label_left`, `heading`, `description`, etc.).

4. **Publish karein:**
   - Upar right corner mein **Publish changes (変更を公開)** dabao.

5. **Page Editor mein use karein:**
   - Home page ya kisi bhi subpage editor mein jao.
   - Explore module ke neeche naya 1-column section add karo:
     - Section width: **Full width (100%)**
     - Section padding: Top `0px`, Bottom `0px`, Left `0px`, Right `0px`
   - Is section mein `Swimmy Contact` module drag karke drop kar do.

---

## Notes
- **Line breaks (`//`):** Heading aur description fields mein jahan bhi line break chahiye, wahan `//` type karein. HubL macro isko automatic `<br>` mein convert kar deta hai.
- **Brand link:** Agar `button_2_link` ya `button_1_link` set hai, toh left column ka "Contact ↗" text bhi clickable rehta hai aur wahi URL open karta hai.
- **Button Visibility:** Agar kisi button ka text blank chhodenge, toh woh button page par render nahi hoga.
