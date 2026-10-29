# swimmy-key-facts — Fields Reference
# HubSpot Design Manager → Module fields
# Used on Company page (Section 02 / KEY FACTS) to display a 2x2 grid of key corporate statistics with hairlines and footnote.

| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 1 | Text | top_label          | 02 / KEY FACTS |
| 2 | Text | heading            | 積み重ねてきた実績。 |
| 3 | Text | as_of              | As of October 2026 |

Repeater Group:
- Group Label: `Stats`
- HubL Variable Name: `stats`
- Repeater options: Min: 1, Default count: 4

Fields inside `stats` group:
| # | Type | HubL Variable Name | Label       | Default Value |
|---|------|--------------------|-------------|---------------|
| 1 | Text | stat_number        | Stat Number | (e.g. `60+`)  |
| 2 | Text | stat_label         | Stat Label  | (e.g. `Active Clients`) |

Closing field:
| # | Type | HubL Variable Name | Default Value |
|---|------|--------------------|---------------|
| 4 | Text | footnote           | * 各事業及びパートナーを含む体制 |

## Default Stats Content:
- Item 1: `stat_number`: `60+`   | `stat_label`: `Active Clients`
- Item 2: `stat_number`: `200+`  | `stat_label`: `Clients Served`
- Item 3: `stat_number`: `20+`   | `stat_label`: `Professionals*` (or `Professionals＊`)
- Item 4: `stat_number`: `2013`  | `stat_label`: `Founded`

## Notes
- Numbers render in large 64px bold font; labels render in 16px font with an individual 1px `#dce5e7` hairline separator below each item.
- Module label in HubSpot: "Swimmy Key Facts"
- Section settings in page editor: Padding `0px`, Full width.
