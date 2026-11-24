# TaskFlow Recovery: Business Analysis Project

> **Simulated engagement.** TaskFlow is a simulated SaaS product (about 1,500 accounts, January 2023 to December 2025). The data, roles, costs and targets are assumed. No real client, person or quote is represented.

This project follows on from my SQL investigation and Power BI dashboard in [TaskFlow-Analysis](https://github.com/Hai-Anh-Dang/TaskFlow-Analysis). I took that analysis as a starting point and worked on it the way a business analyst would: framing the problem, testing what the evidence can and cannot show, comparing options, and planning delivery with requirements, user stories, tests, risks and decision gates.

## The problem

TaskFlow's recorded renewal receipts fell from AUD 2,653 in June 2025 to AUD 2,084 in December, a drop of 21.5%. Pro subscribers fell from 187 to 144 over the same seven months. Two causes fit the evidence:

- a 50.1% Pro price rise (AUD 9.99 to AUD 14.99) that added only priority support;
- a 2025 redesign that coincided with lower checkout completion and with new workflow and Android sync failures.

## Recommendation

I compared three options: do nothing, fix reliability only, and a phased recovery programme. The phased programme is the strongest, but once staff time is costed its growth case does not pay for itself on current assumptions. In my view, funding the full programme now would be premature.

I recommend approving **Wave 0**, which restates the baselines and confirms what can change. At Gate G0 the sponsor funds the reliability fixes on customer-harm grounds, and funds the growth changes only if they pay. Benefits are reviewed on 31 August and 30 November 2026.

## What to read

| File | What it contains |
|---|---|
| `TaskFlow_Business_Case.docx` | **Start here.** 13-page business case: executive summary, current state with AS-IS/TO-BE processes, objectives, option scoring, capability, POPIT impact, risks, implementation plan, monitoring and conclusion |
| `TaskFlow_Project_Workbook.xlsx` | Delivery workbook: requirements (27), epics (4), user stories (15), acceptance criteria and test cases (56), roadmap, calendar, Gantt chart, traceability matrix, RAID log (25 entries), stakeholders and RACI, KPIs and release rules, delivery approach |
| `03_05_checkout_process_before_asis_tobe.png` | Checkout process before June 2025, as observed since, and as I propose it |
| `process_renewal_asis_tobe.png`, `process_sync_asis_tobe.png` | AS-IS and TO-BE diagrams for renewal and Android sync |

## Present State problem (As-Is)

| Measure | Before | After | Period and definition |
|---|---|---|---|
| Pro price | AUD 9.99 | AUD 14.99 | From 1 March 2025 |
| Monthly cancellation rate | 3.53% | 8.89% | 2024 vs March–December 2025; request date over opening Pro subscribers |
| Checkout completion | 67.9% (305/449) | 26.3% (63/240) | January 2023–May 2025 vs June–December 2025 |
| Workflow failure among resolved attempts | 1.9% (previous interface) | 25.4% (new interface) | 2025 |
| Android v7.0 sync failure | 0% on other platforms | 35.8% (175/489) | July–December 2025 |

Projections in the business case (subscribers, receipts, return on investment) are a model, not observed data.

## Targets if the programme goes ahead

- Monthly cancellations at or below 5.7%
- Checkout completion back to about 59.8%
- Sync failures below 2% and workflow failures below 5%
- Monthly receipts back above the June 2025 peak

## Limits

- All data is synthetic. Cancellation reasons and reviews show patterns, not customer motive.
- Only one global price-notice date is recorded, so the data cannot show who received notice.
- First-upgrade payments are incompletely recorded, so I report recorded renewal receipts, not revenue or profit. There is no cost data.
- The previous interface was not served after June 2025, so old against new is not a controlled comparison.
- Volumes are small (about 34 checkout starts and 10 new Pro subscriptions a month), so tests are directional and benefits can only be judged months after delivery.

## Repository layout

```
TaskFlow_Business_Analyst/
├── README.md
├── TaskFlow_Business_Case.docx      # business case
├── TaskFlow_Project_Workbook.xlsx         # requirements, stories, tests, plan, RAID
├── 03_05_checkout_process_before_asis_tobe.png
├── process_renewal_asis_tobe.png
└── process_sync_asis_tobe.png
```
