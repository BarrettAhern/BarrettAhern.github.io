# Barrett Ahern Design System v1.1

One system. Paper neutrals and editorial type from barrettahern.com, a clean app-UI structure and patterns, British racing green as the single accent, and audit components for data and reports. It replaces the earlier three-palette version: there is no palette switch any more.

**Files**
- `tokens.css`: generated. One palette, light and dark. Never hand-edit; change `build_tokens.py` and regenerate.
- `components.css`: every component. Tokens only, no hex values.
- `index.html`: live gallery. Every component has copyable HTML. Add new patterns here first.
- `COMPONENT_REFERENCE.md`: class names, when to use, when to avoid, data shape.

## 1. Rules (non-negotiable)

1. **Tokens, never hex.** Components read CSS variables. Client work uses the same system; do not fork a second palette.
2. **One accent per view.** The accent marks the one thing the page argues from. Status uses the five status tones (success, warning, danger, attention, info), never the accent.
3. **Colour never carries meaning alone.** Every status has a word and a square marker. Every delta has an arrow and a stated comparison period.
4. **Every number has a client, a period and a source.** Label anything modelled or illustrative where it appears. Never invent figures.
5. **Reuse before you build.** If a component exists, copy it. A new pattern uses the same tokens, gets a gallery entry and a row in the component reference.
6. **Accessible by default.** Text 4.5:1 or better (validated in `build_tokens.py`), visible 2px focus ring, 44px touch targets on mobile, reduced motion honoured, one `h1` per page.
7. **Copy.** British spelling. No em dashes. Sentence case. Numbers in tabular figures (`.ds-num`).

## 2. Colour

Paper carries the page. British racing green is the accent. Cotswold stone is the quiet secondary. Theme follows the OS; force with `<html data-theme="light|dark">`.

| Role | Light | Dark | Used for |
|---|---|---|---|
| Page | `#FAFAF8` | `#1C1B19` | `--bg-base` |
| Card | `#FFFFFF` | `#242320` | `--bg-raised` |
| Ink | `#1C1B19` | `#F4F3EF` | text, primary buttons, verdict card |
| Accent (BRG) | `#0F4C3A` | `#62A390` | `--accent` fills, active bars, one hard number |
| Accent text | `#0F4C3A` | `#7FB8A4` | `--accent-text` links and figures |
| Accent on verdict | `#94C3B4` | `#0F4C3A` | `--accent-on-invert`, the uplift chip |
| Stone | `#736046` | `#C4B091` | `--accent-2`, stat trends and quiet emphasis only |

The accent is lighter in dark mode because racing green on near-black fails contrast. Use the tokens and it flips for you. Status colours are separate and fixed (see section 3).

Typography is DM Serif Display for display, DM Sans for text and numerals (tabular), DM Mono for labels, refs and code. Client audit work uses this same system.

## 3. Tokens (semantic names, same in light and dark)

- **Surfaces:** `--bg-base` page, `--bg-raised` cards and inputs, `--bg-sunken` wells and table heads, `--bg-overlay`, `--bg-invert` (verdict, tooltips, toasts) with `--text-on-invert`.
- **Text:** `--text-primary`, `--text-secondary`, `--text-muted` (meta only, still AA).
- **Lines and states:** `--border-subtle`, `--border-faint`, `--border-strong`, `--hover`, `--selected`, `--focus`.
- **Accent (racing green):** `--accent` (fills), `--accent-ink` (text on accent), `--accent-text` (accent as text on page surfaces), `--accent-on-invert` and `--accent-on-invert-ink` (accent on the dark verdict card), `--accent-2` (Cotswold stone, stats and trends only).
- **Action:** `--action-bg`, `--action-ink`. Primary buttons are ink, so the green stays singular.
- **Chart:** `--chart-ink`, `--chart-quiet`, `--chart-accent`. Quiet grey for everything, accent for the one bar that matters.
- **Status:** `--status-{success|warning|danger|attention|info}` plus `-tint`, `-ink`, `-text` (text flips light in dark mode).
- **Type:** `--font-display`, `--font-sans`, `--font-num`, `--font-mono`. Sizes `--text-2xs` 11 to `--text-4xl` 44.
- **Space (4px grid):** `--space-100` 4px, 200 8, 300 12, 400 16, 600 24, 800 32, 1200 48, 1600 64.
- **Shape:** `--radius-sm` 4, `--radius-md` 8, `--radius-lg` 12. Cards are flat with hairlines; only overlays use `--shadow-pop`.
- **Controls:** `--control-sm` 28, `--control-md` 36, `--control-lg` 44.
- **Motion:** `--ease` cubic-bezier(.16,1,.3,1), 120 / 200 / 360ms.

Compatibility aliases (`--color-bg`, `--color-ink`, `--color-rule` and so on) are included so the existing site stylesheet runs on these tokens unchanged.

## 4. Type scale

| Role | Class | Spec |
|---|---|---|
| Display | `.ds-h1` | display font, clamp 28 to 44, 1.15, -0.02em |
| Section title | `.ds-h2` | display font, clamp 22 to 32, max 30ch |
| Card title | `.ds-h3` | sans 600, 16 |
| Standfirst | `.ds-standfirst` | 16/24, secondary, max 68ch |
| Body | `.ds-body` | 14/20 |
| Eyebrow | `.ds-eyebrow` | mono 11, .14em, uppercase |
| Note | `.ds-note` | 12/16, secondary |
| Numbers | `.ds-num` | tabular lining figures, always |

## 5. Layout

- Content width 1160px (`.ds-wrap`), 720px for reading (`.ds-wrap--narrow`). Gutters 16px, 32px from 768px.
- Section band 48px vertical, 64px from 768px, hairline bottom rule (`.ds-band`).
- Grids: gap 12px, auto-fit (`.ds-g2` 320, `.ds-g3` 260, `.ds-g4` 210).
- App pages: breadcrumb, `.ds-page-header` with one primary action, then `.ds-layout` (main two thirds, secondary one third). Settings pages use `.ds-annotated`.
- Breakpoints: 600 (nav wraps), 768 (gutters, bands), 900 (two-column layouts).

## 6. Report spine (client audits)

Verdict, what's working, where the money leaks, journeys, technical foundations, options, roadmap, method. Drop sections, never reorder. Every finding has a ref ID, a severity badge and an evidence tier. Exports copy CSV to the clipboard (downloads fail in artifacts).

## 7. Building checklist

1. Start from the gallery HTML, not a blank file. 2. Load `tokens.css` then `components.css`. 3. Add `class="ds-root"` to `body`. 4. Check one accent per view, sources on every number, focus ring visible, 390px wide with no horizontal scroll, light and dark. 5. If you invented a pattern, add it to the gallery and the reference.

## 8. Things to watch

- **Success green sits close to racing green.** Status never relies on colour alone (word plus square marker), so the two stay distinguishable, but do not put a success badge directly beside an accent fill.
- **The accent is dark.** Racing green and ink are near neighbours in light mode, which is why primary buttons are ink and the accent is reserved for the one thing the page argues from.
- Secondary text is darker than the old site grey (`#787470` measured about 4.3:1) so every pair passes AA.
- `Design_System_Showcase.html` in the project is the earlier racing green exploration and is superseded by this system.
