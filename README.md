# Air Freight Performance Dashboard
### Project background
Satnaq, a fictional Australian airline, operates in both passenger and freight services, across domestic and international market. 
The Head of Commercial & Freight Operations has requested a business performance analysis in preparation for an upcoming leadership meeting. The goal is to assess current-year performance and develop a forecast for the next 12 months to support strategic planning and decision-making.

The freight industry typically has strong seasonality driven by:

Peak seasons:
* Before and around Boxing Day and Christmas (August-December) - Highest volume due to holiday shopping, back-to-school, and year-end retail inventory
* Pre-Lunar New Year (January-February for Asia-Pacific routes) - Manufacturing rush before factory closures

Slower periods:
* Post-holiday (January-February) - Drop after holiday peak
* Mid-year (June-July) - Typically softer before peak season buildup
<br>

### Main KPIs
* Revenue - sales, equals to total chargeable weight multiplied by rate
* Weight - chargeable weight of the product
* Average rate - equals to revenue divided by weight
<br>

### Current Performance
<img width="1667" height="949" alt="image" src="https://github.com/user-attachments/assets/12d15243-346c-4432-8ad7-d75404bc74b9" />

Satnaq's freight division delivered $4.0 billion in revenue for FY25, with cargo operations contributing 97% ($3.88B) and mail services 3% ($124M). The business maintains a balanced operational model with freight equally distributed between dedicated freighter aircraft and passenger belly capacity.

| 1. Regional Performance |2. Network Concentration|3. Product Portfolio|4. Recommendation|
|---------|---------|---------|---------|
|Asia remains our strongest market at $1,938M, demonstrating robust growth of 37% from Q1 to Q4. The Americas emerged as our fastest-growing region with $1,536M in revenue and exceptional 39% quarter-on-quarter acceleration. Australasia contributed $438M with healthy 54% growth trajectory. UKEMEA at $93M offers considerable expansion opportunity. |Chicago O'Hare (ORD) leads origin points at 30% of revenue, followed by Shanghai Pudong (24%) and Hong Kong (17%). On the destination side, Sydney commands 49% of all revenue at $1.6B, with Melbourne adding another 17%. Combined, Australian destinations represent two-thirds of our total revenue, indicating significant market dependency. |QGQ 2 dominates at $2.5B ($7/kg), split between Kalulu Cargo ($1.7B) and Satnaq ($745M). QGQ 9 generates $796M at premium $15/kg rates via Kalulu Cargo. Satnaq operates mid-tier products (QGQ 4-5: $439M combined) and Mail ($124M). Premium products PRIORITY and QGQ 7 offer high yields ($25/kg, $18/kg) but lower volumes ($21M, $20M). |Average price of $7-$25/kg across carriers presents pricing and capacity optimisation opportunities. The strong Q4 performance across all regions provides positive momentum entering the new fiscal year. However, our heavy reliance on Australian destinations and limited UKEMEA presence present both risk and investment potentials. The focus is to optimise fleet utilisation by working with external stakeholders and other carriers while minimising costs. |
<br>

### Looking forward

<img width="1691" height="700" alt="image" src="https://github.com/user-attachments/assets/12d048a9-376a-4c02-a833-1e801a1b65e2" />

The forecast suggests a normalization period ahead, with revenue plateauing near or below current levels, around $300M - $350M per month. This provides an opportunity to focus on yield optimisation and operational efficiency rather than volume-driven growth. The seasonal peaks evident in historical data should continue, making Q4 and Q1 critical periods for maximising revenue capture.


### <br>Methodology
* Data source: extracts from ERP system
* Tools used: Excel for dataset, Power Query for data manipulation, Power BI for visualisation and PowerPoint for presentation and final callouts.

#### Data structure
| Field name | Definition | Data type                              |
|---------|-------------|--------------------------------------------|
| Fiscal Year | Finanical Year July - June | string |
| Month Sort| Combination of year and month | string |
| Carrier Code| Two digit airline code | string |
| Aircraft Type | Freighter or Passenger aircraft | string |
| Leg Orig | Three digit airport code detailing the origin of the flight | string |
| Leg Dest | Three digit airport code detailing the destination of the flight | string |
| Sales Region | The geographical region that generated the revenue | string |
| Product | Name of the product (each product has a different price point) | string |
| Revenue (AUD) | Revenue expressed in AUD | float64 |
| Chargeble Weight | Weight of the cargo/mail used for yield calculations | float64 |
| Average Rate | equals to Revenue divided by Chargeable Weight | float64 |
| Service Type| Cargo or Mail | string |

