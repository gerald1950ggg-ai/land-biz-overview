# County Search Workflow
### Repeatable Protocol for Auditing Counties — Land Flipping (Jack Bosch Criteria)

**Last Updated:** June 2026  
**Purpose:** Produce auditable, verified county-level go/no-go decisions. No fabricated data. Every data point must come from a named source.

---

## Overview

This workflow evaluates any U.S. county against the six Jack Bosch market selection criteria. Each step specifies the exact source, exact pull method, and a pass/fail/conditional threshold. When data is unavailable, you flag it — you never estimate and record it as fact.

**Estimated time per county:** 45–90 minutes for a full audit.

---

## Before You Start: Set Your Acreage Range

Jack Bosch's system works best on **1–40 acre rural parcels**. Before pulling any data, decide your target range and use it consistently across all searches:

| Range | Notes |
|---|---|
| 1–5 acres | Recreational, lifestyle, near-town parcels |
| 5–20 acres | Mini ranch, homestead play — Jack's sweet spot |
| 20–40 acres | Mini ranch, hunting land |
| 1–40 acres | Broadest filter — use when learning a new county |

Document your chosen range in your tracking spreadsheet before proceeding. **Never mix acreage ranges within the same ratio calculation.**

---

## CRITERION 1: State Disclosure Status

### What It Is
Whether the state publicly records real estate sale prices. Affects data quality for all subsequent steps.

### Data Source
**MOST Policy Initiative disclosure map** — [https://mostpolicyinitiative.org/science-note/disclosure-of-real-estate-sales-prices/](https://mostpolicyinitiative.org/science-note/disclosure-of-real-estate-sales-prices/)

Or use this reference list (verified June 2026):

| Category | States |
|---|---|
| **Full Disclosure** (sale prices public) | Most U.S. states including CO, CA, FL, AZ, NC, GA, TN, SC, OR, WA, NV, and many others |
| **Non-Disclosure** (sale prices private) | TX, ID, UT, AK, MS, ND, KS, LA, MO (most counties), MT, NM, WY |

### Pull Method
1. Check the list above or search "[State name] disclosure state real estate"
2. Confirm at the county assessor's website by searching a recent residential sale — if price is listed, it's a disclosure state

### Pass/Fail
- ✅ **PASS:** Full disclosure state — proceed normally
- ⚠️ **CONDITIONAL:** Non-disclosure state — use the Non-Disclosure Protocol (see end of document)
- ❌ No automatic fail — non-disclosure states are workable, but data-intensive

### Record In Spreadsheet
`Disclosure Status: Full / Non-Disclosure / Unknown`

---

## CRITERION 2: Metro Population (750K+ Required)

### What It Is
The nearest major metropolitan statistical area (MSA) must have a population of at least 750,000. This ensures there's a buyer base capable of absorbing the land you're selling.

### Data Source
**U.S. Census Bureau MSA population estimates** — [https://www.census.gov/data/tables/time-series/demo/popest/2020s-metro-and-micro-statistical-areas-detail.html](https://www.census.gov/data/tables/time-series/demo/popest/2020s-metro-and-micro-statistical-areas-detail.html)

**Backup:** Wikipedia's "List of Metropolitan Statistical Areas" — [https://en.wikipedia.org/wiki/List_of_metropolitan_statistical_areas](https://en.wikipedia.org/wiki/List_of_metropolitan_statistical_areas) (usually within 2% of Census estimates, good for quick check)

### Pull Method
1. Identify the nearest major city to the county under review (Google Maps: "[County name] to [nearest city] drive time")
2. Go to Census Bureau link above or Wikipedia
3. Find the MSA that encompasses that city
4. Record the population estimate

**Alternatively:** Google "[City name] metro area population 2024" — Google's Knowledge Panel usually shows Census MSA data

### Pass/Fail
- ✅ **PASS:** MSA population ≥ 750,000
- ❌ **FAIL:** MSA population < 750,000

### Record In Spreadsheet
`Nearest Metro: [City Name]` | `MSA Population: [number]` | `Source: Census/Wikipedia`

---

## CRITERION 3: Donut Distance (30–100 Miles from Metro Center)

### What It Is
The county must be within the "donut" — close enough to a major metro to attract buyers (retirees, outdoor enthusiasts, lifestyle buyers) but not so close that land prices are already retail. Sweet spot: **30–100 miles from the metro's center**.

### Data Source
**Google Maps** (no account needed) — [https://maps.google.com](https://maps.google.com)

### Pull Method
1. Open Google Maps
2. Search the metro city (e.g., "Denver, CO")
3. Right-click on the city center → "Measure distance"
4. Click on the county seat or county's center point
5. Record the straight-line distance **and** driving distance/time

**Alternative for batch work:** Draw concentric circles on Google Maps or use [https://www.freemaptools.com/radius-around-point.htm](https://www.freemaptools.com/radius-around-point.htm) — enter the metro city and set radii at 30 and 100 miles to see which counties fall in the donut.

### Pass/Fail
- ✅ **PASS:** County center is 30–100 miles (driving) from the metro center
- ⚠️ **CONDITIONAL:** 25–30 miles or 100–120 miles — research prices carefully, may still work if other criteria pass strongly
- ❌ **FAIL:** Less than 25 miles (too urban, land too expensive) or more than 120 miles (too remote, buyer pool thins out)

### Record In Spreadsheet
`Drive Distance to Metro: [X] miles` | `Drive Time: [X] hours` | `In Donut: Yes/No/Borderline`

---

## CRITERION 4: Infrastructure & Topography

### What It Is
Land in the target county must be accessible and usable. Rocky mountains, swamps, flood zones, and no road access make land harder to sell.

### Data Sources

**Road Access Check:**
- **Google Maps Satellite View** — [https://maps.google.com](https://maps.google.com) — switch to satellite, zoom into the county's rural areas and look for road grid patterns
- **USGS National Map** — [https://apps.nationalmap.gov/viewer/](https://apps.nationalmap.gov/viewer/) — shows topographic elevation

**Flood Zone Check:**
- **FEMA Flood Map Service Center** — [https://msc.fema.gov/portal/home](https://msc.fema.gov/portal/home) — search a parcel address or zoom into the county; identify what percentage of rural land falls in Zone AE (high-risk flood) vs. Zone X (low risk)

**Utility Access (Rough Check):**
- Google Maps Satellite View: Look for power lines in the area
- County GIS map (search "[County Name] County GIS") for utility overlay layers

### Pull Method
1. Open Google Maps Satellite View of the target county
2. Scan several rural areas — are there county roads on a regular grid? Or large roadless areas?
3. Check FEMA Flood Map for major flood zones
4. Note any obvious topographic barriers (major mountains, river floodplains)

### Pass/Fail
- ✅ **PASS:** County road grid accessible, mostly Zone X flood status, no major topographic barriers
- ⚠️ **CONDITIONAL:** Some flood-prone areas but not dominant; hilly terrain but accessible roads
- ❌ **FAIL:** Major portions are flood zone AE or AO, dense mountains with no road access, or desert with no infrastructure

### Record In Spreadsheet
`Road Access: Good/Moderate/Poor` | `Flood Risk: Low/Moderate/High` | `Topography: Flat/Rolling/Mountainous`

---

## CRITERION 5: Sold-to-Active Ratio (20–130%, Minimum 50 Sold)

### What It Is
The percentage of active listings that sold in the past 12 months. Also called the Sell-Through Rate (STR).

**Formula:** (Parcels Sold in Past 12 Months) ÷ (Current Active Listings) × 100 = STR%

**Jack Bosch's thresholds:**
- Target: 20–130% STR (sweet spot around 60–100%)
- Minimum sample: 50+ sold comps in the past 12 months (small counts = unreliable data)
- High STR (>130%): Seller's market — great for exits, but you may be overpaying on acquisition
- Very low STR (<20%): Slow market — land sits, cash tied up too long

### Data Source (Primary): Zillow
[https://www.zillow.com](https://www.zillow.com)

### Pull Method — Zillow Active Count

1. Go to zillow.com
2. In the search bar, type the county name (e.g., "Elbert County, CO")
3. Hit Enter — Zillow may show a map view
4. **Filter by property type:** Click "Home Type" → select **Lots/Land only** (uncheck all others)
5. **Filter by acreage:** Click "More filters" → under "Lot size," set to your target range (e.g., 5 acres min, 20 acres max)
6. **Status:** Make sure you're viewing "For Sale" listings
7. Under "Days on Zillow" — select **Any** (to capture all active, not just recent)
8. Record the total number of results shown in the upper-left (e.g., "47 results")

**→ This is your Active Count**

### Pull Method — Zillow Sold Count

1. Same filters (lots/land, acreage range)
2. Change status to **"Sold"**
3. Under "Sold In Last" — select **12 months**
4. Record the total number of results

**→ This is your Sold Count**

### Calculate the Ratio
`Sold Count ÷ Active Count × 100 = STR%`

**Example:**
- Active: 47
- Sold: 82
- STR = 82 ÷ 47 × 100 = **174%** ← hot market

### Cross-Check with Redfin (Required)
1. Go to [https://www.redfin.com](https://www.redfin.com)
2. Search the same county
3. Filter: Land/Lots only, same acreage range
4. Pull Active count and Sold-in-12-months count
5. Calculate Redfin STR

**If Zillow and Redfin are within 20–25% of each other:** Data is reliable, use the average  
**If they diverge by more than 25%:** Pull a third source (Realtor.com or Land.com) and identify which is the outlier

### Minimum Sample Threshold
If **Sold count is below 50** in the past 12 months: Mark the county as **insufficient data** — don't continue analysis. The sample size is too small to draw reliable conclusions. Flag it and move on to the next candidate.

### Pass/Fail
- ✅ **PASS:** STR 20–130% AND sold count ≥ 50
- ✅ **STRONG PASS:** STR 60–130% — active, predictable market
- ⚠️ **CONDITIONAL:** STR 130–200% — hot but may mean prices are running up; check median prices
- ⚠️ **CONDITIONAL:** STR 20–40% — slower market, adjust offer prices down accordingly (buy at 15–20% of value instead of 25–30%)
- ❌ **FAIL:** STR < 20% OR sold count < 50

### Record In Spreadsheet
`Active Count: [n]` | `Sold Count (12mo): [n]` | `STR: [%]` | `Source: Zillow/Redfin avg` | `Sample Adequate: Yes/No`

---

## CRITERION 6: Market Value Distribution ($5K–$300K Sweet Spot)

### What It Is
The range of land values in the county. You want most parcels priced between $5,000 and $300,000 — cheap enough to acquire with limited capital, expensive enough to make meaningful profit margins.

### Data Source (Primary): Zillow Active Listings
Use the same filtered view from Criterion 5 (lots/land, your acreage range, For Sale, Any days)

### Pull Method
1. In your filtered Zillow view (active listings), sort by **Price: Low to High**
2. Note the lowest 10% of prices (are most above $5K? or is there trash below $1K?)
3. Sort by **Price: High to Low** — note what the top 10% looks like
4. Scroll through to get a visual distribution: Where is the bulk of inventory priced?
5. Calculate or estimate the median price

**For a cleaner distribution:**
- Use Zillow's "List Price" filter — set Min: $5,000, Max: $300,000
- Note what % of listings fall within this range vs. outside it

### Cross-Check: County Assessor
Each county has a public assessor site with assessed values. While assessed values ≠ market values (assessors often run 6–12 months behind), they confirm whether the county has significant land inventory in your range.

**Find the county assessor:**
- Google: "[County Name] County Assessor parcel search"
- Most county assessors provide a public parcel search portal
- Search for vacant land parcels in your acreage range and review the assessed values

### Pass/Fail
- ✅ **PASS:** Majority of comparable parcels priced $5K–$300K; good distribution across the range
- ✅ **STRONG PASS:** Sweet spot concentration in $10K–$100K range — best for rapid acquisition and sale
- ⚠️ **CONDITIONAL:** Many listings below $5K (possible quality/access issues with cheap parcels) OR many above $300K (capital-intensive)
- ❌ **FAIL:** Average parcel price > $300K with most inventory above that level OR almost everything below $5K (too cheap = problem parcels)

### Record In Spreadsheet
`Price Range Observed: $[X]K – $[X]K` | `Median Price: ~$[X]K` | `% in Sweet Spot: [estimated %]`

---

## Scoring Summary Table

After completing all six criteria, score the county:

| Criterion | Weight | Your Data | Result |
|---|---|---|---|
| 1. Disclosure Status | Qualifier | | Pass / Non-Disc Protocol |
| 2. Metro Population ≥ 750K | Qualifier | | Pass / Fail |
| 3. Donut Distance 30–100 mi | Qualifier | | Pass / Conditional / Fail |
| 4. Infrastructure/Topography | Qualifier | | Pass / Conditional / Fail |
| 5. STR 20–130%, ≥50 sold | Primary Signal | | Pass / Conditional / Fail |
| 6. Price Range $5K–$300K | Primary Signal | | Pass / Conditional / Fail |

**Go:** All qualifiers pass + both primary signals pass  
**Conditional:** 1–2 conditionals, no hard fails → proceed with adjusted strategy  
**No-Go:** Any qualifier fails hard, or both primary signals fail

---

## Non-Disclosure State Protocol

When the county falls in a non-disclosure state (TX, ID, UT, AK, MS, ND, KS, LA, MT, NM, WY, or most of MO), sale prices are not in public records. You cannot rely on Zillow/Redfin sold data because those platforms populate sold prices from public records — what they show in non-disclosure states is often incomplete or from MLS-only.

### Step 1: Count Active Listings (Still Works)
Zillow and Redfin active listing counts remain valid — they show listings regardless of disclosure. Pull active count normally.

### Step 2: Get Sold Count from PropStream (Paid — ~$99/mo)
PropStream aggregates MLS data and off-MLS transactions. For non-disclosure states, it has the most complete sold data available to non-agents.
- **URL:** [https://propstream.com](https://propstream.com)
- **Pull method:** Search county → filter "Land" → filter by your acreage range → set "Sold In Last" to 12 months → record count
- **Cost:** ~$99/mo (cancel after research if needed)

**Free alternative:** If you know a local real estate agent in that state, they can pull MLS comps. This is the most reliable free method in non-disclosure states.

### Step 3: County Appraisal District (CAD) Data — For TX Specifically
Texas has its own appraisal district system with public parcel data (though not sale prices).
- **Find the CAD:** Google "[County Name] County Appraisal District" or [https://www.sao.texas.gov/Resources/Databases/Pages/AppraisalDistrictDatabase.aspx](https://www.sao.texas.gov/Resources/Databases/Pages/AppraisalDistrictDatabase.aspx)
- Each CAD has a public property search
- Pull: Appraised value, land size, prior year value trend
- **Note:** Appraised value in TX CAD ≠ market value. Use it as a floor/proxy, not a comp.

### Step 4: PropStream AVM for Individual Parcels
Once you have a specific parcel in mind, use PropStream's AVM to estimate market value.
- PropStream uses public records + MLS data + algorithm to produce an estimated value
- AVM error rate in non-disclosure states is 10–15% (vs. 1–2% in disclosure states)
- **Label any AVM-derived value as "ESTIMATED (PropStream AVM)" — never record it as a verified sale price**

### Step 5: Zillow Zestimate as Sanity Check
- Pull the individual parcel on Zillow
- Note the Zestimate — this is also an AVM, also 10–15% error in non-disclosure states
- If PropStream AVM and Zillow Zestimate are within 15% of each other: reasonable confidence
- If they diverge by more than 20%: treat as unreliable, escalate to Step 6

### Step 6: Local Realtor Call
When data is inadequate, call a local real estate agent or land broker in the county.
- Search [LandAndFarm.com](https://www.landandfarm.com) or [LandWatch.com](https://www.landwatch.com) for recent land listings in the county
- Call the listing agent of a recent comparable land listing
- Ask: "I'm researching land values in [County]. Can you tell me roughly what [X]-acre parcels have been selling for in the past 6 months?"
- **Record their response verbatim** and label it: "Local Realtor Estimate ([Name], [Date])"

### Non-Disclosure State Disclosure Record
In your spreadsheet, add a row:

`Non-Disclosure Protocol Used: Yes` | `AVM Source: PropStream / Zillow Zestimate` | `AVM Confidence: High / Medium / Low` | `Verified By: Realtor Name (if applicable)`

---

## Handling Unavailable Data

When any data point cannot be verified:

1. **Leave the cell blank or enter "—"** — never fill in a guess
2. **Add a note:** "Source unavailable as of [date]"
3. **Attempt an alternative source** (per this protocol)
4. **If still unavailable:** Mark the criterion as "Unverified" and downgrade the county's score by one tier

**What counts as unavailable:**
- Zillow shows < 10 results (too few to extrapolate)
- County assessor site is down or doesn't have a searchable portal
- Sold count < 50 (not "unavailable" — it's a data-based fail)
- Non-disclosure state with no PropStream access and no local realtor contact

**What does NOT count as unavailable:**
- "I didn't feel like looking it up" — every data point in this protocol has a free or paid source

---

## Recommended Tracking Spreadsheet Structure

Create one row per county evaluated. Columns:

| Column | Type |
|---|---|
| County Name | Text |
| State | Text |
| Date Audited | Date |
| Nearest Metro | Text |
| MSA Population | Number |
| Drive Distance (mi) | Number |
| In Donut? | Yes/No/Conditional |
| Disclosure Status | Full/Non-Disc |
| Road Access | Good/Mod/Poor |
| Flood Risk | Low/Mod/High |
| Active Count (Zillow) | Number |
| Active Count (Redfin) | Number |
| Sold Count 12mo (Zillow) | Number |
| Sold Count 12mo (Redfin) | Number |
| STR % | Calculated |
| Sample Adequate (≥50 sold) | Yes/No |
| Median Price | Dollar |
| Price Range | Text |
| Overall Score | Go/Conditional/No-Go |
| Notes | Text |

---

## Quick-Grab Reference — All Sources

| Data Point | Primary Source | Backup Source |
|---|---|---|
| Disclosure status | MOST Policy Initiative | State-specific search |
| Metro population | Census Bureau MSA tables | Wikipedia MSA list |
| Drive distance | Google Maps measure tool | FreemapTools radius |
| Infrastructure | Google Maps Satellite | USGS National Map |
| Flood zones | FEMA Flood Map (msc.fema.gov) | — |
| Active land count | Zillow (Lots/Land filter) | Redfin |
| Sold count (disclosure states) | Zillow 12-month sold | Redfin |
| Sold count (non-disclosure) | PropStream (~$99/mo) | Local MLS agent |
| Individual parcel AVM | PropStream AVM | Zillow Zestimate |
| County assessor values | County assessor portal | BatchData (paid) |
| Price distribution | Zillow active listing prices | County assessor |
| Local market intel | LandAndFarm.com listing agents | LandWatch.com |

---

*Sources: REtipster.com (Sold-to-For-Sale Ratio methodology, 2024), LandInvestingOnline.com (county selection workflow, 2025), LandAcademy.com (Red-Yellow-Green test), RealEstateInvestingMastery.com (county research podcast), BatchData.io (non-disclosure state AVM accuracy), PropLab.app (non-disclosure valuation guide), MOST Policy Initiative (disclosure state map), FEMA.gov, Census Bureau MSA data*
