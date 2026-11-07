# Design system
Follow the Barrett Ahern Design System v1.2 (tokens.css, components.css, gallery in design-system/).
- One palette (paper + racing green). Link tokens.css then components.css. body class "ds-root".
- Use var(--token) only. No hex values in new CSS. Reuse .ds-* components; if you add one, add it to design-system/index.html and COMPONENT_REFERENCE.md.
- The legacy css/style.css maps onto the tokens through the compatibility aliases in tokens.css. When touching a page, migrate its classes to .ds-* rather than adding new legacy classes.
- Tables use .ds-table-wrap + .ds-table (sticky header and first column). Never ship an unstyled <table>.
- One accent per view, AA contrast, visible focus, 390px with no horizontal scroll, light and dark.
- British spelling. No em dashes. Plain HTML and CSS, no build step, GitHub Pages.

# Sitemap
Whenever an image is added, replaced or renamed, or a page is added, update sitemap.xml in the same change.
- Add or update the page's <url> entry, with lastmod set to the date of the change.
- List each image as an <image:image> entry under every indexable page where it appears. Check the file loads at that URL first.
- Leave out redirect stubs and noindex pages.
