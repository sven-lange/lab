# Color Change Map

This file lists where color settings are defined in this site so future updates are quick and safe.

## 1) Active Scheme Selection
- File: `config/_default/params.toml`
- Key: `colorScheme = "sven"`
- Purpose: chooses which scheme file Hugo loads.

## 2) Core Palette Tokens (Global)
- File: `assets/css/schemes/sven.css`
- Keys:
  - `--color-neutral` (base neutral tone)
  - `--color-neutral-800`, `--color-neutral-900` (dark surfaces)
  - `--color-primary-*` (link/highlight/accent ramp)
- Purpose: Tailwind utility classes like `bg-neutral`, `dark:bg-neutral-800`, `text-primary-*` use these tokens.

## 3) Global Mode Overrides
- File: `assets/css/custom.css`
- Important blocks:
  - `html:not(.dark) body` (light mode background/text hard overrides)
  - `html.dark body` (dark mode background/text hard overrides)
  - `html.dark .dark\:bg-neutral-*` and `html.dark .dark\:from-neutral-800` / `to-neutral-800`
- Purpose: forces exact mode colors where utility classes alone are not enough.

## 4) Landing/Homepage-Specific Colors
- File: `layouts/partials/home/background.html`
- Important classes/areas:
  - `home-landing-title` heading class (title color controlled in `assets/css/custom.css`)
  - intro/background layers using `bg-neutral`, `dark:bg-neutral-800`, gradient utilities.
- Purpose: homepage has extra layers that can diverge from site-wide body colors.

## 5) People Page Social Icon Chips (Email, Scholar, ORCID, etc.)
- Markup file: `layouts/partials/people/member-card.html`
  - class: `people-member-link`
- Color rules file: `assets/css/custom.css`
  - selectors: `.people-member-link`, `html.dark .people-member-link`
- Purpose: controls the small circular icon backgrounds in People cards.

## 6) Theme Email Chips (Article/Metadata Blocks)
- Markup source (theme): `themes/blowfish/layouts/_default/single.html`
  - class pattern: `email-link m-1 rounded ...`
- Local override file: `assets/css/custom.css`
  - selectors: `.email-link.m-1.rounded` (+ dark and hover variants)
- Purpose: updates legacy rounded email chip backgrounds without editing theme files.

## 7) Menus, Search Modal, and Other Theme Components
- Theme markup references:
  - `themes/blowfish/layouts/partials/header/components/mobile-menu.html`
  - `themes/blowfish/layouts/partials/search.html`
- These mostly use utility classes tied to neutral tokens and dark variants.
- If needed, override in `assets/css/custom.css` (preferred) rather than editing theme files.

## 8) Do Not Edit Generated Output
- Generated files in `public/` mirror the source after build.
- Always edit source files above, then rebuild:

```bash
hugo
```

## 9) Quick Update Workflow
1. Edit `assets/css/schemes/sven.css` tokens.
2. Update any hard overrides in `assets/css/custom.css`.
3. Rebuild with `hugo`.
4. Hard-refresh browser / clear cache if colors seem stale.
