# HR Attendance Analytics Dashboard (Power BI)

An HR analytics project built on employee attendance data (Apr–Jun 2022, ~99 employees). The dashboard answers two questions HR asked:

1. What are employees' **working preferences** (office vs. work from home)?
2. What is the **sick leave percentage**, and what patterns sit behind it?

## Dashboard Preview

![HR Attendance Dashboard](dashboard_screenshot.png)

📄 [Download full report (PDF)](HR_Dashboard_Report.pdf)

## Tools
Power BI · DAX · Power Query · Excel

## Project files
| File | Description |
|---|---|
| `hr_analysis_ge.pbix` | Power BI report (data model, DAX measures, dashboard) |
| `Attendance-Sheet-2022-2023.xlsx` | Source data: monthly attendance sheets + attendance key |
| `HR_Dashboard_Report.pdf` | Exported PDF of the Power BI dashboard |
| `dashboard_screenshot.png` | Image preview of the dashboard |

## Approach
1. **Data preparation (Power Query):** combined the monthly sheets, unpivoted the date columns, standardized leave codes (P, WFH, SL, PL, LWP, ML, etc.) and handled half-day entries.
2. **Modelling (DAX):** created a measure table with `presence %`, `WFH %` and `SL %`.
3. **Visualization:** KPI cards, trend area charts with trend lines, day-of-week tables, an employee-level table and a month slicer.

## Key insights

| KPI | Value |
|---|---|
| Presence % | 91.83% |
| WFH % | 10.00% |
| Sick leave (SL) % | 1.10% |

**Working preference**
- About 1 in 10 working days is work from home, and the WFH trend line rises over Apr–Jun 2022.
- WFH is highest on **Friday (13.01%)** and **Thursday (11.51%)**, and lowest on Tuesday (8.11%). Presence is correspondingly lowest on Friday (90.19%) and highest on Monday (93.21%).
- A small group of employees works fully remote (100% WFH), while most work mainly from the office.

**Sick leave**
- Overall sick leave is **1.10%**, and its trend line rises slightly over the period.
- **Monday** has the highest sick leave rate (1.62%) and Friday the lowest (0.70%), a pattern HR may want to look into.
- Sick leave is concentrated in a few employees rather than spread evenly.

**Limitation:** the data has no reason-for-leave field, so the analysis shows *when* and *who*, not *why*. The patterns above are starting points for HR follow-up.

## Data notes
- Some employee codes appear for more than one employee name.
- Each monthly sheet has a stray extra date column.

## How to use
Open `hr_analysis_ge.pbix` in Power BI Desktop.
