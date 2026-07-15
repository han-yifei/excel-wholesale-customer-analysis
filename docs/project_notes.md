# Project notes

## Workflow

1. Kept the official CSV unchanged on the `Raw Data` sheet.
2. Linked raw fields into `Clean Data` with cross-sheet formulas.
3. Added readable channel and region labels with lookup tables.
4. Calculated total spend, grocery share, and a median-based value band.
5. Built formula-driven summaries for category, channel, region, and top-customer analysis.
6. Added a channel drop-down, KPI cards, conditional formatting, and native Excel charts.
7. Reconciled workbook totals against the source CSV and scanned for formula errors.

## Reconciliation checks

| Check | Result |
|---|---:|
| Source rows | 440 |
| Total annual spend | 14,619,500 m.u. |
| Average spend per customer | 33,226.14 m.u. |
| Median spend | 27,492 m.u. |
| Horeca customers | 298 |
| Retail customers | 142 |
| Lisbon customers | 77 |
| Oporto customers | 47 |
| Other-region customers | 316 |

## Limitations

- The source is historical and anonymised.
- The dataset contains annual category spending, not dated transactions, revenue, profit, or margin.
- Monetary units are not assigned a currency in the source.
- The median-based value band is a simple descriptive rule and has not been validated as a business segmentation model.
- The workbook supports descriptive analysis only; it is not a forecast.
