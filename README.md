# The-Hub-

## Closing Desk (`closing-desk/index.html`)

A SoftPro-style closing and title workbench that generates a HUD-1 Settlement Statement. It is a single HTML file with no build step: open it in a browser.

**Enter once, use everywhere.** Each fact is entered on one screen and every other module reads it:

| Module | What it holds | Feeds |
|---|---|---|
| Order | File/loan numbers, dates, property, legal, price, loan, deposit | HUD boxes B, G, I; lines 101, 201, 202 |
| Contacts | Buyer, seller, lender, settlement agent, underwriter, brokers, tax collector, recorder, payoff lenders | HUD boxes D, E, F, H; every payee dropdown |
| Prorations | Annual tax/assessment, period, paid/unpaid | Lines 106–112 / 406–412 or 210–219 / 510–519 |
| Settlement charges | Lines 700–1300, payee per line, P.O.C., rate-table calcs | Line 1400 → 103 and 502; ledger disbursements |
| Payoffs & credits | Lien payoffs, seller credits, third-party items | 500 series and paired 100/200/400 lines |
| Trust ledger | Receipts, auto-built disbursements, check/wire issuance | Balance check: receipts − disbursements = $0.00 |
| HUD-1 | Generated 3-page statement with discrepancy check | Close file is blocked while anything is out of balance |
| Field codes & merge | `{{Order.Buyer.Names}}`-style codes and a merge template | Any document template |

New files start with every amount at $0.00. **Rates & settings → Open a test scenario** loads clearly fictional data that exercises every calculation.

The default rates are Florida's: promulgated title rates, $0.70/$100 deed stamps, $0.35/$100 mortgage stamps, 0.2% intangible tax and a 70% agent split. Verify them for your county and underwriter before use. Data is saved in the browser's local storage only. Use "Copy this file's data" for backups.
