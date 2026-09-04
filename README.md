# csv

A page for making small CSV files by hand. No install, no account. It runs entirely in the browser, so nothing you type leaves your machine.

Live: https://paleomitchelljs.github.io/csv/

## What it does

Type a name in the box at the top. It gets lowercased, spaces become underscores, and that's the download name (`fossil counts` becomes `fossil_counts.csv`).

The top row is labeled *column name* and takes any text, but it is cleaned up on the way out: spaces become underscores and everything that isn't a letter or a numeral -- parentheses, punctuation, accents -- is dropped, so `Mass (g) 2` saves as `Mass_g_2`. The grid keeps what you typed; only the saved file is scrubbed. The numbered rows under it -- 1, 2, 3 and on down -- take numbers only -- digits, one decimal point, an optional leading minus. Commas are stripped as you type, so a pasted `1,234.50` lands as `1234.50` and won't split a field.

Copy CSV puts the file on your clipboard. Download CSV writes it to disk. Trailing empty rows and columns are dropped from the output, so the extra grid you didn't fill in costs nothing.

Arrow keys and Enter move between cells. Enter on the bottom row adds a row.

## Deploying

One file, `index.html`, no build step and no dependencies. Push to `main`, then Settings > Pages > Deploy from a branch > main / root.
