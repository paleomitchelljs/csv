# csv

A page for making small CSV files by hand. No install, no account. It runs entirely in the browser, so nothing you type leaves your machine.

Live: https://paleomitchelljs.github.io/csv/

## What it does

Type a name in the box at the top. It gets lowercased, spaces become underscores, and that's the download name (`fossil counts` becomes `fossil_counts.csv`).

Row 1 is the header row and takes any text. Every row under it takes numbers only -- digits, one decimal point, an optional leading minus. Commas are stripped as you type, so a pasted `1,234.50` lands as `1234.50` and won't split a field.

Copy CSV puts the file on your clipboard. Download CSV writes it to disk. Trailing empty rows and columns are dropped from the output, so the extra grid you didn't fill in costs nothing.

Arrow keys and Enter move between cells. Enter on the bottom row adds a row.

## Deploying

One file, `index.html`, no build step and no dependencies. Push to `main`, then Settings > Pages > Deploy from a branch > main / root.
