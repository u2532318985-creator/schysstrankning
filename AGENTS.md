# AGENTS.md

## Architecture
Plain static site, no build step and no package.json. Netlify publishes `public/` (see `netlify.toml`).

- `public/index.html` – single landing page (Swedish). Sections are anchored: `#start`, `#sa-fungerar-det`, `#tjanster`, `#priser`, `#nfc`, `#faq`, `#kontakt`.
- `public/tack.html` – thank-you page, served extensionless at `/tack`.

## Conventions
- Styling uses the Tailwind Play CDN plus a few custom classes (`glass-card`, `gradient-text`, `hover-lift`, `grid-pattern`, `form-input`, `font-display`) defined in inline `<style>` blocks. Reuse them on new pages to match the look.
- All copy is Swedish; prices are stated exclusive of VAT.
- The site deliberately does not promise rankings or results – keep new copy consistent with the disclaimer in the pricing section.

## Forms
- The contact form `kontakt-schysst-rankning` uses Netlify Forms (`data-netlify="true"`, honeypot `bot-field`, hidden `subject`). Its `action` must stay extensionless (`/tack`, not `/tack.html`).
- Changing field names changes what Netlify stores; keep names stable (`foretag`, `namn`, `email`, `telefon`, `meddelande`).
- Form detection is enabled via the marker in `.netlify/features/netlify-forms`.
