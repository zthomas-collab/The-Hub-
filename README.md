# The-Hub-

## The Closing Desk (`closing-desk/index.html`)

A SoftPro-style closing and title workbench that generates a HUD-1 Settlement Statement. It is a single HTML file with no build step: open it in a browser.

**Enter once, use everywhere.** Each fact is entered on one screen and every other module reads it:

| Module | What it holds | Feeds |
|---|---|---|
| Dashboard (home) | Clickable metric tiles (open, closing this week / 30 days, need attention, coming due, closed this month), flagged-files list, 7-week closing schedule timeline, notifications, next-14-days list, recent activity and documents | Each alert opens the file on the screen that fixes it |
| Closing tracker | Per-file milestones (title search, buyer/seller info sheets, payoff, survey, HOA estoppel, lender package, HUD-1, closing, funding, recording) with due dates computed from open/closing dates | Overdue items flag the file; Drive documents with matching names auto-mark items received |
| Audit log | Automatic who/when/what entry for every field change, receipt, check, wire, HUD version, document and automation action | Dashboard recent activity |
| Contacts directory | Every contact across all files, combined by name, with their files and next closing | Name autocomplete fills contact details on any file |
| File sidebar | Search every saved file by file #, address, party or parcel; open files, upcoming closings, recent documents | Opens any file into the SoftPro-style header band |
| Order | File/loan numbers, dates, property, legal, price, loan, deposit | HUD boxes B, G, I; lines 101, 201, 202 |
| Contacts | Buyer, seller, lender, settlement agent, underwriter, brokers, tax collector, recorder, payoff lenders | HUD boxes D, E, F, H; every payee dropdown |
| Prorations | Annual tax/assessment, period, paid/unpaid | Lines 106–112 / 406–412 or 210–219 / 510–519 |
| Settlement charges | Lines 700–1300, payee per line, P.O.C., rate-table calcs | Line 1400 → 103 and 502; ledger disbursements |
| Transfer & excise taxes | State rule set for all 50 states + DC (deed/transfer, mansion, mortgage, intangible taxes; graduated and marginal brackets; customary payer), listed localities (NYC, Chicago, Philadelphia, Miami-Dade, LA, etc.), local add-ons, per-file confirmation | Lines 1203–1206 and the ledger; rules marked "confirm locally" raise a warning until confirmed |
| Payoffs & credits | Lien payoffs, seller credits, third-party items | 500 series and paired 100/200/400 lines |
| Trust ledger | Receipts, auto-built disbursements, check/wire issuance | Balance check: receipts − disbursements = $0.00 |
| HUD-1 | Generated 3-page statement; click any amount to enter it and it saves to the owning screen (charges, order, payoffs/credits) with an audit entry with discrepancy check | Close file is blocked while anything is out of balance |
| Documents · Drive | Per-file Google Drive folder (create or link), HUD-1 versions saved as Google Docs, new Docs/Sheets, attach existing Drive files | Dashboard document list |
| Deed | North Carolina general warranty deed filled from the file: grantor/grantee (Contacts), legal description, parcel, county, property address, excise tax (tax engine), derivation clause (book/page/date of the vesting deed), plat reference, tenancy, marital status, entity signers and NC acknowledgment. Readiness checks include a grantor vs. owner-of-record match | Download (.html) or save to the file's Drive folder; versioned and audited |
| File labels | Preset and custom labels (Rush, Cash deal, 1031 exchange, Estate / probate...) | Sidebar, file header, dashboard filter and search |
| Field codes & merge | `{{Order.Buyer.Names}}`-style codes and a merge template | Any document template |

New files start with every amount at $0.00. **Rates & settings → Open a test scenario** loads clearly fictional data that exercises every calculation.

Title premium defaults are Florida's promulgated rates with a 70% agent split. Transfer tax rules reflect statutes and common local rates as known in mid-2025. Verify them for your county and underwriter before use. When opened as the published claude.ai artifact, files save to the artifact's shared database (visible on any device and to people the artifact is shared with) and Google Drive runs through each viewer's own claude.ai Google Drive connector. Opened as a local file, it falls back to browser storage and Drive is unavailable.
