# Industrial Warehouse NNN Acquisition Model

Excel model analyzing the purchase of a 2,016 SF industrial warehouse that will be leased on a triple-net (NNN) basis and sold after a 5, 8 or 10-year hold. It includes a month-by-month rent schedule for the 3-year lease.

## Files

| File | Purpose |
|---|---|
| `Warehouse_NNN_130K_Down_Analysis.xlsx` | The financial model (5 tabs) |
| `Investment_Memo_Warehouse_NNN.pdf` | 6-page investment memo with recommendation, results and rent schedule findings |
| `Investment_Memo_Warehouse_NNN.docx` | Same memo in Word (for editing / Google Drive) |
| `README.md` | This guide |

## Deal inputs (from the client)

| Item | Value |
|---|---|
| Purchase (offer) price | $270,000 |
| Building size | 2,016 SF |
| Base rent | $14.00/SF/yr |
| NNN charges | $4.50/SF/yr |
| Annual rent escalation | 3.5% |
| Down payment | $130,000 |
| Hold periods | 5, 8 and 10 years |
| Lease | 3 years, NNN, 1 month free rent, no tenant improvement allowance |

Everything else (expense growth, vacancy, management fee, reserves, closing costs, loan terms, exit cap rate, selling costs, lease start date) is an **assumption** and is shaded yellow. Replace them with real quotes and actuals.

## Workbook tabs

1. **Inputs** - every deal assumption in one place. Blue text = typed input, black = formula, yellow fill = assumption to confirm. Change deal numbers here only.
2. **Summary** - side-by-side deal metrics and returns (5/8/10-year) for both loan scenarios, plus a DSCR check against the lender minimum.
3. **Rent Schedule** - 36-month lease schedule. Links to Inputs for SF, rent, NNN, escalation and expense growth; lease-specific inputs on the tab are start date, term, free-rent months, NNN-abatement toggle and TI allowance. Shows monthly base rent, abatement, NNN, total due and cumulative cash, then an annual summary and key lease metrics.
4. **PF Client 130K** - 11-year pro forma for the client's $130,000 down payment: income, expenses, NOI, debt schedule, DSCR, cash flow, sale analysis, IRR and equity multiple.
5. **PF Alt 70 LTV** - same pro forma for a 70% loan-to-value comparison loan.

### How the model works
- **NOI** = base rent - vacancy + NNN reimbursements - NNN expenses - management fee - non-recoverable expenses - capital reserve.
- **Loan payment** = monthly P&I on a fixed-rate loan; the loan balance at any year is calculated with `FV`.
- **Sale price** = Year N+1 NOI / exit cap rate, less selling costs, less loan payoff.
- **IRR** uses the equity cash flows in rows 55-57 of each pro forma tab (initial equity, annual cash flow after debt, and net sale proceeds in the final year).
- **Max loan at lender DSCR** shows the largest loan the income supports at the minimum coverage ratio.
- **Rent schedule:** base rent steps up by the escalation each lease anniversary; Month 1 base rent is abated; NNN is still billed during free rent unless cell B13 on the Rent Schedule tab is set to 1.

## Using the model

1. Open in Excel. The file has no stored results until it calculates; if values look stale or blank, press Ctrl+Alt+F9 (Cmd+= on Mac).
2. Edit only the blue cells on **Inputs** (and the lease cells on **Rent Schedule**). Do not type over formulas elsewhere.
3. Review **Summary** and **Rent Schedule** for results and the memo for the narrative.

## Default financing assumptions (confirm with lenders)

6.75% fixed, 25-year amortization, 10-year term, 1% origination fee + $5,000 lender costs, 1.25x minimum DSCR, 7.0% exit cap rate, 3.5% selling costs.

## Results (client scenario, $130K down)

| Metric | Value |
|---|---|
| Loan / LTV | $140,000 / 51.9% |
| Cash to close | $140,450 |
| Year-1 NOI | $26,326 |
| Going-in cap rate | 9.8% |
| Year-1 DSCR | 2.27x |
| IRR (5 / 8 / 10 yr) | 25.6% / 21.3% / 19.9% |
| Equity multiple (5 / 8 / 10 yr) | 2.76x / 3.61x / 4.24x |

## Rent schedule findings (3-year lease, 1 month free, no TI)

| | Net base rent | NNN | Total due from tenant |
|---|---|---|---|
| Year 1 | $25,872 | $9,072 | $34,944 |
| Year 2 | $29,212 | $9,344 | $38,556 |
| Year 3 | $30,234 | $9,624 | $39,859 |
| **3-year total** | **$85,318** | **$28,041** | **$113,359** |

- Month 1 is only the $756 NNN charge (base rent abated). From Month 2 the tenant pays $3,108/month ($2,352 base + $756 NNN), rising 3.5% on each anniversary.
- The free month is worth $2,352 (about 2.7% of scheduled base rent). With no TI allowance, that is the only landlord concession.
- Average net base rent over the term is $14.11/SF/yr.
- The pro forma tabs do **not** deduct the free month, so Year-1 income there is $2,352 too high. Adjusted, Year-1 cash flow is about $12,366 (vs. $14,718), Year-1 DSCR about 2.07x, and IRRs are about 25.2% / 21.0% / 19.7% (0.2-0.4 points lower). This adjustment is calculated separately; it is not in the workbook.
- The 3-year lease is shorter than the 5, 8 and 10-year holds; the model assumes rent keeps growing 3.5% after expiry. Renewal or re-leasing risk should be verified.

## Recommendation (see memo)

Acquire at the $270,000 offer with $130,000 down, subject to confirming size, rent, lease and tenant credit, inspection, Phase I environmental, title, zoning and financing, and re-testing a higher exit cap rate.

## Limitations

- Pre-income-tax: no depreciation, capital gains, recapture or 1031 exchange modeling.
- Florida's state sales tax on commercial rent was repealed effective Oct 1, 2025 and is not modeled.
- The $270,000 price for 2,016 SF is about $134/SF and yields a ~9.8% cap rate, well above typical Central Florida industrial cap rates. Verify price, size and rent before relying on the results.
- The 7.0% exit cap rate is below the 9.8% going-in cap rate, which assumes value growth at sale; test a higher exit cap rate for a conservative case.
- Lease start date (01/01/2027) is a placeholder.
- Market benchmarks mentioned are general knowledge, not verified current data. This is not investment, tax or legal advice.
