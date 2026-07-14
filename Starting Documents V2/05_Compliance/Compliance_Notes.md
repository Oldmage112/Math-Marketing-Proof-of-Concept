# Compliance Notes

This folder exists because two source materials in this repo carry licensing conditions
that need a human sign-off before content goes live. Nothing here has been cleared yet —
that's a deliberate default, not an oversight.

## 1. Visual assets — `License_Attribution_Tracker.csv`
100 images/animations sourced from Wikimedia Commons (`02_Visual_Assets/Images_and_Animations/`).
Licenses split roughly into:
- **True public domain** — a small minority, no attribution required.
- **CC BY-SA** — the majority. Free to use commercially, but requires attribution, and
  share-alike terms apply if the file itself is modified and redistributed.
- Several rows are marked "verify version on file page" — the exact license version
  (3.0 vs 4.0) wasn't confirmed down to the specific sub-version during sourcing.

Every row in the tracker currently reads **cleared_status: Not Reviewed**. Assign an
owner to work through it — realistically per-category rather than per-file, since
license patterns tend to be consistent within a category (per the original sourcing
notes in `02_Visual_Assets/Images_and_Animations/README.md`).

## 2. Reference textbooks — CC BY-NC-SA 4.0
All five OpenStax textbooks in `03_Source_Material/Textbooks/` are licensed
**CC BY-NC-SA 4.0** — NonCommercial. They're safe to use for fact-checking (facts and
ideas aren't copyrightable), but not safe to quote verbatim or reproduce diagrams from if
this account's output is monetized in any way that would count as "commercial" under the
license. Confirm how the account is monetized (ads, sponsorships, paid placement) and
decide whether that triggers the NC restriction before textbook content is quoted
directly anywhere. See `03_Source_Material/Textbook_Topic_Map.md` for the full note.

## 3. Fonts — provenance unverified, needs review
`02_Visual_Assets/Fonts/` currently contains two files, `Paraaminobenzoic.otf` and
`Styrofoam Feelings.otf`, referenced in `01_Brand_Voice/Math_Content_Brand_Voice_Guide.md`
Section 8. No license file (no `COPYING`, `AUTHORS`, or equivalent) ships alongside
either file in this folder, so their license terms can't be confirmed from what's in the
repo. Don't assume these are cleared for commercial use — track them in
`License_Attribution_Tracker.csv` or an equivalent font-specific log until someone
confirms the source and license of each file.

## Suggested workflow
1. Assign an owner for `License_Attribution_Tracker.csv`.
2. Work category-by-category (10 files each), confirming license version on the Commons
   file page and filling `attribution_text_drafted` with the exact credit line to use.
3. Mark `cleared_status` as `Cleared`, `Cleared with attribution`, or `Rejected — do not
   use`, with `reviewed_by` and `review_date` filled in.
4. Anything still `Not Reviewed` should not be pulled into a generation prompt — the
   `04_Generation_Prompts/MASTER_PROMPT_TEMPLATE.md` instructs the LLM to check this
   column and flag uncleared assets rather than silently using them.
