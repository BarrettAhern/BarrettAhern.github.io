# Component reference

Class names are `ds-<component>`, variants `ds-<component>--<variant>`, parts `ds-<component>__<part>`. Open `index.html` for live demos and copyable HTML.

| Component | Classes | Use for | Avoid | Source |
|---|---|---|---|---|
| Button | `.ds-btn` `--primary` `--accent` `--plain` `--critical` `--sm` `--lg` `--icon`, `aria-busy`, `.ds-btn-group`, `.ds-cta` | One primary per view; secondary default; critical only destructive | Two accent buttons; icon-only without `aria-label` | Polaris |
| Form controls | `.ds-field` `.ds-label` `.ds-help` `.ds-error-text` `.ds-input` `.ds-select` `.ds-textarea` `.ds-check` `.ds-switch` `.ds-range` `.ds-search` | Label above, help below, error names the fix (`aria-invalid="true"`) | Placeholder as label | Polaris |
| Badge | `.ds-badge` `--success` `--warning` `--critical` `--attention` `--info` `--plain` | Status and severity. Word plus square marker | Green for non-success; accent as status | Polaris + Vervaunt |
| Evidence tier | `.ds-tier` `--f` `--a` `--c` | Strength of evidence: F fact, A analysed, B observed, C inferred | Tier without a source | Vervaunt |
| Banner | `.ds-banner` `--success` `--warning` `--critical` `--attention`, `__icon` `__title` `__body` | Page-level message; title states the point | More than one per view | Polaris |
| Toast | `.ds-toast[data-open]` | Confirm a completed action | Errors that need action (use a banner) | Polaris |
| Spinner, skeleton, progress | `.ds-spinner` `.ds-skeleton` `.ds-progress` | Loading and determinate progress | Spinner over a whole page | Polaris |
| Card | `.ds-card` `--flat` `--sunken` `--interactive`, `__head` `__foot` `__media` | One idea per card | Cards inside cards | Polaris + site |
| Callout (method) | `.ds-callout` | How a number was made, two sentences | Findings | Vervaunt |
| Empty state | `.ds-empty` | First-run and no-result states with one action | Decorative filler | Polaris |
| Page header, layout | `.ds-page-header` `.ds-layout` `.ds-annotated` `.ds-breadcrumbs` | Every app page | Skipping the breadcrumb on deep pages | Polaris |
| Navigation | `.ds-nav` `__logo` `__links` (`aria-current="page"`), `.ds-tabs` `.ds-tab[aria-selected]`, `.ds-pagination`, `.ds-disclosure` | Site nav, view switching, long lists, FAQs | Tabs that show the same point four ways | Site + Polaris |
| Data table | `.ds-table-wrap` (`--scroll` for fixed height) `.ds-table` (`.has-select` for a checkbox first column) `.is-num` `.is-wrap`, `th[aria-sort]`, `tr[aria-selected]`, `.ds-table-bar` (search, filters, bulk actions), `.ds-table-foot` (count, pagination) | Polaris index table: sticky header and sticky first column (checkbox and name both stick with `.has-select`), hairline rows, numbers right-aligned in tabular figures, units in the column name | Fewer than three columns; wrapping the first column; zebra stripes | Polaris |
| List, avatar, tags | `.ds-list` `.ds-avatar` `.ds-tags` `.ds-tag` | People, resources, skills | | Polaris + site |
| Verdict + chip | `.ds-verdict` `__claim`, `.ds-chip` `__val` `__cap` (uses `--accent-on-invert`) | Open every report; chip carries the only accent | Number without its basis; chip when lab and field diverge | Vervaunt |
| KPI | `.ds-kpi` `__lbl` `__val` `__sub`, `.ds-delta` `--up/down/flat`, `.ds-spark` | Four across in a hero | More than four; delta without a period | Vervaunt |
| Score dial | `.ds-dial` `--good` `--mid` `--poor` with `--v` 0 to 100 | Lab and composite scores; band named in text | Field metrics | Vervaunt |
| Hard number | `.ds-statline` `.ds-bignum` `--accent` | One finding as one number with source | Two per view | Vervaunt |
| Theme bars | `.ds-hbars` `.ds-hbar` `--hot` with `--v` | Survey themes, review topics | Pie charts | Vervaunt |
| Mix bar | `.ds-mix` `i.is-hot` `.ds-legend` | Share of revenue, max five segments | Six or more segments | Vervaunt |
| Dumbbell | `.ds-dumb` `__row` `__plot` with `--a` `--b` | Segment gaps, max seven rows | | Vervaunt |
| Quote | `.ds-quote` with `<cite>` | One verbatim line with source and date | Unsourced quotes | Vervaunt |
| Deadline | `.ds-deadline` `.ds-dot` | Dated, sourced deprecations | Dates you cannot source | Vervaunt |
| Findings table | `.ds-findings` (`details` rows) `__body`, `.ds-diff` | Technical backlog with ref IDs | Persona or CRO stories | Vervaunt |
| Options | `.ds-card` + `.ds-option--recommended` | Two or three routes with trade-offs | | Vervaunt |
| Steps | `.ds-steps` | Numbered process | | System |
| Hero, stat, service, publication, event, testimonial, footer | `.ds-hero` `.ds-stat` `.ds-service` `.ds-pub` `.ds-event` `.ds-testimonial` `.ds-footer` | barrettahern.com pages | In dense app screens | Site |
| Modal, tooltip | `.ds-modal` (native `<dialog>`), `.ds-tooltip[data-tip]` | Confirm irreversible actions | Forms with more than five fields | Polaris |

## Not yet built (add to the gallery first, then here)

Tabbed analysis chart, annotated screenshot walkthrough, sticky-viewport journey step, value model as a reusable function. The gallery shows a static value model; the full versions live in the Vervaunt Audit Specimen and should be copied from it, not rebuilt.

## Adding a component

1. Build from tokens only. 2. Add a gallery block (title, use, avoid, demo). 3. Add a row here. 4. Check light and dark, and 390px wide. 5. Flag it so the inventory is updated.
