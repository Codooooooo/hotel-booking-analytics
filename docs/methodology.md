# Methodology and limitations

The original Alteryx workflows select, transform, summarize, join, and deduplicate hotel booking data. Their business rules are preserved; local absolute file paths are replaced with paths relative to workflows/.

- `Booking.yxmd`: booking preparation, derived checkout date, joins, sorting and deduplication.
- `CustomerProfile.yxmd`: profile preparation and aggregation. Its Customer_ID is constructed from repeated-guest status and reservation-status date. It is not a unique person identifier; do not interpret counts as distinct guests.
- `MarketSegments.yxmd`: market-segment descriptions and summaries. The supplied workflow has no CSV output tool; MarketSegments.csv is a supplied snapshot.

The original checkout-date formula adds stay duration to reservation_status_date. This is not guaranteed to be the arrival date, so the derived CheckOut_Date is not a validated actual checkout date.

The top-level and Power BI CustomerProfile.csv files differ and are both preserved in separate folders. Use the data/powerbi/ snapshots when reconnecting the existing report. Regenerating top-level workflow outputs does not automatically update these snapshots.

The Power BI report contains ALL and Trend 1-5 pages. They cover monthly stay nights, lead time versus ADR by cancellation status, stay nights by customer type, cancellation share with deposit filters, and market-segment ADR versus canceled bookings. Visual definitions were inspected from the PBIX package; no report was rendered or refreshed in Power BI. Avoid causal claims or numerical findings without validating the model and aggregations.

The original source URL, license, and geographic provenance were not supplied. The filename and schema resemble commonly distributed hotel booking demand datasets, but this is not verified provenance and the data must not be described as Thailand-specific. No external-data license or open-source license is inferred.
