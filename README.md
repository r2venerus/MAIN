# Debt Capital Partners CRM

An onboarding & referral-relationship tracker for Baird Augustine's retail debt
providers, built from the **Retail Debt Partners** workbook. It tracks where each
lender sits in the referral-agreement process, the referral economics for each, and
carries **every column** from the source sheet.

## Open it

Open **`index.html`** in any browser — it's a single self-contained file (no build,
no server, no dependencies). Works offline.

## What's in it

- **Pipeline KPIs** — total partners and a breakdown by onboarding status
  (Signed · In Progress · Prospect · No Program).
- **Directory** — sortable, searchable table of all 30 partners with status, referral
  split, capital category, deal size, and relationship owner. Click any row to open a
  full profile drawer.
- **Referral economics view** — a focused table of the recorded agreement status, the
  **BA SF** referral split, and a link to each signed agreement.
- **Partner drawer** — every field from the workbook, grouped into *Referral economics*,
  *Capital & lending profile*, and *Relationship & contacts*, with clickable Drive links,
  emails, phones, and websites.
- Filter by status chips, by relationship owner, and free-text search across all fields.
- Light / dark theme.

## Columns carried from the source workbook

`Name` · `Referral Agreement Signed?` · `BA SF` (referral split) · `Capital Category` ·
`Product Types` · `Industries Served` · `Deal Size` · `Cost of Capital` ·
`Revenue Requirements` · `Required Documentation` · `Link to Google Drive for Marketing
Materials` · `Relationship Owner` · `Website` · `Contact Email` · `Contact Phone` ·
`Contact Name` · `Meeting Notes` · `Referral Agreement` (link).

The **Onboarding Status** column is derived from the recorded agreement text to drive the
pipeline (Signed / In Progress / Prospect / No Program).

## Data files

- `data/lenders.json` — structured records (source of truth for the app; the same data is
  embedded inline in `index.html`).
- `data/lenders.csv` — flat export for import into a spreadsheet or another CRM.

## Updating

Edit `data/lenders.json` (or the CSV), then re-embed it into `index.html`. The dataset is
inlined so the page stays self-contained; keeping `data/lenders.json` in sync gives you a
clean import path if you later move to a hosted CRM.

## Notes on data quality

Records were extracted from a PDF export of the workbook. A handful of cells in the source
(mostly long URLs and tightly-packed contact fields) overlapped in the PDF; those were
de-interleaved and, where the split was unambiguous, corrected by hand (e.g. splitting a
merged website / email / phone / name). Spot-check contact details against the original
before outreach. `JTSA`, `Raiseview`, and `Ondeck` are early, largely-empty prospect rows
carried over from the bottom of the sheet.
