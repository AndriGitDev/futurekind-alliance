## 2025-01-24 - [Robust Navigation Active States]
**Learning:** Route normalization (handling trailing slashes) is essential for reliable navigation active states. Without it, `aria-current` and visual indicators may fail depending on how the server or SSG handles URLs.
**Action:** Use a normalization helper (like `.replace(/\/$/, '') || '/'`) when comparing `Astro.url.pathname` with link `href` values.
