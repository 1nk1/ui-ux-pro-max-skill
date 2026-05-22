# UI/UX Domain Search

Search the ui-ux-pro-max database for design guidance.

## Usage

```
/project:ui-search <query> --domain <domain>
```

## Available Domains

| Domain | Use For |
|--------|---------|
| `product` | Product type patterns (SaaS, e-commerce, fintech, healthcare) |
| `style` | UI styles (glassmorphism, minimalism, brutalism, neumorphism) |
| `color` | Color palettes by product/industry |
| `typography` | Font pairings and Google Fonts |
| `landing` | Page structure, hero patterns, CTA strategies |
| `chart` | Chart types and data visualization |
| `ux` | Best practices, accessibility, animation rules |
| `google-fonts` | Individual Google Fonts lookup |
| `react` | React/Next.js performance guidelines |
| `web` | App interface guidelines (iOS/Android/RN) |
| `prompt` | AI prompts and CSS keywords for styles |

## Instructions

Parse `$ARGUMENTS` to extract query and `--domain` flag, then run:

```bash
python3 src/ui-ux-pro-max/scripts/search.py "<query>" --domain <domain> -n 5
```

If no `--domain` is specified, run without it (auto-detection):

```bash
python3 src/ui-ux-pro-max/scripts/search.py "<query>"
```

Present results with practical implementation recommendations.
