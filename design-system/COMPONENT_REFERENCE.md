# Component reference

Class names are `ds-<component>`, variants `ds-<component>--<variant>`, parts `ds-<component>__<part>`. Open `index.html` for live demos and copyable HTML.

| Component | Classes | Use for | Avoid |
|---|---|---|---|
| Button | `.ds-btn` `--primary` `--accent` `--plain` `--critical` `--sm` `--lg` `--icon`, `aria-busy`, `.ds-btn-group`, `.ds-cta` | One primary per view; secondary default; critical only destructive | Two accent buttons; icon-only without `aria-label` |
| Form controls | `.ds-field` `.ds-label` `.ds-help` `.ds-error-text` `.ds-input` `.ds-select` `.ds-textarea` `.ds-check` `.ds-switch` `.ds-range` `.ds-search` | Label above, help below, error names the fix (`aria-invalid="true"`) | Placeholder as label |
| Badge | `.ds-badge` `--success` `--warning` `--critical` `--attention` `--info` `--plain` | Status and severity. Word plus square marker | Green for non-success; accent as status |
| Evidence tier | `.ds-tier` `--f` `--a` `--c` | Strength of evidence: F fact, A analysed, B observed, C inferred | Tier without a source |
| Banner | `.ds-banner` `--success` `--warning` `--critical` `--attention`, `__icon` `__title` `__body` | Page-level message; title states the point | More than one per view |
| Toast | `.ds-toast[data-open]` | Confirm a completed action | Errors that need action (use a banner) |
| Spinner, skeleton, progress | `.ds-spinner` `.ds-skeleton` `.ds-progress` | Loading and determinate progress | Spinner over a whole page |
| Card | `.ds-card` `--flat` `--sunken` `--interactive`, `__head` `__foot` `__media` | One idea per card | Cards inside cards |
| Callout (method) | `.ds-callout` | How a number was made, two sentences | Findings |
| Empty state | `.ds-empty` | First-run and no-result states with one action | Decorative filler |
| Page header, layout | `.ds-page-header` `.ds-layout` `.ds-annotated` `.ds-breadcrumbs` | Every app page | Skipping the breadcrumb on deep pages |
| Navigation | `.ds-nav` `__logo` `__links` (`aria-current="page"`), `.ds-tabs` `.ds-tab[aria-selected]`, `.ds-pagination`, `.ds-disclosure` | Site nav, view switching, long lists, FAQs | Tabs that show the same point four ways |
| Data table | `.ds-table-wrap` (`--scroll` for fixed height) `.ds-table` (`.has-select` for a checkbox first column) `.is-num` `.is-wrap`, `th[aria-sort]`, `tr[aria-selected]`, `.ds-table-bar` (search, filters, bulk actions), `.ds-table-foot` (count, pagination) | Index table: sticky header and sticky first column (checkbox and name both stick with `.has-select`), hairline rows, numbers right-aligned in tabular figures, units in the column name | Fewer than three columns; wrapping the first column; zebra stripes |
| List, avatar, tags | `.ds-list` `.ds-avatar` `.ds-tags` `.ds-tag` | People, resources, skills | |
| Verdict + chip | `.ds-verdict` `__claim`, `.ds-chip` `__val` `__cap` (uses `--accent-on-invert`) | Open every report; chip carries the only accent | Number without its basis; chip when lab and field diverge |
| KPI | `.ds-kpi` `__lbl` `__val` `__sub`, `.ds-delta` `--up/down/flat`, `.ds-spark` | Four across in a hero | More than four; delta without a period |
| Score dial | `.ds-dial` `--good` `--mid` `--poor` with `--v` 0 to 100 | Lab and composite scores; band named in text | Field metrics |
| Hard number | `.ds-statline` `.ds-bignum` `--accent` | One finding as one number with source | Two per view |
| Theme bars | `.ds-hbars` `.ds-hbar` `--hot` with `--v` | Survey themes, review topics | Pie charts |
| Mix bar | `.ds-mix` `i.is-hot` `.ds-legend` | Share of revenue, max five segments | Six or more segments |
| Dumbbell | `.ds-dumb` `__row` `__plot` with `--a` `--b` | Segment gaps, max seven rows | |
| Quote | `.ds-quote` with `<cite>` | One verbatim line with source and date | Unsourced quotes |
| Deadline | `.ds-deadline` `.ds-dot` | Dated, sourced deprecations | Dates you cannot source |
| Findings table | `.ds-findings` (`details` rows) `__body`, `.ds-diff` | Technical backlog with ref IDs | Persona or CRO stories |
| Options | `.ds-card` + `.ds-option--recommended` | Two or three routes with trade-offs | |
| Steps | `.ds-steps` | Numbered process | |
| Hero, stat, service, publication, event, testimonial, footer | `.ds-hero` `.ds-stat` `.ds-service` `.ds-pub` `.ds-event` `.ds-testimonial` `.ds-footer` | barrettahern.com pages | In dense app screens |
| Modal, tooltip | `.ds-modal` (native `<dialog>`), `.ds-tooltip[data-tip]` | Confirm irreversible actions | Forms with more than five fields |
| Person marker | `.ds-person[data-person][data-initial]`, tokens `--person-*` | Who an item belongs to: initial plus name | Person colour for state |
| Agenda row | `.ds-agenda > li[data-person][data-state]` `__time` `__title` `__meta` | Any timed list: calendar, rota, schedule. Owner bar, state badge | State by colour alone |
| Task row | `.ds-task[data-state=done]` `__title` `__meta`, `.ds-domain` | A task with a 44px tick target, priority and state as words, area as emoji plus text name | Marking Done from email or calendar evidence alone |
| Source and freshness | `.ds-source[data-state]` | Every panel header: source, time and state in words | Hiding a failure; a failed panel keeps its last copy and says so |
| Scope chip | `.ds-scope[data-scope]` | Top of any screen others can see | Using the chip as the safety control; shared views must not load private data |
| Next action | `.ds-next` `__claim` | One recommendation, one action, with its source | The verdict card outside reports |
| Wall mode | `.ds-wall` `__title` `__row` `__time`, tokens `--text-wall-*` | Read-only 10-foot screens such as the Echo Show | Buttons, private items, relying on the browser staying open |
| Density, three-panel layout | `[data-density=compact]`, `.ds-layout--3` | Tighter rows on a container; three equal panels from 900px | Compact density on touch screens |

## Not yet built (add to the gallery first, then here)

Tabbed analysis chart, annotated screenshot walkthrough, sticky-viewport journey step, value model as a reusable function. The gallery shows a static value model; the full versions live in the audit specimen and should be copied from it, not rebuilt.

## Adding a component

1. Build from tokens only. 2. Add a gallery block (title, use, avoid, demo). 3. Add a row here. 4. Check light and dark, and 390px wide. 5. Flag it so the inventory is updated.
