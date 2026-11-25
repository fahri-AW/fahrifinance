# AGENTS.md

## FinanceFlow engineering and product-design standards

These instructions apply to every planning, design, implementation, integration, review, and testing task in this repository. They are an active working contract, not optional inspiration.

### Required working modes

Apply all three standards together:

1. **Anti-Slop DURING**: maintain a distinctive, purposeful interface; avoid generic AI patterns; make every control real; verify the rendered result; and complete the mandatory PASS/FAIL Delivery Gate before handoff.
2. **Impeccable**: work as a design director for this product's actual user and task. FinanceFlow is an **Operate** surface: task completion, scanability, predictable interaction, data legibility, and restrained brand expression take priority over marketing theatrics.
3. **UI UX Pro Max**: establish a product-specific design system before creating or changing UI. Use relevant product, style, palette, typography, UX, accessibility, responsive, motion, chart, and stack guidance. Do not choose a style or component because it is fashionable.

### Project context

- Product: FinanceFlow, a financial bookkeeping and reporting application for small-business operators.
- Primary tasks: record sales, purchases, expenses, capital, withdrawals, cash movements, receivables, and payables; review journals, ledgers, trial balance, and financial statements.
- Existing stack: HTML, CSS, browser JavaScript, Node.js, Express, PostgreSQL, and Chart.js. Confirm the current repository before changing the stack.
- Preserve existing accounting rules, data contracts, API behavior, authentication, authorization, and working user flows unless the task explicitly requires a change.
- Treat financial data as high-integrity data. Never fabricate sample business metrics, balances, customer records, testimonials, or claims.

### Mandatory workflow

#### 1. Plan before coding
- Inspect the current implementation, routes, API contracts, database schema/migrations, tests, and existing design documentation.
- Identify the target users, their primary jobs, relevant constraints, and the measurable outcome of the requested change.
- Map affected screens, navigation, permissions, interaction states, loading/empty/error/success states, and responsive behavior.
- Record assumptions and risks. Ask only when a missing fact materially blocks safe implementation.
- Define the scope and regression risks. Do not rewrite unrelated working features.

#### 2. Design before implementation
- Read `DESIGN.md` and keep it as the visual source of truth unless the user approves a redesign.
- Define or update semantic design tokens before styling: color roles, typography scale, spacing, radii, borders, elevation, focus, and motion.
- Give each screen a clear focal point and hierarchy. Use whitespace structurally.
- Choose patterns based on the accounting task and data density. Do not default to generic hero sections, decorative bento grids, nested cards, gratuitous gradients, pill-shaped everything, or oversized icon tiles.
- Maintain WCAG 2.2 AA contrast targets: 4.5:1 for normal text and 3:1 for large text and meaningful UI graphics. Never rely on color alone to convey financial status.
- Design mobile as a different interaction context, not merely a shrunken desktop layout.

#### 3. Develop with restraint
- Keep existing APIs, IDs, selectors, data models, and accounting behavior stable unless change is necessary and documented.
- Use semantic HTML, accessible names, visible labels, keyboard-operable controls, visible focus, and correct ARIA only where native semantics are insufficient.
- Every visible button, link, menu, tab, input, filter, and dialog control must have a real, testable behavior.
- Provide validation, useful inline errors, loading feedback, empty states, success feedback, and recoverable failure behavior.
- Avoid dead controls, fake charts, invented data, hidden destructive actions, and success messages before persistence is confirmed.
- Respect `prefers-reduced-motion`. Motion must communicate state, not decorate the page.
- Keep secrets in environment variables. Validate and authorize all server-side operations. Protect financial writes and destructive actions.

#### 4. Integrate and preserve data integrity
- Trace important flows end-to-end: UI -> API -> validation -> authorization -> database -> response -> UI state.
- Verify create, read, update, delete, posting, reversal, and reporting behavior where affected.
- Use transactions for multi-step accounting writes. Preserve double-entry balance invariants and decimal-safe money calculations.
- Do not claim data is saved until the server/database confirms success.
- Add or update migrations and tests when schema or business rules change.

#### 5. Test and inspect
- Run the repository's actual test scripts and production build/start checks where available. Report exact commands and outcomes.
- Test affected user flows, including validation failures, empty data, server errors, loading, success, keyboard-only use, and destructive-action confirmation.
- Inspect responsive layouts at 320, 375, 768, 1024, and 1440 CSS pixels (or the nearest supported viewport).
- Inspect the rendered application at the sizes it ships at. Source inspection alone is not visual verification.
- Check browser console and network errors, chart readability, table overflow, long labels, zoom/reflow, and focus restoration.
- If browser automation or a live browser is unavailable, state that limitation. Do not pretend a click-through or visual inspection occurred.

### Design-system consistency

- `DESIGN.md` defines the product's visual direction and composition dials.
- Use semantic CSS variables/tokens. Avoid one-off hardcoded values when a token exists.
- Components must share consistent states: default, hover, focus-visible, active, disabled, loading, error, and success where applicable.
- Keep typography, spacing, radii, table density, form controls, status labels, and chart treatment consistent across screens.
- Update `DESIGN.md` when an approved design decision changes the system.
- Any new component must have a documented purpose and responsive behavior.

### Anti-Slop DURING delivery gate

Run this gate before every handoff. A failed item blocks delivery until fixed or explicitly reported as a known, accepted limitation. Never mark an untested item PASS.

#### A. Product truth and scope
- [ ] No fabricated financial values, customer details, statistics, testimonials, capabilities, or security claims.
- [ ] Existing working flows and accounting rules remain intact, or changes are explicitly documented and tested.
- [ ] Every navigation destination exists and every visible action has a real behavior.
- [ ] No unrelated feature or dependency was added without a reason.

#### B. Visual and responsive quality
- [ ] A clear design direction and rationale are documented.
- [ ] The interface is distinctive to FinanceFlow and appropriate for an accounting workspace.
- [ ] Design tokens and component states are consistent.
- [ ] No horizontal page overflow or clipped content at supported widths.
- [ ] Dense tables remain usable on mobile without breaking the whole page.
- [ ] Contrast meets WCAG AA for checked text and UI states.
- [ ] Keyboard focus, labels, semantics, zoom/reflow, and reduced motion are verified.

#### C. Functionality and reliability
- [ ] Every visible control has been exercised or has an explicitly documented test limitation.
- [ ] Forms validate on client and server as appropriate.
- [ ] Loading, empty, error, and success states are verified for affected flows.
- [ ] Financial writes persist correctly and preserve double-entry invariants.
- [ ] No console errors, unhandled promise rejections, or broken network requests in tested flows.
- [ ] Destructive operations require appropriate confirmation and authorization.

#### D. Evidence and release
- [ ] Automated tests were run; exact command and result are recorded.
- [ ] Production build/start or deployment check was run where available.
- [ ] Rendered UI was inspected at target desktop and mobile sizes, or the limitation is explicit.
- [ ] Deployment status is checked against the exact final commit.
- [ ] Every PASS includes concrete evidence. Unknown or untested items are NOT VERIFIED, never PASS.

### Required handoff format

1. Summary of changes and affected files.
2. Design/system decisions and why they fit the task.
3. Tests run with exact outcomes.
4. Deployment status tied to the final commit, if applicable.
5. Delivery Gate with PASS / FAIL / NOT VERIFIED for every relevant item.
6. Known limitations and next steps.

### Reference standards

- Anti-Slop: https://github.com/miqdadbadjuber/anti-slop
- Impeccable: https://github.com/pbakaus/impeccable
- UI UX Pro Max: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

Use the current upstream guidance when available. These references inform the process; do not claim their CLIs or agent plugins are installed unless installation and execution are verified.
