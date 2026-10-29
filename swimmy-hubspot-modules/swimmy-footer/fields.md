# swimmy-footer — Fields Reference
# HubSpot Design Manager → Module fields
# Used as the shared global footer across all website pages.
# Leverages HubSpot global branding (`site_settings.logo_src`, `site_settings.company_name`) and HubSpot Navigation Menus (`main_menu`, `legal_menu`).

| # | Type | HubL Variable Name | Label       | Default / Setup |
|---|------|--------------------|-------------|-----------------|
| 1 | Menu | main_menu          | Main Menu   | Select primary site header menu (What We Do, Partners’ Stories, Our Story, Company, Contact) |
| 2 | Text | tagline            | Tagline     | `Different Strengths, Working Together` |
| 3 | Menu | legal_menu         | Legal Menu  | Select `Footer Legal` menu (Privacy Policy, Terms) |
| 4 | Text | top_text           | Top Link    | `Back to top ↑` |

## Global Data Sources:
- **Logo:** Automatically pulls from `site_settings.logo_src` with alt text `site_settings.logo_alt`. If no image is set, falls back to text `site_settings.company_name|default('Swimmy')`.
- **Copyright:** Automatically formats as `© {{ site_settings.company_name|default('Swimmy') }}. All rights reserved.`
- **Navigation:** Dynamically loops through items assigned to `main_menu` and `legal_menu` via the HubSpot `menu()` function.
- **Back to top:** Renders with `href="#"` to smoothly return to the page top without external dependencies.

## Layout & Design Specifications:
- Desktop dimensions: 1440 × 320px, `#F8F9F7` background.
- Padding: `80px 100px 40px`, `64px` gap between main brand row and bottom copyright row.
- Both rows share identical 2-column grid alignment: 542.8px left / 637.2px right with 60px column gap, ensuring navigation links and legal links align to the exact same vertical x-coordinate (~703px).
- Hairline: 1px `#DCE5E7` border above copyright row.
- Module label in HubSpot: "Swimmy Footer"
- Section settings in page editor: Padding `0px`, Full width.
