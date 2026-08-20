# Instacart Sales & Customer Insights Dashboard

**Role:** Data Analyst / Business Intelligence Analyst
**Industry:** Retail / Online Grocery
**Tools:** PostgreSQL, SQL, Power BI, Power Query, DAX
**Model:** Star schema (Orders fact table + Products/Aisles/Departments dimensions)
**Analysis type:** Descriptive, diagnostic, and prescriptive

## Executive summary
An end-to-end analytics project combining SQL business-question analysis with an interactive Power BI reporting solution, giving management a consolidated view of Instacart's sales, customers, product performance, profitability, time-based demand, and departmental activity.

**Headline KPIs:** $158.37M total revenue · 1M total orders · 63K total customers · $151.03 average order value

## Business problem
Instacart's high-volume transaction environment made it hard for management to see which departments and products actually drive sales, distinguish high-demand from high-profit areas, understand peak ordering periods for workforce planning, and get consistent, reproducible answers to recurring business questions — rather than relying on assumptions.

## What I did
- Modeled a star schema (Orders as the fact table; Products, Aisles, and Departments as dimensions) in Power Query/Power BI
- Answered 5 core business questions directly in SQL (top departments by revenue, top weekend products, category profitability comparisons, unsold-product detection via LEFT JOIN, and executive KPIs)
- Built two dashboard pages: **Product Performance** (best/worst products, aisle demand vs. profitability) and **Sales Performance** (trend, time-of-day, department quantity), plus an updated Sales page with Year/Quarter filtering
- Created DAX measures for revenue, orders, customers, AOV, and profitability; built a time-of-day classification for workforce analysis

## Key findings
- **Top 5 products** sold within a fairly narrow band (233–267 units) — demand at the top is balanced. **Bottom 5** ranged from just 28–49 units, a 239-unit gap vs. the top seller
- **High demand ≠ high profit:** aisles like Fresh Herbs (10K units, $29K profit) and Frozen Breads/Doughs (10K units, $27K profit) sell well but return comparatively low profit — worth a pricing/cost review
- **High demand AND high profit:** Candy/Chocolate ($0.40M profit, 144K units) and Ice Cream ($0.35M, 127K units) are the strongest categories for both metrics
- **Afternoon dominates ordering** — 497K orders (~47%) vs. just 19K (~2%) in the late night window
- **Personal Care, Snacks, and Pantry** are the top 3 departments by quantity sold (759K / 623K / 507K), together ~1.89M units — vs. just 4K for the lowest (Bulk)
- **Annual quantity sold was remarkably stable (2015–2022)**, holding between ~695K–700K units per year; the lower 2023 figure reflects a partial year (data ends 7 April 2023), not a real demand drop
- **Data-quality flag:** a "Missing" aisle/category label appears as the top high-demand/high-profit group — indicating some products lack a populated category and should be corrected before final decisions

## Recommendations
- Protect stock availability in Personal Care, Snacks, and Pantry — the clear volume leaders
- Review supplier cost/pricing on high-demand, low-profit aisles (e.g. Fresh Herbs, Frozen Breads)
- Align staffing and fulfilment capacity toward the afternoon peak; reassess late-night coverage for cost efficiency
- Promote and protect inventory for high-demand/high-profit aisles like Candy and Ice Cream
- Resolve the "Missing" category data-quality issue before using aisle rankings for decisions
- Review bottom-performing products for placement, pricing, or rationalization
- Use monthly demand patterns (January's peak vs. June's low) for stock planning

## Limitations & future improvements
Findings show association, not confirmed causation. 2023 is a partial year and shouldn't be compared directly to complete prior years — a YTD vs. prior-YTD view would be more appropriate. Profitability analysis would benefit from supplier costs, promotions, and discount data; customer segmentation and predictive forecasting are natural next steps once the "Missing" category issue is resolved.

## Skills demonstrated
SQL (JOINs, LEFT JOIN, GROUP BY, aggregation, CASE logic, NULL analysis) · Power BI (data modeling, relationships, slicers, KPI cards) · Power Query (transformation, nested-table handling) · DAX (measures, time-of-day classification) · descriptive/diagnostic/prescriptive analysis · business problem framing and recommendations

## Files
- [Instacart_Portfolio_Report.docx](./Instacart_Portfolio_Report.docx) — full written case study
- [InstaCart PBI Ikea link.docx](https://github.com/user-attachments/files/31281602/InstaCart.PBI.Ikea.link.docx)
— the Power BI file
- [Sales_dashboard.png](./Sales_dashboard.png) — Sales Performance view (with Year/Quarter filter)
- [Product_dashboard.png](./Product_dashboard.png) — Product Performance view
