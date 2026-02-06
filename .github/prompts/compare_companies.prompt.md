---
description: "Compare 2 companies from same sector"
---

Act as a comparative business analyst and generate a consulting-style dossier contrasting {Company A} and {Company B} within the {Industry}. Focus on evidence-led analysis using the 80/20 principle to highlight critical components.

Objective: 
- Identify which company has a higher probability of growth over the next 5-10 years, focusing on product segments and geographies.
- Determine which company exhibits superior profitability and margin profiles linked explicitly to product segments and geographies.

Inputs:
- Peers: {Company A}, {Company B}
- Industry: {Industry}
- Currency: {Currency} (state FX basis if converted)

Data Collection:
- Fetch relevant information from web sources including:
  - Company websites (investor relations sections)
  - BSE/NSE and SEBI databases for filings (annual reports, quarterly results, disclosures)
  - Earnings call transcripts from company IR pages or Indian financial platforms like Moneycontrol, Business Standard
  - Analyst reports from Indian brokerage firms (e.g., HDFC Securities, ICICI Direct, Motilal Oswal) or global firms
  - Industry reports from Indian rating agencies (CRISIL, ICRA, CARE) or global sources adapted to Indian context
  - Regulatory databases (e.g., SEBI, RBI, MCA for corporate filings)
- Use search queries to locate the most recent and relevant documents (e.g., "{Company A} annual report FY2024", "{Company B} earnings presentation Q3 FY2025")
- Prioritize primary sources and verify dates; use current date as reference for recency.
- Extract key data on financials, product segments, geographies, competitive positioning, risks, and growth drivers.

Source Policy: 
Utilize primary/high-signal sources such as audited reports, investor decks, earnings call transcripts, regulator databases, and expert market research. Append sources to each exhibit as: [Source: Title — URL — Doc date]. Use “ND” for missing data and tag inferences with brief logic. Apply ISO date format.

Normalization: 
Standardize product and region labels across companies. Align channel terms. Use reporting currency; note FX basis for conversions.

Output Format: 
Generate the report in structured Markdown format suitable for saving as a .md file. Include tables first, followed by short narratives per exhibit: Context → Insight → Implication → KPI, with direct A-vs-B comparisons throughout.

1. Executive Summary
   - Growth call: Declare which business has a greater growth probability based on product × geography, including 2–3 factual reasons.
   - Profitability call: State which business has better margin/earnings quality, tied to specific segments and geographies.
   - Identify 3 growth drivers explaining future growth odds.
   - Highlight 3 vulnerabilities that might flip growth margins.
   - Provide a Segment–Geography scorecard (0–5).
   - Outline 3 business KPIs for the next 12–24 months.

2. SECTION A — Top Cells: Analyze top products by country.
3. SECTION B — Price Control &amp; Route-to-Market: Assess net price realization efficiency.
4. SECTION C — Supply Resilience: Evaluate supply sourcing and continuity.
5. SECTION D — Segment Growth Engines: Examine growth drivers and profitability.
6. SECTION E — Product &amp; Geography Overview: Contextualize product and geographical analysis.
7. SECTION F — Competitive Landscape: Scrutinize competitive positioning.
8. SECTION G — Risks by Segment: Map potential risks.
9. SECTION H — Causal Diagnosis &amp; Decision: Compare causal disparities and suggest KPI-driven actions.

Quality Checks:
- Ensure explicit A vs B contrasts.
- Normalize labels and currencies.
- End each exhibit with Context → Insight → Implication → KPI, and a source tag.
- Apply the 80/20 filter to prioritize impactful segments.