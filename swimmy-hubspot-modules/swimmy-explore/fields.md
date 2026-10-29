# swimmy-explore — Fields Reference
# HubSpot Design Manager → Module fields
# Rows are built from a repeatable group field (max 4 fields per group in HubSpot).
# Add rows in the page editor via "Add item" button.

## Simple fields (3)
| #  | Type  | HubL Variable Name | Default Value                                                              |
|----|-------|--------------------|----------------------------------------------------------------------------|
| 1  | Text  | top_label          | 05 / EXPLORE SWIMMY                                                        |
| 2  | Text  | heading            | あなたに合った形で、//Swimmyを知る。                                        |
| 3  | Text  | intro              | 私たちの関わり方、これまでの仕事、そしてSwimmyが生まれた背景。//それぞれのページから、Swimmyについて知っていただければ幸いです。 |

## Repeatable group field (HubL variable name: rows)
Create 4 fields inside the group, then make the group repeatable (min 1, default count 3):

| Type  | HubL Variable Name (inside group) |
|-------|-----------------------------------|
| Text  | row_title                         |
| Text  | row_text                          |
| Text  | row_link_text                     |
| Link  | row_link                          |

## How to create the group in HubSpot Design Manager
1. First create the 4 fields above as regular fields (not inside a group yet).
2. In the Fields section, click Actions → Group (グループ).
3. Select all 4 fields → Create group.
4. Edit the group: label = "Rows", HubL variable name = "rows".
5. In the group's Repeater options: toggle ON, minimum = 1, default count = 3.

## Row content (fill in page editor after adding module)
| row_title          | row_text                                                                                 | row_link_text    |
|--------------------|------------------------------------------------------------------------------------------|------------------|
| What We Do         | 実務を支えることから、事業の当事者として関わることまで。//Swimmyの3つの関わり方をご紹介します。 | Explore ↗        |
| Partners' Stories  | パートナーとともに向き合ってきた課題や、実際の取り組みを、一つひとつのストーリーとしてご紹介します。 | Read Stories ↗   |
| Our Story          | Swimmyが生まれた背景と、私たちが大切にしている考え方について。                             | Discover ↗       |

## Notes
- row_link: leave blank until target pages are published; span (not <a>) is shown when empty.
- The whole row becomes clickable (via ::after) when row_link is filled.
- Numbers (01, 02, 03) are generated automatically from loop.index — do not add them to row_title.
- Use "//" in row_text to insert line breaks.
- Module label in HubSpot: "Swimmy Explore"
