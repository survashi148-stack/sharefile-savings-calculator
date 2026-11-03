# ShareFile Savings Calculator (web version)

A browser version of `ShareFile_Savings_Calculator_V2 (.xlsm)`. It uses the same inputs, formulas,
Price Book and Manual Entry lock as the workbook, and **Export to Slides** builds the same
PowerPoint deck: Cover, Summary, Cost Comparison + Talk Track, and Deal slide when a deal price is entered.
The deck is generated in the browser with PptxGenJS, so you don't need Excel or PowerPoint installed.

## Deploy on GitHub Pages
1. Create a repository and upload `index.html` (and this README) to the root.
2. Go to **Settings → Pages → Build and deployment**, set Source to **Deploy from a branch**, then choose `main` and `/ (root)`.
3. After about a minute the site is live at `https://<user-or-org>.github.io/<repo>/`.

> Pages sites on public repos can be seen by anyone who has the link. For internal-only use,
> put the repo in a GitHub Enterprise org and set the Pages visibility to **Private**.

## Updating prices
Open `index.html` and edit the `PRICE_BOOK` block near the top of the `<script>`. All values are $/user/year.
- `esign` matches 'Price Book'!A2:E6
- `fileSharing` matches A9:D26
- `sharefile` matches A29:D32
The Collaboration Tool dropdown (`FS_LIST`) matches the Excel validation range A15:A26.
The Price Book and Pricing Sources tabs show the same data and update automatically.

## Notes
- The page needs internet access once to load the slide library from cdn.jsdelivr.net (pinned to pptxgenjs@3.12.0).
- Inputs are remembered in the browser (localStorage). Use **Clear inputs** to reset.
- The logo is embedded in the page, so there are no other files to host.
