# Methods

**Scope.** Published US prices for private (residential/domestic) water well work: drilling, casing, complete systems, pumps and tanks, permits and state notifications, water testing, inspection, disinfection, deepening, hydrofracturing and abandonment.

**Collection (Oct 15, 2026).** Sources were found by web search and by reusing cost-source leads in The Well Drilling Guide's research files. Each page or PDF was downloaded and converted to text; two JavaScript-rendered pages (T.J. Ogden Co.; Kalamazoo County PDF) were captured with a page-fetch tool. Raw captures are kept in `raw/` (not for publication).

**Rules.**
1. Only prices printed on the source. Nothing is estimated, interpolated, averaged, inflation-adjusted or converted.
2. Every row carries a verbatim quote; a script checks that each quote appears in the captured source text. All price rows pass.
3. "Starting at", "about", "approximately" and open-ended "+" values are recorded as published and flagged in `unit`/`notes`.
4. Where a fee schedule shows two years (e.g. 2025 and 2026), the current year is used and both are noted.
5. Inferred fields are flagged in `notes` (e.g. Portage County's state, Bracker Pump Service's region from area codes).
6. Method notes are separate rows with `record_type = method_note`.

**Tiers.** Primary: a contractor's own published price, or a government/university fee schedule. Secondary: compiled ranges from cost guides (DrillerDB, HomeGuide, HomeAdvisor) and a contractor's self-listed ranges on a directory profile (ProMatcher).

**Limitations.**
- Not a random or representative sample; heavily weighted to pump work, permits and lab testing, because few drillers publish per-foot drilling prices.
- Rows flagged HISTORICAL in `notes`: the Haynes & Sons price list (undated, 2017 upload path), NCWQR lab prices (2014) and UNL extension figures (2002 survey). They are kept for reference only. Many other contractor pages are undated.
- Contractor "cost guide" pages describe typical local ranges, not fixed price lists.
- Government fees exclude state surcharges unless stated.
- One row (Lincoln Trail District, KY) is quoted through DrillerDB because the agency page could not be fetched as text.

**License.** Compilation released under CC BY 4.0 by The Well Drilling Guide. Underlying figures belong to their publishers; cite them.
