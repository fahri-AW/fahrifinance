# FinanceFlow Design Direction

## Product identity
FinanceFlow is a focused bookkeeping workspace for small businesses. It should feel dependable, precise, and calm. The interface supports daily financial work, not product marketing.

## Audience and primary task
Operators record sales, purchases, expenses, capital, withdrawals, cash movements, receivables, and payables. They review journals, ledgers, trial balance, and financial statements. The most frequent action is recording a transaction and checking its accounting effect.

## Visual concept: Ledger Studio
A contemporary accounting ledger with a warm paper-like workspace and deep botanical-teal navigation. The visual identity uses restrained contrast, compact information hierarchy, fine rules, and clear financial typography. It avoids decorative gradients, glowing panels, oversized icons, and excessive card nesting.

## Design tokens
- Canvas: soft mineral grey-green (#f3f4ef).
- Surface: warm near-white (#fffefa).
- Navigation: deep evergreen charcoal (#172c2b).
- Primary action: muted ledger teal (#245b57).
- Primary text: dark green-grey (#202d2b).
- Secondary text: muted grey-green (#66736f).
- Border: quiet grey-green (#dce2dc).
- Positive: accessible green (#267653), paired with labels.
- Negative: muted red (#b84f49), paired with labels.
- Warning: amber-brown (#9b6b24), paired with labels.
- Typography: Plus Jakarta Sans with system fallbacks.
- Radii: 7px small, 11px medium, 15px large.
- Elevation: subtle borders and low, diffuse shadows. Avoid floating-card excess.

## Layout
- Desktop: fixed grouped navigation, wide content canvas, clear page title, financial summaries, transaction composer, analytics, and ledger tables.
- Tablet: compact navigation and adaptive columns.
- Mobile: sticky horizontal navigation, stacked page header, two-column metrics where readable, single-column forms, and contained horizontal scrolling for dense tables.
- Print: hide navigation and controls; show selected report with a clear business header and A4-friendly tables.

## Interaction principles
- Transaction entry remains the primary workflow.
- Every control has visible hover, focus-visible, active, and disabled states.
- Use visible form labels, clear validation, and recoverable errors.
- Confirm posting and destructive operations.
- Provide loading, empty, error, and success feedback.
- Never use color alone to communicate financial status.
- Respect keyboard navigation, zoom/reflow, and prefers-reduced-motion.

## Composition dials
- ENERGY: 2/5. Calm and trustworthy.
- RHYTHM: 3/5. Distinct sections with compact accounting density.
- MOTION: 1/5. Only brief feedback transitions.

## Rationale
The evergreen navigation establishes a stable application frame. Warm neutral surfaces reduce visual glare. Teal identifies primary actions without competing with positive and negative accounting states. Fine table rules and tabular number alignment support accurate scanning. Mobile navigation remains thumb-scrollable while dense records scroll inside their own containers.
