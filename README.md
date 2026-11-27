# Singapore at NeurIPS 2026

A list of accepted NeurIPS 2026 papers with at least one author from a Singapore institution, filterable by institution and by presentation type (oral, spotlight, poster).

## Files

- `index.html`: the whole site. Settings you might change (the footer date, institution codes and colours) are in the `SITE` block at the top of the script.
- `matched_papers.csv` and `matched_authors.csv`: the data, produced by `filter_by_affiliation.ipynb`.

## Updating the papers

1. Re-run `filter_by_affiliation.ipynb` (for example, after editing `affiliations.csv`).
2. On GitHub, choose **Add file → Upload files** and upload the new `matched_papers.csv` and `matched_authors.csv`. Files with the same names are replaced.
3. Click **Commit changes**. The site updates within a minute or two.

A new institution needs no code change: it gets a code made from its initials and a spare colour. To choose its code and colour yourself, add it to `SITE.institutions` in `index.html`.

## Previewing on your own computer

Browsers won't let a page opened straight from disk read the CSV files, so run a small local server from this folder:

```
python -m http.server
```

Then open http://localhost:8000.

## Sharing a filtered view

Filters are kept in the address, so you can link straight to them, for example `?inst=NUS,NTU&status=oral` or `?q=diffusion`.
