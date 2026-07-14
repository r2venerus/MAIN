# Lender Materials — Gap Analysis

**Source:** `data/lenders.json` (Retail Debt Partners workbook, 30 partners)
**Prepared:** July 14, 2026

This document inventories what is missing or unreliable in the lender materials so the
team can close the gaps before leaning on the CRM for referrals. Gaps fall into three
buckets: **missing records** (empty fields), **placeholder values** (a field is "filled"
but with a note like *Follow up* instead of real content), and **data-hygiene problems**
(content that is present but wrong, misfiled, or duplicated).

---

## Executive summary

- **Executed referral agreements are almost entirely missing from the file.** 15 partners
  are marked *Signed*, yet only **1 of 30** records carries a `Referral Agreement Link` —
  and that one is JTSA, a prospect that hasn't signed. **None of the 15 signed agreements
  has a copy on file.** This is the single largest gap and a compliance/collections risk:
  if a fee dispute arises, the split terms recorded in the sheet are unverifiable.
- **Three signed or near-signed partners have no recorded economics.** Slim Capital
  (signed, "sending over copy" — split blank), Dexly Finance (signed, split reads *"Need to
  Acquire Comp breakdown"*), and Ready Capital / Forward Financing / Agile Solutions
  (in progress, `BA SF` blank). A signed partner with unknown economics can't be
  prioritized for referrals.
- **10 partners have no usable marketing materials link** — 8 blank plus Awaken Finance and
  GMO Payment Gateway, which say only *"Follow up"*. Two of the missing are **signed**
  partners (Hum Capital, Liquid Ventures). NFS Leasing's link exists but is misfiled in
  `Required Documentation`.
- **Several signed partners are unreachable from the sheet.** Haut Finance and Reiger
  Shore — both signed — have **no contact name, email, phone, or website**. Liquid
  Ventures has only a bare email.
- **The three bottom-of-sheet prospects (JTSA, Raiseview, Ondeck) are effectively empty
  rows** (14–17 of 17 fields blank) and should either be worked or archived.
- At least **6 records have hygiene defects** carried over from the PDF extraction
  (concatenated URLs, a stray "Ryan" fused onto a link, an identical Drive link shared by
  two unrelated partners, duplicated links within one cell).

---

## 1. Field completeness scoreboard

Counts treat placeholder text (e.g. *"Follow up"*) as filled; see §3 for those.

| Field | Filled | Gap | Missing for |
|---|---|---|---|
| Referral Agreement Link | **1 / 30** | 29 | Everyone except JTSA — including all 15 signed partners |
| Meeting Notes | 9 / 30 | 21 | Most of the book (low priority — see §6) |
| Contact Phone | 20 / 30 | 10 | Haut, Awaken, GMO, Clearco, Reiger Shore, ARC, Liquid Ventures, JTSA, Raiseview, Ondeck |
| Cost of Capital | 21 / 30 | 9 | Haut, Awaken, GMO, Reiger Shore, Liquid Ventures, Forward Financing, JTSA, Raiseview, Ondeck |
| Required Documentation | 21 / 30 | 9 | Same as Cost of Capital minus Haut… (Haut included; see per-lender table) |
| Revenue Requirements | 22 / 30 | 8 | Awaken, GMO, Reiger Shore, Liquid Ventures, Forward Financing, JTSA, Raiseview, Ondeck |
| Marketing Materials Link | 22 / 30 | 8 blank (+2 placeholders) | Liquid Ventures, Hum Capital, NFS Leasing†, Customers Bank, Agile Solutions, JTSA, Raiseview, Ondeck |
| BA SF (referral split) | 23 / 30 | 7 | Ready Capital, Slim Capital, Forward Financing, Agile Solutions, JTSA, Raiseview, Ondeck |
| Contact Name | 23 / 30 | 7 | Haut, Awaken, Reiger Shore, Liquid Ventures, JTSA, Raiseview, Ondeck |
| Contact Email | 24 / 30 | 6 | Haut, Awaken, Reiger Shore, JTSA, Raiseview, Ondeck |
| Website | 24 / 30 | 6 | Haut, Awaken, Reiger Shore, Liquid Ventures, Raiseview, Ondeck |
| Relationship Owner | 25 / 30 | 5 | Clearco‡, Liquid Ventures, JTSA, Raiseview, Ondeck |
| Product Types / Industries / Deal Size | 26 / 30 | 4 | Liquid Ventures, JTSA, Raiseview, Ondeck |
| Referral Agreement Signed? | 27 / 30 | 3 | JTSA, Raiseview, Ondeck |
| Capital Category | 28 / 30 | 2 | Raiseview, Ondeck |

† NFS Leasing's materials link exists but sits in `Required Documentation`.
‡ Clearco's owner ("Ryan") was fused onto its marketing-materials URL in the source PDF.

---

## 2. Critical gaps (act first)

### 2.1 No executed agreements on file — all 15 signed partners

Haut Finance, BDIM, Big Think Capital, C6, Clearco, Reiger Shore, Liquid Ventures,
Breakout Finance, Slim Capital, Hum Capital, Bigfoot Capital, ARF Financial, Quantum
Financial Technologies, Dexly Finance, National Business Capital.

Every one is marked *Signed* but has an empty `Referral Agreement Link`. Several of the
recorded splits are non-trivial (e.g. Breakout's clawback terms, Quantum's per-product
schedule, Clearco's step-down over 12 months) and can't be enforced or audited from a
sheet cell. **Action:** locate each executed PDF in Drive, link it, and confirm the split
text in `BA SF` matches the contract.

### 2.2 Signed / near-signed partners with unknown economics

| Partner | Status | Problem |
|---|---|---|
| Slim Capital | Signed ("sending over copy") | `BA SF` blank — signed with no recorded split |
| Dexly Finance | Signed | `BA SF` = *"Need to Acquire Comp breakdown"* |
| Ready Capital | In Progress (W-9 / wiring sent) | `BA SF` blank |
| Forward Financing | In Progress | `BA SF` blank |
| Agile Solutions | In Progress (50/50 discussed, unsigned) | `BA SF` blank — verbal only |

### 2.3 Signed partners with no way to contact them

| Partner | Missing |
|---|---|
| Haut Finance | Contact name, email, phone, website (only a Drive link and "Ryan" as owner) |
| Reiger Shore (Greg) | Contact name, email, phone, website — "Greg" in the row title is the only identifier |
| Liquid Ventures | Only `M@liquidityventures.io`; no name, phone, website, or owner |

### 2.4 Missing or placeholder marketing materials

| Partner | Status | Gap |
|---|---|---|
| Hum Capital | **Signed** | No materials link at all |
| Liquid Ventures | **Signed** | None; notes say "Reached out regarding Marketing materials" — pending since |
| Awaken Finance | In Progress | Placeholder *"Follow up"* |
| GMO Payment Gateway | No Program | Placeholder *"Follow up"* (low priority given status) |
| NFS Leasing | In Progress | Link exists but is misfiled under `Required Documentation` — move it |
| Customers Bank | In Progress | None (notes say "Sent all materials" — theirs to us may exist; not linked) |
| Agile Solutions | In Progress | None |
| JTSA / Raiseview / Ondeck | Prospect | None (rows are empty shells; see §5) |

---

## 3. Placeholder values masquerading as data

These fields pass a "non-empty" check but contain no usable information:

- **Awaken Finance** — `Marketing Materials Link`: "Follow up"; `Referral Agreement
  Signed?` / `BA SF`: "Willing to share economics" (no numbers).
- **GMO Payment Gateway** — `Marketing Materials Link`: "Follow up".
- **Dexly Finance** — `BA SF`: "Need to Acquire Comp breakdown".
- **Area (Aera)** — `Contact Phone`: a Calendly URL, not a phone number.
- **Agile Solutions** — `Contact Phone`: a Google Calendar booking URL, not a phone number.
- **Saratoga Investment Corp** — `BA SF`: "50/50 **Pending agreement**" (terms not final).
- **Monroe Capital** — `BA SF`: "Mentioned 50 Bips" (verbal, unconfirmed).

---

## 4. Data-hygiene defects (present but wrong)

Carried over from the PDF extraction; each needs a one-time cleanup in
`data/lenders.json` / `data/lenders.csv` (and re-embedding into `index.html`):

1. **ARC and Reiger Shore share the identical Drive link**
   (`…1kIW5VJ5xM_m4WD9B9_KNVhBeKvI_oS2y…`) as their marketing materials. Two unrelated
   firms almost certainly don't share one deck — one of the two links is a copy/paste
   error. Verify which partner the file actually belongs to and re-source the other.
2. **Clearco** — the string `Ryan` is fused onto the end of the second marketing URL, and
   `Relationship Owner` is empty. Move "Ryan" into the owner field and fix the URL.
3. **C6** — the same Drive link appears twice in `Marketing Materials Link`
   (`…1nXxHSMH7vjEmEqmenIaaLYw59dI8UTEW…` duplicated); dedupe.
4. **Biz2Credit** — one Drive link duplicated (with a stray trailing `.` on two links);
   dedupe and strip punctuation.
5. **BDIM, Ready Capital, ARF Financial, National Business Capital** — multiple Drive
   URLs concatenated with no separator (`…drive_linkhttps://…`), which breaks link parsing.
   Insert separators.
6. **NFS Leasing** — a Drive link (likely the credit application or a one-pager) is
   embedded at the end of `Required Documentation` instead of `Marketing Materials Link`.
7. **Hum Capital** — a URL (`humcapital.com/our-story/`) is fused onto the end of
   `Required Documentation`.
8. **ARC** — a Google Docs link is fused into `Meeting Notes` text with no separator.
9. **Area vs. Aera** — the row is named "Area" but the website, email, and contact all say
   **Aera** (`aera.inc`). Confirm the correct name and normalize.
10. **Name normalization** — "Reiger Shore (Greg)" and "Liquid Ventures limited (Crypto
    Lending)" embed contact/category info in the `Name` field; move it to the proper columns.

---

## 5. Empty-shell prospect rows

**JTSA (Crypto Lending)**, **Raiseview**, and **Ondeck** are 14–17 fields empty each.
JTSA at least has a website and — oddly — the book's *only* populated
`Referral Agreement Link` despite no signature recorded (verify what that document
actually is; if it's a draft, label it as such). Raiseview and Ondeck have literally
nothing but a name. **Action:** either assign an owner and start discovery, or move them
out of the active book so pipeline metrics aren't diluted.

---

## 6. Lower-priority gaps

- **Meeting Notes** are empty for 21 of 30 partners, including long-standing signed ones.
  Not blocking, but the CRM can't answer "when did we last talk to X" for most of the book.
- **Cost of Capital / Revenue Requirements / Required Documentation** are missing for the
  same cluster (Haut, Awaken, GMO, Reiger Shore, Liquid Ventures, Forward Financing, plus
  the empty prospects). For advisory-style partners (Reiger Shore, Agile) this may be
  inherently deal-specific — note that explicitly rather than leaving the cell blank.
- **GMO Payment Gateway** is *No Program* (no referral fee; must charge client 1–2%) —
  decide whether it stays in the book as a pass-through option or is archived.

---

## 7. Per-lender gap matrix

Sorted by number of missing fields (hard blanks only; placeholders flagged with ⚠ in §3).

| # | Partner | Status | Missing fields |
|---|---|---|---|
| 29 | Raiseview | Prospect | **All 17** |
| 30 | Ondeck | Prospect | **All 17** |
| 28 | JTSA (Crypto Lending) | Prospect | 14 — everything except category, website, agreement link |
| 10 | Liquid Ventures | Signed | 12 — products, industries, deal size, cost, revenue reqs, docs, materials, owner, website, phone, name, agreement link |
| 4 | Awaken Finance | In Progress | 9 — cost, revenue reqs, docs, website, email, phone, name, notes, agreement link |
| 8 | Reiger Shore (Greg) | Signed | 9 — cost, revenue reqs, docs, website, email, phone, name, notes, agreement link |
| 1 | Haut Finance | Signed | 8 — cost, docs, website, email, phone, name, notes, agreement link |
| 5 | GMO Payment Gateway | No Program | 6 — cost, revenue reqs, docs, phone, notes, agreement link |
| 17 | Forward Financing | In Progress | 5 — split, cost, revenue reqs, docs, agreement link |
| 7 | Clearco | Signed | 4 — owner‡, phone, notes, agreement link |
| 11 | Ready Capital | In Progress | 3 — split, notes, agreement link |
| 15 | Slim Capital | Signed | 3 — split, notes, agreement link |
| 18 | Hum Capital | Signed | 3 — materials, notes, agreement link |
| 21 | NFS Leasing | In Progress | 3 — materials†, notes, agreement link |
| 26 | Agile Solutions | In Progress | 3 — split, materials, agreement link |
| 2 | BDIM | Signed | 2 — notes, agreement link |
| 3 | Big Think Capital | Signed | 2 — notes, agreement link |
| 6 | C6 | Signed | 2 — notes, agreement link |
| 9 | ARC | In Progress | 2 — phone, agreement link |
| 14 | Breakout Finance | Signed | 2 — notes, agreement link |
| 19 | Bigfoot Capital | Signed | 2 — notes, agreement link |
| 20 | Area (Aera) | No Program | 2 — notes, agreement link |
| 22 | ARF Financial | Signed | 2 — notes, agreement link |
| 23 | Quantum Financial Technologies | Signed | 2 — notes, agreement link |
| 24 | Dexly Finance | Signed | 2 — notes, agreement link (⚠ split is placeholder) |
| 25 | Customers Bank | In Progress | 2 — materials, agreement link |
| 12 | Saratoga Investment Corp | In Progress | 1 — agreement link |
| 13 | Monroe Capital | In Progress | 1 — agreement link |
| 16 | Biz2Credit | In Progress | 1 — agreement link |
| 27 | National Business Capital | Signed | 1 — agreement link |

† misfiled, not absent — see §4. ‡ fused onto URL — see §4.

---

## 8. Recommended closure plan

1. **Agreements on file (this week):** pull all 15 executed referral agreements into the
   Drive folder and populate `Referral Agreement Link`; verify recorded splits against
   contract text. Chase Slim Capital's promised copy and Dexly's comp breakdown.
2. **Economics before referrals:** don't route deals to Slim, Dexly, Ready Capital,
   Forward Financing, or Agile until the split is documented.
3. **Contact rescue:** get a named contact + email for Haut Finance, Reiger Shore, and
   Liquid Ventures (all signed, all currently unreachable from the sheet).
4. **Materials sweep:** collect decks/one-pagers for Hum, Liquid Ventures, Awaken,
   Customers Bank, Agile; relocate NFS Leasing's misfiled link.
5. **One-time data cleanup:** fix the ten hygiene items in §4 in `data/lenders.json`,
   regenerate `data/lenders.csv`, and re-embed into `index.html`.
6. **Prospect triage:** work or archive JTSA, Raiseview, Ondeck; decide GMO's disposition.

---

*Methodology: field-by-field completeness computed programmatically from
`data/lenders.json` (30 records, 17 tracked fields plus derived `Onboarding Status`);
placeholder and hygiene findings from manual review of every record. Per the repo README,
records were extracted from a PDF export — spot-check contact details against the original
workbook before outreach.*
