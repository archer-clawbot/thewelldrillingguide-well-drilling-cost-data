# Well Drilling Cost Register (US, published prices, October 2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23404401.svg)](https://doi.org/10.5281/zenodo.23404401)

Published by **The Well Drilling Guide** (https://www.thewelldrillingguide.com/). This GitHub repository is a mirror; the canonical, versioned release is on Zenodo.

- **DOI:** [10.5281/zenodo.23404401](https://doi.org/10.5281/zenodo.23404401)
- **Zenodo record:** https://zenodo.org/records/23404401
- **Data page:** https://www.thewelldrillingguide.com/well-drilling-cost-data/
- **License:** CC BY 4.0 (see LICENSE)

## How to cite
The Well Drilling Guide. *Well Drilling Cost Register (US, published prices, October 2026)*. Zenodo. https://doi.org/10.5281/zenodo.23404401

---

---
license: cc-by-4.0
language:
- en
pretty_name: Well Drilling Cost Register (US, published prices, 2026)
size_categories:
- n<1K
tags:
- prices
- water-wells
- well-drilling
- private-wells
- construction-costs
- united-states
- tabular
configs:
- config_name: default
  data_files: well-drilling-cost-register.csv
---

# Well Drilling Cost Register (US, published prices, October 2026)

A dated, source-cited register of **180 published prices** for private water well drilling, casing, pumps, pressure tanks, permits, water testing, inspection, deepening, rehabilitation and abandonment in the United States. Every row records what the price covers, the market it applies to, the publisher, a link to the source page, the page's own date, the date we checked it, and the price wording quoted verbatim from the source.

Published by **The Well Drilling Guide** ([https://www.thewelldrillingguide.com/well-drilling-cost-data/](https://www.thewelldrillingguide.com/well-drilling-cost-data/)).

DOI: [10.5281/zenodo.23404401](https://doi.org/10.5281/zenodo.23404401)

## At a glance
| | |
|---|---|
| Rows | 181 (180 prices, 1 method note; 14 flagged HISTORICAL) |
| Sources | 58 web pages/documents, 27 independent businesses, plus state/county agencies, university labs and published cost guides |
| Tiers | 152 primary (businesses' own prices, government fee schedules, lab fee pages), 28 secondary (cost guides, directory profiles) |
| States | 32 states plus national rows: AR, AZ, CA, CO, CT, FL, GA, ID, IN, KY, MA, MD, MI, MN, MO, NC, NE, NH, NM, NY, OH, OK, PA, RI, SC, TN, TX, UT, VA, VT, WA, WI |
| Cost items | water_testing 38, pump_system 33, drilling 23, permit 23, complete_system 21, casing 6, inspection 6, pressure_tank 5, deepening 5, service_diagnostic 4, abandonment 4, disinfection 3, rehabilitation 2, controls_electrical 1, seal_grout 1, development 1, test_hole 1, service_labor 1, wellhead 1, drilling_casing 1 |
| Retrieved | Oct 15, 2026 |
| Format | CSV, UTF-8, 20 columns |
| License | CC BY 4.0 (compilation); figures are third-party facts, so cite the original source |

## Files
- `well-drilling-cost-register.csv`: the data
- `DATA-DICTIONARY.md`: every column
- `METHODS.md`: collection, tiers, rules, limitations

## Use it well
- **Compare like with like:** filter on `cost_item`, `scope`, `unit` and `geography`.
- **Count businesses, not rows:** use `independent_business`.
- **Don't average across rows** to make a "national average"; sources differ in scope and method.
- Government fees change on fiscal-year cycles; check `source_date`.
- `record_type = method_note` rows are not prices.
- These are **published prices, not quotes or completed-job data**, and not a representative sample.

## Example
```python
import pandas as pd
df = pd.read_csv("well-drilling-cost-register.csv")
permits = df[(df.cost_item == "permit") & (df.record_type == "price")]
print(permits[["service_component", "low_usd", "high_usd", "point_or_stated_usd", "unit", "geography", "source_publisher"]])
```

## Citation
The Well Drilling Guide (2026). *Well Drilling Cost Register (US, published prices, October 2026)*. CC BY 4.0. DOI: to be assigned on deposit.


## Citation
The Well Drilling Guide (2026). *Well Drilling Cost Register (US, published prices, October 2026)*. https://www.thewelldrillingguide.com/well-drilling-cost-data/. DOI: https://doi.org/10.5281/zenodo.23404401
