# swimmy-hero — Fields Reference
# HubSpot Design Manager → Module fields
# NOTE: "body" is a reserved name in HubSpot — use "intro_text" instead.

| #  | Type       | HubL Variable Name | Default Value                                      |
|----|------------|--------------------|----------------------------------------------------|
| 1  | Text       | eyebrow            | DIFFERENT STRENGTHS, WORKING TOGETHER              |
| 2  | Text       | heading_line1      | あなたひとりで、                                    |
| 3  | Text       | heading_line2      | やらなくていい。                                    |
| 4  | Text       | subheading         | Different Strengths, Working Together              |
| 5  | Rich text  | intro_text         | (see paragraphs below)                             |
| 6  | Text       | button_1_text      | View Our Stories ↗                                 |
| 7  | Link       | button_1_link      | (leave blank, fill when pages are ready)           |
| 8  | Text       | button_2_text      | Contact Us ↗                                       |
| 9  | Link       | button_2_link      | (leave blank, fill when pages are ready)           |
| 10 | Text       | scroll_text        | Scroll to explore real stories of working together ↓ |
| 11 | Image      | bg_image           | (leave blank, upload raw ship photo)               |

## intro_text default content (Rich text field — paste as plain text then format)

Paragraph 1 (Normal):
国や分野を越え、それぞれの強みを持つ人が集まる。Swimmyは、事業の構想から日々の実務、新たな事業への参画まで、必要な形でパートナーとともに動きます。

Paragraph 2 (Normal):
ひとりでは進められないことも、異なる経験や専門性が重なることで、前に進めることがある。私たちは、そのための仲間でありたいと考えています。

## Notes
- bg_image: Export the RAW ship photo from Figma (layer "hero-photo") WITHOUT the curve applied.
  The border-bottom-left-radius curve is handled in CSS (border-bottom-left-radius: min(23.04vw, 331.8px)).
  Compress to <400KB using squoosh.app before uploading.
- The white gradient fade is also handled in CSS (::before pseudo-element) — do NOT bake it into the image.
- Module label in HubSpot: "Swimmy Hero"
