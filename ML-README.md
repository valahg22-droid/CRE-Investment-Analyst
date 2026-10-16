# Medical Office Lease Analysis Model (Tenant Representation)

Excel model built from a real Letter of Intent I negotiated as the tenant's broker for a 1,500 SF chiropractic suite in Clermont, FL. Names and address are anonymized.

## LOI terms modeled
| Term | Value |
|---|---|
| Premises | 1,500 SF |
| Base rent | $32.00/SF/yr NNN, 3% annual escalation |
| NNN charges (maint., taxes, insurance) | $6.25/SF/yr |
| Term | 3 years + two 3-year renewal options |
| Concession | 1 month free base rent |
| Broker commission | 3% of aggregate contract, paid by Landlord, also due on renewals |
| Deposit | 1 month ($4,781.25) |
| Year-1 total rent / monthly | $57,375 / $4,781.25 (model reconciles to LOI) |

## Workbook tabs
- **Assumptions** – all inputs. Blue = LOI term, blue on yellow = analyst assumption, black = formula.
- **Summary** – annual cash flow, effective rent, NPV, rent-to-revenue, commission, chart.
- **Sensitivity** – five tables: (1) base rent × escalation, (2) base rent × free-rent months, (3) free-rent months × lease term, (4) base rent × practice revenue, and (5) four negotiation scenarios. Tables 1–4 are Excel What-If Data Tables driven by the "driver" cells in `I3:J17`; keep those equal to the Assumptions base case. Table 5 is direct formulas.
- **Monthly Schedule** – 108-month engine (initial term + two renewal options) behind everything else.

## Key formulas
- Escalated rent: `Rent × (1+g)^(year-1)`
- Total base rent over N years: `SF × Rent × ((1+g)^N − 1)/g − SF × Rent/12 × FreeMonths`
- Net effective rent: `Total base rent ÷ (N × SF)`; gross effective adds NNN
- NPV: monthly cash flows × `1/(1+r/12)^month`

## Assumptions not in the LOI
3% NNN growth, 8% discount rate, $450K illustrative practice revenue. Market rent of $32/SF is the Clermont rate at the start of 2026.

## Key takeaways
- Face rent is at market ($32/SF), so the value is in the concessions: one free month lowers effective rent, and the 1-month deposit limits landlord exposure.
- A landlord counter (higher rent, 3.5% bumps, no free rent, higher NNN) would cost about $16,400 more over 3 years; the tenant's best case would save about $13,500.
- A free month is worth more on short terms: $1.33/SF at 2 years vs. $0.38/SF at 7 years.

## How this was built
I negotiated the lease and defined the terms and analysis. I used AI assistance (Claude) to build the initial workbook structure, then rebuilt and tested the sensitivity tables myself with Excel What-If Data Tables and checked the results against the LOI (Year-1 total rent $57,375; $4,781.25/month).

Open in Excel to calculate.
