# Startup Expansion Strategy Dashboard (Power BI)

A Power BI dashboard advising a growing startup, *We Wash You Sleep*, on regional performance and new market opportunities. The company runs 150 stores across the U.S., including 10 recently opened expansion locations. This analysis combines store sales data with city demographics to guide where marketing investment should go next.

**Author:** Faith Kangogo &nbsp;&nbsp; **Tools:** Power BI Desktop · DAX · Excel · CSV

## Skills Demonstrated

- Power BI data modelling (joining business + demographic datasets)
- Custom DAX measures (ROMI, average revenue, average marketing spend)
- Interactive report design (slicers, cross-filtering, map visuals)
- Data cleaning and standardisation across sources
- Translating analysis into an expansion strategy

---

## Business Question

The company opened stores in 10 new U.S. cities and needed to know:

1. Which sales region is performing more efficiently?
2. How are the 10 new expansion stores performing against the established base?
3. Where are expansion efforts most likely to succeed next?

## Data

| Dataset | Contents |
| --- | --- |
| `StartupExpansion.xlsx` | 150 stores: city, state, sales region, expansion status, marketing spend, revenue |
| `US-Cities-Population.csv` | City population estimates, growth (2010-2015), density, and coordinates |

The two sources were cleaned and joined in Power BI on standardised city/state fields.

## Approach

1. **Data preparation:** cleaned and merged the Excel and CSV sources, standardised location fields.
2. **DAX measures:** built Average Revenue, Average Marketing Spend, and **ROMI** (Return on Marketing Investment = Revenue ÷ Marketing Spend). A ROMI of 14 means every $1 of marketing is associated with $14 of revenue.
3. **Report design:** region-level comparisons, a ranked analysis of the 10 new cities, a store location map, and slicers by region, city, and expansion status.

---

## Key Findings

*All figures computed directly from the source data.*

### 1. The two regions perform almost equally, with Region 1 holding a slight edge

Both regions spend nearly the same on marketing per store (about $2,890). Region 1 stores average **$40,567** revenue against Region 2's **$38,359**, giving Region 1 a ROMI of **14.0 vs 13.2**. In plain terms: both regions get roughly $13-14 back per marketing dollar, with Region 1 about 6% more efficient. There is no underperforming region to fix. This is a healthy, balanced network.

### 2. The 10 new expansion stores are outperforming the established base

New stores average **$45,809** revenue vs **$38,837** for existing stores (+18%), and convert marketing to revenue better too: ROMI of **15.8 vs 13.4**. The expansion strategy is working.

### 3. Standouts: Glendale (CA) and Brownsville (TX), plus one city to watch

**Glendale, CA** has the best marketing efficiency of any new store ($20.90 back per marketing dollar). **Brownsville, TX** generates the highest revenue of the ten ($63,148) while staying well above average on efficiency. At the other end, **College Station, TX** returns just $7.50 per marketing dollar, half the company average, on the lowest revenue of the group. It's a candidate for a strategy review, not more marketing spend.

### 4. Within the tested range, bigger cities performed better

All 10 new cities have populations between roughly **108K and 201K**. Within that band, both revenue and ROMI rise with city size (correlation of about 0.8): the largest of the new markets (Glendale, Chattanooga, Brownsville, Tempe) cluster at the top, while the smallest, College Station, sits at the bottom. This suggests the next round of expansion should favour the upper end of the mid-size range. *Caveat: with only 10 cities and no expansions into larger markets to compare against, this pattern holds within the tested range. It doesn't prove bigger is always better.*

## Dashboard Preview

![Dashboard map visual](image.png)

![New expansion cities view](new-expansions-view.png)

*Filtered to the 10 new expansion cities. Glendale, CA leads on marketing efficiency; Brownsville, TX leads on revenue.*

📄 The full report is available as a PDF: [View the dashboard export](startup-expansion-dashboard.pdf)

## Repository Contents

| File | Description |
| --- | --- |
| `startup-expansion-dashboard.pbix` | Power BI report file (open in Power BI Desktop) |
| `startup-expansion-dashboard.pdf` | PDF export of the full dashboard |
| `StartupExpansion.xlsx` | Store performance dataset |
| `US-Cities-Population.csv` | City demographic dataset |
| `image.png` | Dashboard screenshot |
| `new-expansions-view.png` | Dashboard filtered to the 10 new expansion cities |

## How to Explore

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Download and open `startup-expansion-dashboard.pbix`.
3. Use the slicers to filter by region, city, or expansion status. All visuals update dynamically.

No Power BI? The PDF export shows the complete dashboard.

## Possible Extensions

- Add time-series data to track ROMI trends after marketing changes.
- Test the city-size relationship with expansions into larger markets.
- Publish to Power BI Service for shareable, browser-based access.
