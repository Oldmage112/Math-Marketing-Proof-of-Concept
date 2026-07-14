# Public Domain / Openly Licensed Math Asset Library

## What this is
100 individually verified, openly licensed math images and animations sourced from
**Wikimedia Commons**, split into two catalogs of 50 each:

1. `Public_Domain_Math_Assets_Catalog.xlsx` — static images, 5 categories × 10:
   3D Geometric Solids · Fractals & Self-Similar Patterns · Classical Theorems & Proof
   Diagrams · Number Patterns (Pascal's Triangle & Golden Ratio) · Equations, Algebra &
   Applied Diagrams.
2. `Public_Domain_Math_Animations_Catalog.xlsx` — GIFs/animations/short video, 5
   categories × 10: Fractal Zoom & Growth Animations · Algorithm & Discrete Math
   Animations · Calculus & Function Animations · Theorem & Geometric Proof Animations ·
   Short Educational Videos (WebM/OGV).

Each row includes the exact file name, a plain-language description, a direct Wikimedia
Commons file URL, and a license note.

## The files are downloaded — start from `Asset_Manifest.csv`, not the raw catalogs
The two `.xlsx` catalogs above are the original sourcing spreadsheets. `download_commons_assets.py`
(a batch fetcher, since binary downloads need a pipeline with open internet access) was
run against both, and the results live in `downloads/<category>/<file name>`.

`Asset_Manifest.csv` in this folder is the merged, current source of truth: it joins both
catalogs with the actual local file path, a `downloaded` status, and a `compliance_status`
column. **99 of 100 assets downloaded successfully.** The one failure —
`All Platonic solids & Some Archimedean solids.jpg` (3D Geometric Solids, 404 on Commons) —
is flagged in `downloads/_download_log.csv` and in `../../GAPS_AND_OPEN_ITEMS.md`, with
candidate replacement leads.

When an LLM or a person needs a reference image, point them at `Asset_Manifest.csv`, not
the raw `.xlsx` files — it's the only file with working local paths.

## ⚠️ Important licensing note for your compliance handoff
"Public domain" and "freely usable" are not the same thing, and Wikimedia Commons hosts
both:

- **True public domain** (no restrictions, no attribution required): only a few items in
  this set qualify outright — e.g. the Fractal Broccoli photo (explicitly dedicated to
  PD by its author) and the Oliver Byrne 1847 Euclid plates (public domain by age).
- **CC BY-SA** (the majority of items): free to use, including commercially, but
  requires **attribution** and, if you modify and redistribute the file itself,
  **share-alike** licensing of that derivative. This is *not* the same as public domain.
- Every "verify version on file page" note means the exact CC BY-SA version (3.0 vs 4.0)
  or a dual-license option wasn't fully confirmed in the original sourcing pass — click
  through to the Commons file page before use.

Treat this library as a **sourcing shortlist**, not a pre-cleared asset list. Compliance
sign-off per item now has a dedicated tracker: `../../05_Compliance/License_Attribution_Tracker.csv`
— every row currently reads "Not Reviewed" and needs an owner.

## Files in this folder
- `Asset_Manifest.csv` — merged catalog + local path + status, the file to reference for actual use
- `Public_Domain_Math_Assets_Catalog.xlsx` — original 50-item image sourcing catalog
- `Public_Domain_Math_Animations_Catalog.xlsx` — original 50-item animation/video sourcing catalog
- `downloads/` — the actual media files, organized by category
- `download_commons_assets.py` / `.ipynb` — the batch-fetch script (re-run to retry the 1 failure or pull new catalog rows)
- `README.md` — this file
