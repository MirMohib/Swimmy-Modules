# Swimmy HubSpot Custom Modules

Comprehensive custom HubSpot CMS modules developed for the **Swimmy** corporate website ([swimmy.pro](https://swimmy.pro)).  
Faithfully designed and built directly from the Figma specifications (1440px desktop grid, responsive down to 390px mobile) and formatted according to HubSpot Design Manager best practices (HTML + HubL, Scoped Vanilla CSS with fluid `clamp()`, and field configuration specs).

---

## Table of Contents
1. [Design System & Theme Tokens](#design-system--theme-tokens)
2. [Universal Conventions & Best Practices](#universal-conventions--best-practices)
3. [Page-by-Page Module Architecture](#page-by-page-module-architecture)
4. [Master Module Directory (25 Modules)](#master-module-directory-25-modules)
5. [HubSpot Blog & Dual Tagging Architecture](#hubspot-blog--dual-tagging-architecture)
6. [HubSpot Design Manager Setup Instructions](#hubspot-design-manager-setup-instructions)

---

## Design System & Theme Tokens

- **CMS Platform:** HubSpot CMS (Marketing / Content Hub)
- **Grid & Viewport:** 1240px container on 1440px desktop grid; fluid responsive down to 390px mobile.
- **Typography:**
  - Latin / English: [Gothic A1](https://fonts.google.com/specimen/Gothic+A1) (weights: 400, 500, 600, 700)
  - Japanese: [Noto Sans JP](https://fonts.google.com/specimen/Noto+Sans+JP) (weights: 400, 500, 600, 700)
- **Color Palette:**
  - `Base 1` (`#FFFFFF`): Primary clean white background
  - `Base 2` (`#F8F9F7`): Header, footer, alternate section background
  - `Base 3` (`#24313B`): Primary body text, headings, dark charcoal
  - `Accent 1` (`#E7EEF0`): Soft blue-grey background ("Together." and Access blocks)
  - `Accent 2` (`#55798F`): Eyebrow labels, numbering accents, muted steel blue
  - `Accent 3` (`#233E55`): Dark navy background (Contact banners, primary buttons)
  - Borders / Hairlines: `#DCE5E7` (1px hairlines)
  - Secondary Text / Subheadings: `#657984`

---

## Universal Conventions & Best Practices

1. **Fluid Responsive Typography and Spacing:**
   All module CSS rules avoid hardcoded pixel heights or fragile breakpoints by utilizing fluid `clamp()` functions based on the 1440px desktop baseline (e.g., `clamp(24px, 2.64vw, 38px)` and `clamp(80px, 12.5vw, 180px)`).

2. **Line Breaks via `//` Delimiter:**
   Single-line HubSpot text fields escape HTML `<br>` tags. All relevant modules include the standard `br_lines` HubL macro:
   ```jinja2
   {% macro br_lines(text) %}{% for line in text|split('//') %}{{ line|trim }}{% if not loop.last %}<br>{% endif %}{% endfor %}{% endmacro %}
   ```
   Editors simply insert `//` in any heading or subtitle field to add a clean responsive line break.

3. **Reserved HubL Names in HubSpot:**
   Never name field variables `body`, `label`, or `link` in HubSpot Design Manager, as they are system keywords. Modules in this codebase use `top_label`, `row_label`, `row_link`, `intro_text`, `sec_copy`, or `prose`.

4. **Zero Padding Page Sections:**
   To guarantee pixel-perfect vertical rhythm and edge-to-edge section backgrounds, configure all sections containing these modules in the HubSpot Page Editor to:
   - **Section Width:** Full width (100%)
   - **Padding:** Top `0px`, Bottom `0px`, Left `0px`, Right `0px`

---

## Page-by-Page Module Architecture

### 1. Homepage (`/`)
1. Global Header (Elevate Theme, `#f8f9f7` background)
2. `swimmy-hero`: Hero section with split headline, CTAs, and raw ship photo with CSS curve & white fade.
3. `swimmy-intro`: 01 / WORKING TOGETHER 3-column service overview cards.
4. `swimmy-stories`: 02 / REAL STORIES ("From Our Work") dynamic recent stories list.
5. `swimmy-about`: 03 / OUR STORY ("Together.") soft blue-grey text and 100px typographic mark.
6. `swimmy-featured`: 04 / FEATURED STORY deep-dive on selected story via HubSpot Page picker.
7. `swimmy-explore`: 05 / EXPLORE SWIMMY repeater rows with index numbers.
8. `swimmy-contact`: 06 / LET'S CONNECT dark navy global contact banner with dual CTAs.
9. `swimmy-footer`: Shared global footer with branding, nav menu, and legal links.

### 2. What We Do Page (`/what-we-do`)
1. Global Header
2. `swimmy-page-hero`: `WHAT WE DO / 私たちの関わり方`, headline `We engage, adapt, and grow//with our partners.`, 3-paragraph intro.
3. `swimmy-services`: 3 alternating service sections (01 Stabilize Operations, 02 Build & Commit, 03 Design & Structure) with SVG icons, rich text, and photos.
4. `swimmy-closing`: Soft blue-grey `#e7eef0` block with large "Together" and 3 narrative paragraphs.
5. `swimmy-contact-cta`: Simplified dark navy contact invitation banner with "Talk to Us ↗" button.
6. `swimmy-footer`: Shared global footer.

### 3. Partners’ Stories Page (`/partners-stories`)
1. Global Header
2. `swimmy-stories-intro`: Page hero combined with dynamic blog jump index (`01 中国撤退 ↓`, etc.).
3. `swimmy-stories-page`: Full story loop rendering each published HubSpot blog post with hero image, context index number, rich text body, and closing blockquote.
4. `swimmy-more`: `OTHER ENGAGEMENTS / And more…` closing narrative with bottom hairline separator.
5. `swimmy-contact-cta`: Simplified dark navy contact invitation banner.
6. `swimmy-footer`: Shared global footer.

### 4. Our Story Page (`/our-story`)
1. Global Header
2. `swimmy-page-hero`: `OUR STORY / 私たちの歩み`
3. `swimmy-text-section`: Section 01 / BEGINNINGS (Text-only layout)
4. `swimmy-text-section`: Section 02 / ON THE GROUND (Grey background `#f8f9f7`, photo on left)
5. `swimmy-text-section`: Section 03 / CHALLENGES (White background, photo on right)
6. `swimmy-text-section`: Section 04 / WHY SWIMMY (Wide mode: 64px heading + full-width 1240x520 image)
7. `swimmy-term-rows`: Section 05 / OUR BELIEFS (Repeater rows: Connected, “Modern” Style, Fair Value)
8. `swimmy-letter`: Founder’s letter by Kai Hoshino, signature, hairline divider, profile, and story link.
9. `swimmy-contact-cta`: Simplified dark navy contact invitation banner.
10. `swimmy-footer`: Shared global footer.

### 5. Company Page (`/company`)
1. Global Header
2. `swimmy-info-rows`: `COMPANY / OVERVIEW` (White background, 64px heading, key-value rows: NAME, FOUNDED, BASE, SHAREHOLDERS).
3. `swimmy-structure`: `01 / STRUCTURE` (Grey background `#f8f9f7`, corporate structure: Core Business, Joint Venture, Investment / Partnership with story links).
4. `swimmy-key-facts`: `02 / KEY FACTS` (White background, 2x2 statistics grid: 60+, 200+, 20+, 2013, with footnote).
5. `swimmy-info-rows`: `03 / PRESENCE` (Grey background, 38px heading, 76px wide row gap: CHINA, JAPAN).
6. `swimmy-access`: `04 / ACCESS` (White background, soft blue-grey container `#e7eef0` with location details and inquiry CTA).
7. `swimmy-contact-rows`: `05 / CONTACT` (White background, 3 purpose-based contact rows with hairlines and underline links on the right).
8. `swimmy-footer`: Shared global footer.

### 6. Contact Page (`/contact`)
1. Global Header
2. `swimmy-contact-hero`: `CONTACT / GET IN TOUCH`, 64px "Contact" heading, and 2-line intro copy.
3. `swimmy-contact-form`: HubSpot form embed styled to Figma spec (borderless underline fields, 217px textarea, custom chevron, required note, full-width navy button).
4. `swimmy-footer`: Shared global footer.

---

## Master Module Directory (25 Modules)

```
swimmy-hubspot-modules/
├── README.md
├── swimmy-hero/             # [Home] 00: Top Hero Section
├── swimmy-intro/            # [Home] 01: Working Together (3 Columns)
├── swimmy-stories/          # [Home] 02: Real Stories / From Our Work (Blog list)
├── swimmy-about/            # [Home] 03: Our Story / "Together."
├── swimmy-featured/         # [Home] 04: Featured Story (Page picker)
├── swimmy-explore/          # [Home] 05: Explore Swimmy (Repeater rows)
├── swimmy-contact/          # [Home] 06: Full Contact Banner (Dual CTAs)
├── swimmy-page-hero/        # [Global] Reusable subpage top hero
├── swimmy-services/         # [What We Do] 01-03 Alternating services repeater
├── swimmy-closing/          # [What We Do] Closing "Together" narrative block
├── swimmy-contact-cta/      # [Global Subpages] Simplified dark navy contact banner
├── swimmy-stories-intro/    # [Stories] Intro header + dynamic jump index
├── swimmy-stories-page/     # [Stories] Dynamic full-length story reader loop
├── swimmy-more/             # [Stories] "And more…" closing narrative block
├── swimmy-text-section/     # [Our Story] Multi-mode editorial block (text/split/wide)
├── swimmy-term-rows/        # [Our Story] 05 / OUR BELIEFS repeater rows
├── swimmy-letter/           # [Our Story] Founder's letter, profile & signature
├── swimmy-info-rows/        # [Company] Key-value rows with configurable styling
├── swimmy-structure/        # [Company] 01 / STRUCTURE business entity groups
├── swimmy-key-facts/        # [Company] 02 / KEY FACTS 2x2 statistics grid
├── swimmy-access/           # [Company] 04 / ACCESS office location container
├── swimmy-contact-rows/     # [Company] 05 / CONTACT purpose-based inquiry rows
├── swimmy-contact-hero/     # [Contact] Top hero section with rich text copy
├── swimmy-contact-form/     # [Contact] Underline-only HubSpot Form embed
└── swimmy-footer/           # [Global] Universal footer leveraging global site settings & menus
```

Each module folder contains:
- `module.html`: Validated HubL template code
- `module.css`: Fluid responsive CSS with zero leakage
- `fields.md`: Complete Design Manager fields schema, variable names, and copy defaults

---

## HubSpot Blog & Dual Tagging Architecture

To support both the English category labels on the homepage and the Japanese jump index links on the Partners' Stories page, assign **two tags** to each blog post in HubSpot:

| Story | Slug | Tag 1 (English Category) | Tag 2 (Japanese Short Tag) |
|---|---|---|---|
| Story 01 | `china-withdrawal` | `CHINA / BUSINESS OPERATIONS` | `中国撤退` |
| Story 02 | `cross-border-business` | `CROSS-BORDER BUSINESS` | `海外事業` |
| Story 03 | `accounting-tax` | `ACCOUNTING & TAX` | `会計・税務` |
| Story 04 | `valuation-partnership` | `VALUATION / PARTNERSHIP` | `資産評価` |

### Tag Detection Logic in HubL:
- **English Category Tag:** Filtered via `(t.name|regex_replace('[ -~]', ''))|length == 0` (only ASCII characters).
- **Japanese Short Tag:** Filtered via `(t.name|regex_replace('[ -~]', ''))|length > 0` (contains Japanese multi-byte characters).

---

## HubSpot Design Manager Setup Instructions

1. **Create Module:** In HubSpot Design Manager, navigate to **File → New File → Module**.
2. **Settings:** Select **Page Templates**, keep as **Local Module**, and enter the module folder name (e.g. `swimmy-services`).
3. **Configure Fields:** In the right panel, add the fields matching the specifications in the module's `fields.md`. For repeater groups, add the fields, multi-select them under **Actions → Create group**, and enable **Repeater options**.
4. **Paste Code:** Copy `module.html` into the center HTML/HubL editor and `module.css` into the CSS editor.
5. **Publish:** Click **Publish changes** (変更を公開).
6. **Add to Page:** In the Page Editor, insert a 1-column section, set section width to **Full Width**, set padding to **0px**, and drop the module in.
