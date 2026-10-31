# AGENTS.md

- Static site with no build step. Everything lives in `public/index.html` (inline CSS + JS).
- `netlify.toml` publishes `public/`.
- The Telegram invite URL appears twice: the button `href` and `targetUrl` in the script. Keep both in sync.
- The Meta Pixel ID is set in the `<head>` snippet and in the `<noscript>` fallback. `fbq('track', 'Lead')` fires before every redirect, whether from the button or the countdown.
- Keep the page dependency-free and fast. It's an ad landing page.
