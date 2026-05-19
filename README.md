# Highlands Fellowship Brand

This repository is the single source of truth for Highlands Fellowship's brand assets and guidelines. It is designed to be consumed by agents and automation tools to produce consistently branded work.

## Repository Structure

| Path | Description |
|---|---|
| `brand-kit.json` | Machine-readable brand data — colors, typography, logos, voice, and rules |
| `brand-guidelines.md` | Human and agent-readable guidelines — tone, logo usage, writing conventions, and color rules |
| `index.html` | Visual reference page for all brand assets |
| `logos/` | Logo lockups — H mark, wordmark, combination mark, and avatar |
| `assets/` | Supporting brand assets — embellishments, image treatments |
| `fonts/` | Font files (if self-hosted) |
| `guidelines/` | Official brand guidelines PDF |
| `samples/` | Sample files and usage examples |

## brand-kit.json Structure

```json
{
  "version": "2025.01",
  "base_url": "https://branding.hf.church",

  "brand": {
    // Name, short name, tagline, website
  },

  "locations": [
    // Primary location: Abingdon, VA
  ],

  "color_system": {
    "palette": {
      "primary":      // Navy Blue (#0d1d41) — main brand color, 3 tones, RGB, text_on
      "secondary":    // Teal (#56b6b2) — accents, icon fills, logo backgrounds, 3 tones
      "accent":       // Yellow (#f4b334) — accent text and callouts, used sparingly
      "orange":       // Orange (#da5e14) — extended palette, campaign graphics
      "olive":        // Olive (#77843c) — extended palette, campaign graphics
      "cream":        // Cream (#f2dab2) — warm text on dark backgrounds
      "light_green":  // Light Green (#aac27f) — extended palette, seasonal graphics
      "bright_orange":// Bright Orange (#f58c29) — extended palette, events & CTAs
      "sunset_red":   // HFS Sunset Red (#e74e40) — extended palette, high-impact series
      "neutral":   // Dark Gray (#3d3d3d) — body copy color
    },
    "gradients": {
      "vision": // Teal → Yellow gradient for campaign/sermon series contexts
    },
    "interface": {
      // Neutral scale: white → off-white → light gray → mid gray → dark gray → near black
    }
  },

  "typography": {
    "primary": // Roboto Slab Medium — sole authorized typeface, Google Fonts
               // Heading large: 30pt | Heading body: 18pt | Body: 12pt / 16pt leading
  },

  "radius": {
    // none (0px), sm (4px), md (8px), lg (16px), full (9999px)
    // Each has a value and usage description
  },

  "logos": {
    "lockups": [
      // logo_mark        — circular H monogram (primary, compact contexts)
      // wordmark         — script "Highlands Fellowship" (secondary, full-name contexts)
      // combination_mark — H mark + wordmark together
      // avatar           — H mark for org profiles and directories
      // Each lockup contains an assets[] array with SVG and PNG variants at 256/512/1024
    ],
    "rules": [
      // Logo usage rules for agents and designers
    ]
  },

  "voice": {
    // summary, tone descriptors, writing conventions, words to avoid, example phrases
  },

  "brand_elements": {
    "image_treatment": // Navy blue photo overlay spec for branded backgrounds
    "vision_gradient":  // Teal-to-yellow gradient specification
  },

  "rules": [
    // Top-level agent directives for using this brand kit
  ]
}
```

## Asset Conventions

**Variants:** Every asset entry includes a `variant` field — `light`, `dark`, `teal-bg`, `navy-bg`, `transparent`, or a descriptive label.

**Sizes:** PNG assets are provided at 256, 512, and 1024 px.

**File paths:** All paths are relative to the repository root and match the physical directory structure.

**Hosted URLs:** All logo assets are hosted on Cloudinary at `https://res.cloudinary.com/hfchurch/image/upload/Brand%20Guide%20Logos/`. Each asset entry in `brand-kit.json` includes both a `file` (local path) and a `url` (Cloudinary CDN URL). Use the `url` field for all remote delivery. PNG variants are served via Cloudinary transformations (e.g. `w_256` for 256px wide).

**Logo usage:** Light (white) variants are for use on dark backgrounds (navy, teal, photo overlays). Dark (navy) variants are for use on white or light backgrounds. Prefer SVG for all vector and programmatic use.

## For Agents

When producing branded work for Highlands Fellowship, load `brand-kit.json` first. It is the authoritative source for all colors, typography, logo file paths, voice guidelines, and usage rules. Follow the `rules` array at the top level of the JSON for governing directives.

Key facts for quick reference:
- **Primary color:** Navy Blue `#0d1d41`
- **Secondary color:** Teal `#56b6b2`
- **Accent color:** Yellow `#f4b334` (text/callout use only — sparingly)
- **Extended palette:** Orange `#da5e14`, Olive `#77843c`, Cream `#f2dab2`, Light Green `#aac27f`, Bright Orange `#f58c29`, HFS Sunset Red `#e74e40` (campaign/series contexts)
- **Primary logo mark:** White H on teal background — `https://res.cloudinary.com/hfchurch/image/upload/Brand%20Guide%20Logos/hf-logo-mark-primary.svg`
- **Typeface:** Roboto Slab Medium (Google Fonts)
- **Tagline:** Know God. Find Community. Make a Difference.
- **Website:** https://hf.church
