# Agni Yoga World Community — Discourse Theme

A custom Discourse theme matching the aesthetic of [agniyogaworld.org](https://agniyogaworld.org):
deep indigo/navy backgrounds, warm gold accents, parchment content surfaces,
and elegant Cormorant Garamond serif typography.

---

## File structure

```
agni-yoga-discourse-theme/
├── about.json              ← Theme metadata
├── settings.yml            ← Theme settings (color references)
├── color_scheme.json       ← Discourse color scheme for import
├── common/
│   ├── common.scss         ← Main styles (all devices)
│   ├── head_tag.html       ← Font preconnect tags
│   ├── after_header.html   ← Sub-header tagline banner
│   └── footer.html         ← Custom footer
├── desktop/
│   └── desktop.scss        ← Desktop-only overrides
└── mobile/
    └── mobile.scss         ← Mobile-only overrides
```

---

## Installation options

### Option A — GitHub import (recommended)

1. Push this folder to a GitHub repository.
2. In your Discourse admin: **Customize → Themes → Install → From a git repository**.
3. Paste your repo URL and click Install.
4. Activate the theme for all users (or set as default).

### Option B — Manual upload via Admin panel

1. Go to **Admin → Customize → Themes → New**.
2. In the theme editor, paste the contents of each file into the corresponding section:
   - `common.scss` → **CSS** tab (Common)
   - `after_header.html` → **HTML** tab → *After Header*
   - `footer.html` → **HTML** tab → *Footer*
   - `head_tag.html` → **HTML** tab → *Head Tag*
   - `desktop.scss` → **CSS** tab (Desktop)
   - `mobile.scss` → **CSS** tab (Mobile)
3. Save the theme.

### Color scheme

To import the color scheme separately:
1. **Admin → Customize → Colors → New color scheme**.
2. Use the hex values from `color_scheme.json`:
   - **Primary** (text): `#1e1e3f`
   - **Secondary** (background): `#f5f0e8`
   - **Tertiary** (accent/links): `#c9a84c`
   - **Quaternary**: `#2b2d5e`
   - **Header background**: `#1a1b3a`
   - **Header primary** (header text/icons): `#e8d5a0`
   - **Highlight**: `#e8d5a0`

---

## Fonts used

- **Cormorant Garamond** — headings and topic titles (Google Fonts)
- **EB Garamond** — post body text (Google Fonts)
- **Inter** — UI chrome, labels, navigation (Google Fonts)

Loaded via `@import` in `common.scss`. No additional setup required.

---

## Customisation tips

- **Logo**: Upload your logo in **Admin → Customize → Site Settings → logo**. The header text title will still display if no logo is set.
- **Favicon**: Upload the Maitreya seal or site favicon in **Admin → Customize → Site Settings → favicon**.
- **Category colors**: Each category can have its own badge color. Deep indigo (`#2b2d5e`) works well as the default.
- **Background image** (optional): You can add a subtle Himalayan/starfield texture to `.d-header` by adding `background-image: url(...)` in the CSS.

---

## Notes

- Tested against Discourse v3.x.
- Designed for light mode. Dark mode support can be added by wrapping overrides in `@media (prefers-color-scheme: dark)`.
- The `after_header.html` tagline can be edited to match your forum's description.
