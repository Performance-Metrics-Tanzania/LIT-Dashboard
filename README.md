# LIT Dashboard Test

This repository contains:

- `updatedmap.html` — the dashboard HTML page.
- `LIT schools summary.xlsx` — the Excel workbook used as the data source.

## HTML / XLSX link

`updatedmap.html` now loads `LIT schools summary.xlsx` from the same folder using the browser-side SheetJS library.

- The page fetches `LIT schools summary.xlsx` when it loads.
- It parses the workbook and lists available sheet names.
- It renders the selected sheet as a table and shows a summary of row/column counts.
- If you update the workbook file and then reload the page, the dashboard will display the new data.

## How it works

The dashboard uses these steps:

1. Fetch `LIT schools summary.xlsx` from the repo folder.
2. Convert the workbook binary into a JavaScript workbook object with SheetJS.
3. Read the selected sheet and convert it into an array of rows.
4. Render the rows as HTML in the browser.

## Notes

- Opening the page via `file:///` may block workbook loading in some browsers.
- Use GitHub Pages or a local HTTP server to ensure the workbook fetch works correctly.
- You can also select a local workbook file manually using the file picker.

## Next step

If you want, I can also add a small chart view or map view that uses the workbook data directly instead of just displaying it as a table.
