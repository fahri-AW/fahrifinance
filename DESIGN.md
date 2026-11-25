# FinanceFlow Design Direction

## Product identity
FinanceFlow is a practical financial workspace for small businesses and operators. The interface should feel dependable, legible, and focused on accurate bookkeeping rather than promotional SaaS marketing.

## Audience and primary task
The primary audience records daily sales, purchases, operating expenses, cash movements, receivables, and payables. The most frequent action is entering a transaction and checking its accounting effect.

## Visual language
- Preserve the existing FinanceFlow name and compact F mark.
- Use the established navy and blue identity from the existing application.
- Main canvas: warm, low-glare neutral.
- Primary surface: white.
- Main text: deep blue-grey.
- Primary action: restrained cobalt blue.
- Income and balanced states: green with text labels.
- Expense and error states: muted red with text labels.
- Warning states: amber with text labels.
- Avoid decorative gradients, ambient glows, excessive shadows, and gratuitous animation.

## Typography
Use Plus Jakarta Sans when available, with system sans-serif fallbacks. Headings use compact, confident weights. Tables and metadata prioritize legibility over density.

## Layout
- Desktop: fixed grouped navigation, flexible workspace, financial summaries, transaction composer, charts, and ledger tables.
- Tablet: narrower navigation and fewer columns.
- Mobile: horizontal, thumb-scrollable primary navigation; stacked page header; two-column metric summary where it remains legible; single-column forms; contained horizontal scrolling for dense accounting tables.
- Print: remove navigation and interactive controls; show the selected report with a clear business header and A4-friendly tables.

## Interaction principles
- Transaction input is the primary workflow and must be easy to find.
- Every action has a visible hover, focus, active, and disabled state.
- Forms use visible labels and explicit validation.
- Confirm before posting or destructive changes.
- Data views provide useful empty, loading, and error states.
- Respect reduced-motion preferences and keyboard navigation.

## Composition dials
- ENERGY: 2/5. Calm and purposeful, with enough contrast to make important actions visible.
- RHYTHM: 3/5. Distinguish the transaction composer, financial summary, analytics, and detailed ledgers through spacing and layout.
- MOTION: 1/5. Motion is limited to short feedback transitions; no looping or decorative movement.

## Purpose notes
- Navy navigation separates the application structure from report content.
- Cobalt is reserved for the primary action and selected navigation.
- Green and red communicate financial direction, always paired with text.
- Dense accounting tables stay in their own scroll containers on narrow screens to protect the page layout.
- The highlighted profit metric is visually distinct because it summarizes a key business outcome.
