# CONTINUITY.md

## PLAN
- Fix social sharing meta tags: add logo image + clean up og/twitter metadata. (In progress)

## DECISIONS
- Use Hugo-native `images` site param instead of Blowfish `defaultSocialImage`: theme resolves that via `resources.Get` (assets/ only) while logo lives in static/. [CODE] 2026-07-31
- Disabled (commented) the dead `defaultSocialImage` line rather than deleting it. [TOOL] 2026-07-31
- Site-wide description fallback set in `languages.en.toml [params]` = "Lange Lab: Mechanisms of Ubiquitin-Mediated Transport" (same wording as homepage). [ASSUMPTION] 2026-07-31

## PROGRESS
- Added `images = ["/img/banner_dark.png"]` to params.toml. Build verified: og:image + twitter:image render with absURL on all pages; twitter:card upgraded to summary_large_image. [TOOL] 2026-07-31
- Verified public/img/banner_dark.png published; no duplicate meta tags. [TOOL] 2026-07-31
- Social image switched from thumbnail_logo_w.png to new banner_dark.png (1500x500) per user. [USER] 2026-07-31

## DISCOVERIES
- Blowfish head.html (lines 73-86) only emits defaultSocialImage for files it can resolve via resources.Get — static/ files are silently skipped. [CODE] 2026-07-31
- og:title on homepage = page title from content/_index.md ("Mechanisms of Ubiquitin-Mediated Transport"), which is also the visible homepage heading; <title> tag is site title "LANGE LAB". Changing it changes the visible heading too. [CODE] 2026-07-31

## OUTCOMES
- Pending user decision on og:title wording for socials (LANGE LAB vs research tagline). [USER] 2026-07-31
