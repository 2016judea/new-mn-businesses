# Data model: new Twin Cities businesses, by city and industry

Written 2026-10-17 from the need alone (BUSINESS.md rule 5). Buyer: any bookkeeper or CPA.
First prospect: Matt Daly, MRD Consulting, whose Craigslist post sells "basic QuickBooks
accounting for your business... includes a one-time set up (or clean up fee)" to
"construction, manufacturing, real estate development, professional services, food and
beverage, retail". A business registered this month has no books and no bookkeeper.

## The ideal model

**Business** (one new registration)
| field | the question it answers |
|---|---|
| name | who is it? |
| filing date | is it new enough to have no bookkeeper? |
| entity type (LLC, corp, assumed name) | will it need payroll and a balance sheet, or is it a sole proprietor's DBA? |
| principal address, city | is it in my territory? |
| industry (NAICS sector) | is it one of the industries I know? |
| organizer / manager name | who do I ask for? |
| registered agent | is a law firm or LegalZoom already in the picture? |
| size (employees band) | is it a $50/hr client or a CFO client? |

## Reality check, field by field (2026-10-17)

| field | free source we may sell from? | result |
|---|---|---|
| name, filing date, type, address, officers, agent | MN SoS Business Bulk Data | **We hold it, but it is licensed non-commercial and certified under Minn. Stat. 5.15 / 609.48.** Selling a list from it breaches that. It also ends 2026-07-31, so it holds none of the last 60 days. |
| same, live | mblsportal.sos.mn.gov | Search is by name only, no filing-date query. It also refused connections from here on 10/17 (75 s timeout). |
| industry | none free. SoS: "type of business conducted is NOT AVAILABLE from this office." Only the voluntary MN Business Snapshot survey carries NAICS. | **fails** |
| size | Business Snapshot survey (voluntary) | **fails** without purchase |

Spread is not the problem: SoS reports 8,274 to 11,842 new filings a month statewide in 2026
(9,218 new MN LLCs in August alone).

## Verdict: stop. Every field fails on licence or cost

What would fill it, priced 2026-10-17 from sos.mn.gov (spending is Aidan's gate):

| purchase | fills | cost |
|---|---|---|
| Business Bulk Data, commercial licence | name, date, type, address, officers, agent; may be shown to customers, not resold in bulk | $710 per monthly file |
| Active Business Data, weekly | name + primary address of every active business; diff two weeks = the new ones (no officers) | $30 a week |
| MN Business Snapshot Bulk Data | NAICS industry, employee band, revenue band, for businesses that answered | $100 (Minnesotans), one-time or monthly |

Cheapest version that matches the thesis: Active Business Data weekly ($30/wk) for the new
names and addresses, plus Snapshot bulk ($100) for industry. Check both licence agreements
before buying: the Active Business Data guide and the Snapshot private licence
(sos.mn.gov/media/5531) govern whether a $5 list may show the rows.
