# Global Health Engineering brand

Draft of 16 November 2026. Published so that the group's websites can copy it from a tagged release; not yet agreed with the group.

One file defines the visual identity of Global Health Engineering at ETH Zurich: colours, typography and logo. Tools that understand brand.yml (Quarto, bslib, Shiny, the brand.yml R package) read it directly. The structure follows [openwashdata/brand](https://github.com/openwashdata/brand).

## What is here

- `_brand.yml`: the brand definition, the single source of truth
- `ghe-colour-palette.pdf`: the GHE Colour Palette the colours are taken from
- `logos/`: logo, square logo and icon as SVG, the logo as PNG, the icon in white (from the corporate design folder of the group drive)
- `index.qmd` and `_quarto.yml`: the guide, rendered into `docs/`

## The palette in short

| Token | Value | Role |
|---|---|---|
| ghe-yellow, ghe-orange, ghe-purple, ghe-indigo, ghe-blue, ghe-teal, ghe-green | `#FBE215`, `#ED6D37`, `#901C6C`, `#3C2874`, `#2C76B5`, `#1E8B99`, `#339167` | primary colour range |
| ghe-amber, ghe-red, ghe-violet, ghe-periwinkle, ghe-sky, ghe-pine, ghe-lime | `#EAA238`, `#C63432`, `#602684`, `#5A5BA5`, `#18A5C5`, `#1C7A6F`, `#A6CE8F` | secondary colour range |
| ghe-indigo | `#3C2874` | primary role in the draft: navbar, headings, links |
| ghe-indigo-dark, ghe-indigo-light, ghe-indigo-tint | see file | new: dark backgrounds, primary on dark, light tint for code |
| ghe-gray, ghe-gray-light | `#5c5751`, `#d9d6d2` | new: muted text, rules |
| ink, paper, white | `#1e1e1e`, `#f4f4f4`, `#ffffff` | text and surfaces |
| chart-1 to chart-6 | see file | categorical series: indigo, orange, teal, periwinkle, purple, red |

Yellow, orange, amber, sky and lime are below 3:1 on a light background and are for fills and large type only.

Typography is Atkinson Hyperlegible Next (Google Fonts) with Source Code Pro for code, the same as openwashdata.

## How to use it

- **Quarto:** copy `_brand.yml` and `logos/` into the project root; Quarto discovers the file.
- **Shiny and other bslib apps:** `bslib::bs_theme(brand = "_brand.yml")`.
- **Charts in R:** read the YAML with `yaml::read_yaml()` and take the colours from `color$palette`, `chart-1` to `chart-6` in that order.

## Render the guide

```sh
quarto render
```

## Where it is used

- [ghe-open.ch](https://ghe-open.ch), the open science website of the group, holds a copy in `_brand/` ([source](https://github.com/Global-Health-Engineering/website)).

## Licence

The brand definition (`_brand.yml`: colours, typography and the logo references) and the guide are licensed under [CC BY 4.0](LICENSE). Copy and adapt them with attribution to Global Health Engineering, ETH Zurich.

The logos identify Global Health Engineering and ETH Zurich. CC BY 4.0 does not license trademark rights (section 2(b)(2)). The logo files are here so that material of the group renders with the correct marks; any other use of the logos needs permission from the group.

## Open

- Which colour leads (indigo in the draft; the website uses a blue outside the palette)
- Review by the group
- Dark mode file
- A published guide (the rendered guide is in `docs/`)
