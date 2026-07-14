# Gaps & Open Items

Everything below is either a decision that needs a person, or a real content/asset gap
found while restructuring this repo. Nothing here was silently filled in — this is the
punch list.


## Real content gaps found

1. **Half the content pillars have little or no matching visual asset library.** The
   100-item asset library was built around 10 Commons-scraping categories that map
   cleanly onto only 2–3 of the 6 content pillars in the voice guide:
   - Numbers & Patterns — well covered (Number Patterns category).
   - Geometry & Symmetry — well covered (3D Solids, Classical Theorems, Fractals).
   - Math in Nature — partially covered (Fractals categories overlap loosely; nothing
     depicting phyllotaxis, shells, coastlines directly).
   - **History & Mathematicians — no matching assets at all.** No portraits, period
     diagrams, or historical illustrations in the library.
   - **Paradoxes & Mind-Benders — no matching assets at all.** No Monty Hall, Zeno,
     infinite-set, or similar diagrams.
   - **Everyday Math Magic — no matching assets at all.** No music/art/architecture/
     daily-life diagrams.

   Practical effect: three of six pillars currently have to rely entirely on
   generated (not reference-grounded) imagery. Worth a second sourcing pass targeting
   these three pillars specifically, using the same Commons-catalog-then-batch-download
   workflow already built (`02_Visual_Assets/Images_and_Animations/download_commons_assets.py`).

2. **No source material for the History & Mathematicians pillar at all.** All five
   textbooks are modern OpenStax instructional texts with no historical/biographical
   content. Any post in this pillar currently can't be fact-checked against anything in
   this repo. Suggest adding a source before publishing this pillar — e.g. the MacTutor
   History of Mathematics archive (University of St Andrews) or a comparable
   peer-reviewed history-of-math reference.

3. **Thin source material for Math in Nature.** No dedicated popular-science source for
   nature claims (phyllotaxis, shell spirals, honeycomb geometry). Calculus Volume 1's
   optimization chapters can support "nature optimizes" framing, but nothing here
   verifies the specific natural-world claims themselves.

4. **One visual asset failed to download.** `All Platonic solids & Some Archimedean
   solids.jpg` (3D Geometric Solids category) 404'd on Commons — the file may have been
   renamed or removed since the catalog was built. A web search surfaced two candidate
   replacements that weren't independently verified: `File:Archimedian_Solids_15.jpg`
   and a file titled "Archimedean and platonic solids png.png," both in
   Commons category "Sets of all Archimedean solids." Verify and add manually, or leave
   the category at 9/10 items.

5. **No alt-text / accessibility guidance.** The voice guide covers caption tone
   thoroughly but says nothing about image alt-text, which most platforms require
   separately from the caption. Worth a short addition to Section 6 or 8 if
   accessibility compliance matters for this account.

6. **No posting cadence / content calendar.** The voice guide defines pillars and
    structure but not frequency (how often, what mix across pillars/platforms over time).
    Not strictly a reference-material gap, but worth having before this scales past
    one-off generation.

