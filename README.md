# Hotel Booking Analytics

A coursework portfolio project that prepares hotel booking data with Alteryx and explores booking behavior through an interactive Power BI report.

## Analysis scope

- Monthly weekday and weekend stay patterns.
- Lead time, average daily rate (ADR), and cancellation status.
- Customer-type differences in stay duration.
- Cancellation share and deposit-type filtering.
- Market-segment comparisons of ADR and canceled bookings.

These are the report topics, not independently validated business findings.

## Repository layout

```text
workflows/ Alteryx preparation workflows with relative data paths
reports/   Original Power BI report, renamed for clarity
data/      Supplied source and workflow output CSV snapshots
data/powerbi/ CSV snapshots supplied alongside the Power BI report
docs/      Methodology, data inventory, report inventory, validation
.github/   Issue and pull-request templates
```

## Open the dashboard

1. Install Power BI Desktop on Windows.
2. Open `reports/hotel-booking-dashboard.pbix`.
3. In data source settings or Power Query, replace historical CSV source paths with files under this repository's `data/powerbi/` directory.
4. Review queries and relationships, then refresh and explore the ALL and Trend 1-5 pages.

The binary report is preserved unchanged and may retain original local source paths. It has not been refreshed or visually tested in this environment.

## Open the workflows

Open the `.yxmd` files under `workflows/` in Alteryx Designer. Input/output paths use `../data/` relative to each workflow. The ZIP input references have been changed to the included uncompressed source CSV. Run Booking and CustomerProfile to regenerate their top-level snapshots; the MarketSegments workflow requires an output tool if exporting a new CSV.

## Data and interpretation

Read [methodology and limitations](docs/methodology.md) before interpreting guest counts or derived checkout dates. [Data inventory](docs/data-inventory.json) records row counts and fields; [report inventory](docs/report-inventory.json) records report pages and visual fields.

Source provenance and redistribution rights remain unverified. This repository is initially private. No open-source license is assigned. Original coursework snapshots are retained for traceability; see [validation record](docs/validation.md).
