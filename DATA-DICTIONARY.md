# Data dictionary: well-drilling-cost-register.csv

| Column | Meaning |
|---|---|
| id | Stable row ID. Prefix = item group (DRL drilling, CAS casing, SYS complete system, PMP pump, TNK pressure tank, PRM permit/notification, WTR water testing, INS inspection, DEP deepening, REH rehabilitation, ABN abandonment/sealing, CHL disinfection, SVC service/diagnostic, SEL seal/wellhead, DEV development, TST test hole, ELC controls/electrical, MTH method note) |
| cost_item | Normalized cost category |
| service_component | What is priced, in our words, close to the source wording |
| scope | What the source says is included or excluded; blank if not stated |
| low_usd | Low end of a published range (USD) |
| high_usd | High end of a published range (USD). Open-ended ranges ("$X+") keep the stated top number; see quote |
| point_or_stated_usd | Single published price, "starting at" price, or the source's own stated average |
| unit | Unit as published (per foot, per well, per test, per permit, per job, starting price, add-on, per hour) |
| geography | Market the price applies to, as stated or as shown on the source |
| state | USPS code(s), semicolon-separated; US = national |
| source_publisher | Publisher and type in parentheses (contractor, county agency, state agency, university lab, published cost guide, extension publication) |
| independent_business | Contractor name when the price is a business's own; blank for agencies and guides |
| source_url | Page or document the price came from |
| source_date | The source's own date/effective date, or "Not stated" |
| retrieved_date | Date we fetched the source (YYYY-MM-DD) |
| source_type | Kind of page (contractor price list, government fee schedule, lab fee page, published cost guide, ...) |
| source_tier | primary = the price-setter's own published price/fee; secondary = compiled range (cost guide, directory profile) |
| record_type | price or method_note |
| quote_verbatim | The price wording copied from the source (whitespace normalized; table cells may run together) |
| notes | Caveats: staleness, ambiguity, inferred fields |
