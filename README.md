# Android Build QA Report Generator

A single-file, no-install tool for building Android build QA status reports (defect matrix, defects summary, testing devices, etc.) and copying them straight into a Gmail compose window with formatting intact.

## What it does

- Builds a full QA status report matching the standard email format: header banner, defect matrix, Open Project link, defects summary table, Firebase link + screenshots, optional Bug/Story relation table, testlink screenshot, testing devices, and sign-off.
- Two statuses: **In progress** (no test execution screenshot) or **Completed** (includes one).
- Defect matrix (Priority × Bug Type × Bugs/Suggestions, with totals) is **calculated automatically** from your defect list — no manual counting.
- Defects come from a **CSV upload** (flexible column matching — "Bug ID", "Ticket", "ID" all map correctly) or manual paste/edit in an on-screen table.
- Optional **Bug/Story relation count** table — copy a range straight out of Google Sheets and paste it in.
- One click **"Copy report for Gmail"** — copies the finished report as real HTML (tables, colors, images) so pasting into Gmail keeps formatting.

## How to use it

1. Open the tool (see link above, or just open `qa-report-generator.html` in any browser).
2. Fill in build version, short label, and status.
3. Paste your Open Project and Firebase links (there's a "click here" example link in the form showing the expected URL format).
4. Upload your defects CSV, or add/edit rows directly in the table.
5. Upload any screenshots (Firebase, test execution).
6. Click **Generate report**.
7. Click **Copy report for Gmail**, then paste into a new Gmail compose window.

## Notes

- Everything runs client-side in your browser — no data is uploaded anywhere, no backend, no accounts.
- Works fully offline once loaded; just double-click the HTML file to open it locally if you don't want to use the hosted version.
- Testing devices default to a fixed list (IQOO Z9 5G, Iqoo Z6, Realme 10 Pro Plus, Moto g32, Realme GT 2) but are editable per-report.
