# Schysst Rankning

Webbplats för Schysst Rankning – optimering och löpande hantering av Google Företagsprofil, lokal SEO, recensionshantering och NFC-recensionsnyckelringar för svenska företag.

## Teknik

- Statisk HTML (ingen byggprocess)
- Tailwind CSS via CDN, typsnitten Space Grotesk och Inter från Google Fonts
- Netlify Forms för kontaktformuläret (inklusive honeypot-skydd mot spam)

## Struktur

- `public/index.html` – startsidan med tjänster, process, priser, NFC, frågor och kontaktformulär
- `public/tack.html` – tacksidan som visas efter att formuläret skickats (`/tack`)
- `netlify.toml` – publicerar mappen `public`

## Köra lokalt

```bash
netlify dev --port 8889
```

Eller öppna `public/index.html` direkt i webbläsaren (formuläret fungerar då bara på Netlify).
