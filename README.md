# Noted website

Static GitHub Pages website. No Node dependencies or build step required.

## Preview in VS Code

Open this folder and use Live Server on `index.html`, or run:

```sh
python3 -m http.server 8080 --directory .
```

Then open http://localhost:8080 . Page navigation uses relative URLs, so the site also works under a GitHub project path.

## Publish

Only publish the contents of **Website**, not the app, backend, backups or workspace.

1. Create a public GitHub repository for this site (for example `noted-website`).
2. Upload the files and directories in this folder to its root, including `.nojekyll`.
3. Repository Settings → Pages → Deploy from a branch → main → `/ (root)` → Save.
4. After GitHub confirms deployment, use the actual Pages URL. Do not guess the final URL.
5. Set the app's `NotedWebsiteURL` to that verified URL in both build configurations. Current app page paths: `privacypolicy`, `aboutnoted`, `terms`; site also has `privacy` and `support`.

Connected GitHub profile was `bshoaib1`; no repositories were exposed by the connector during creation. No repository was created or deployed by this local build.

## Before public launch

- Confirm the legal operator name/contact details and review the privacy/terms against final app behavior, providers, retention and applicable law. Current copy is a project-specific draft, not a claim of legal compliance.
- Verify final AI allowances/backend enforcement, subscription prices, intro eligibility, cancellation and receipt validation.
- Replace the coming-soon CTA with the actual App Store URL after approval. Do not use a fake download badge or Say's app link.
- Add absolute canonical, og:url and og:image metadata and sitemap.xml using the verified Pages URL. Current relative assets work for local previews; social scrapers require final absolute URLs.
- Hero uses the screenshot supplied by the owner on 29 October 2026 (`assets/noted-home.png`). Review visible name and balances before public publication. Other chart examples remain explicitly illustrative.
- No marketing analytics or tracking cookies are included. Update the privacy policy before adding them.
- Confirm app-notification automation compatibility on physical device; site copy intentionally does not promise universal capture.
- The website now includes full English and Arabic pages; Arabic pages use RTL layouts and translated metadata, forms, illustrations and legal copy.

Reference review: sayapp.net, /privacy and /terms, 29 October 2026. Only high-level content structure informed this original Noted site. No Say copy, screenshots, testimonials or user counts were copied.

## BeeWorks Studio and contact form — 29 October 2026

BeeWorks Studio is the independent developer brand behind Noted, not described as a registered corporation. The supplied original studio logo is in `assets/beeworks-studio.png` and appears in the footer and About page.

Mobile QA: checked Home at 320, 375, 390, 430, 768 and 1280 CSS pixels after overflow fixes; page width matched viewport at every size. Support, About, Privacy and Terms were also checked at 320/390/430/768/1280 widths without horizontal overflow. At 390px, contact inputs use 16px text, 52px height and a single-column layout. Empty submit stays local and focuses the required name field. Actual message delivery was not exercised; activation remains pending.

## Visual refinement — 29 October 2026

Replaced website gold accents with slate/amethyst and cool neutral lighting. BeeWorks Studio’s supplied logo retains its original brand colors. Feature tiles now use crisp inline 24px vector icons styled like the native app; the privacy figure is a code-native shield/lock and protected-record illustration. Heading: “Record it. Then carry on.”

Voice illustration: `assets/noted-voice-wave.png`, edited using the built-in image-generation tool from the owner’s supplied waveform, then resized for mobile delivery. Original source is unchanged. Generation prompt: “Edit this supplied audio wave image for the Noted fintech website. Preserve the broad horizontal composition and fine flowing layered wire-mesh sound-wave geometry, but recolor every wave exclusively in restrained Noted slate navy #0F172A, slate blue #516686 and amethyst #7954AA with soft pale lavender #B8A4D8 highlights. Premium, elegant, fine detailed mesh. Remove ALL lettering and the AUDIO text at the bottom; no words, no logos, no symbols. Keep background genuinely transparent. Put the waveform in a close-fitting wide landscape canvas around 2.8:1 with modest breathing space, avoiding huge blank areas above or below. No orange, red, gold, hot pink or cyan. A beautiful clean isolated website illustration, not a UI mockup. Export transparent PNG.”

Feature-card illustrations now use original inline SVG: bank SMS on a phone → Noted record, and manual expense-entry form with stylus/save control. Matched neutral stages and slate/amethyst vectors; checked on a 390px phone layout with no horizontal overflow.

## Arabic and RTL

Arabic routes are under `ar/`, including `ar/privacy/`, `ar/terms/`, `ar/support/` and `ar/aboutnoted/`. The English/العربية control switches to the matching page, without resetting to Home. All shared assets remain under `assets/`. The supplied Home screenshot is intentionally unchanged; Arabic illustration labels and surrounding copy are translated. Brand/provider names and ISO currency codes remain in their original forms.

`python3 tools/localize.py` rebuilds static Arabic pages and counterpart links from English pages and the translation mappings in that script. Update translations there when changing English content; `tools/arabic-copy.json` is an exported reference. Interactive tabs, RTL arrow-key navigation and form statuses are localized in `assets/site.js`. No language tracking cookie or automatic redirect is used.

## Current contact behavior

The contact form in both languages prepares a `mailto:` draft addressed to **beeworks.apps@gmail.com**, including the entered name, reply email, subject and message. The user reviews and taps Send in their own email application. The website makes no network submission, does not store the form contents, and never displays a false delivery confirmation. No form-provider account or activation is needed. An installed/configured email handler is required; the direct support address remains visible as a fallback.

Only files local to this folder have been updated; publish the revised files to GitHub Pages to replace the old endpoint on the live site.
