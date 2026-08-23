# Chipotle Mexican Grill (CMG) — Comparable Companies Analysis

A full-cycle trading comps valuation project built in the style of a bulge-bracket Investment Banking Valuation Group deliverable: company research → tiered peer selection → financial data collection → multiples → statistical analysis → implied valuation → DCF cross-check → football field → presentation deck.

## Why This Project

Most "comps" portfolio projects stop at pulling five tickers into a spreadsheet and averaging a multiple. This one is built to demonstrate the parts of the process that actually separate a junior analyst from someone who understands valuation: **tiering a peer set by business-model comparability, handling statistical outliers with judgment rather than blind averages, reconciling two independent valuation methods that disagree, and documenting every assumption instead of hiding it in a hardcoded cell.**

## Deliverables

| File | Description |
|---|---|
| `CMG_Trading_Comps.xlsx` | Fully formula-linked 9-tab model: Cover, Company Overview, Peer Selection, Raw Data, Multiples, Trading Comps & Valuation, Sensitivity, Football Field (with native chart), Dashboard (with native chart) |
| `CMG_Trading_Comps_Deck.pptx` | 12-slide presentation: company overview, peer selection, financial comparison, valuation multiples, trading comps, DCF reconciliation, football field, recommendation, risks, appendix |

## Methodology Highlights

- **Tiered peer set, not a flat list.** Chipotle is ~100% company-operated; McDonald's, Yum!, Domino's, and RBI are majority-franchised. Blending their EV/EBITDA multiples without adjustment produces an apples-to-oranges valuation, so peers are split into a **Core tier** (fast-casual, company-operated — drives the primary valuation) and a **Reference tier** (large-cap franchised QSR — context only).
- **Outliers handled with judgment, not just a formula.** Sweetgreen's near-zero/negative EBITDA is excluded from EV/EBITDA statistics as not meaningful (n.m.). CAVA's 53x EV/EBITDA — a real, current-market number driven by its early growth stage — is carried as an explicit upside scenario rather than blended into a single base-case median.
- **Two independent valuation methods, reconciled rather than picked.** A comps-based valuation ($37–$65/share) is cross-checked against a simplified 5-year DCF ($15–$21/share). The methods diverge meaningfully, and the project explains *why* (a flat capex assumption in the DCF, and the market not yet fully re-rating CMG post food-safety headlines) rather than presenting one number as "the answer."
- **Every hardcoded input is flagged and sourced.** Blue font = input, black = formula, green = cross-sheet link — standard IB modeling convention — with a documented note wherever a figure required judgment (e.g., Wingstop's balance sheet data, which needed estimation from available public sources).

## Data Sourcing & Limitations

Figures were compiled from public company filings, earnings releases, and financial data aggregators as of August 2026. In live deal work, this data would be pulled from a single terminal (Capital IQ or FactSet) on one snapshot date to guarantee consistent accounting treatment across every peer — a constraint this project explicitly calls out rather than glosses over. This is a training/portfolio exercise, not investment advice.

## Tools Used

Python (`openpyxl` for the model, formula-driven throughout — no hardcoded calculated values), `pptxgenjs` for the deck (native charts, not images), public financial data research.
