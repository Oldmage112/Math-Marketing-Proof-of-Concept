# Textbook Topic Map

Maps the six content pillars from `01_Brand_Voice/Math_Content_Brand_Voice_Guide.md`
(Section 5) to the specific textbooks and chapters in `Textbooks/` that can fact-check a
post. Use this to find where to verify a claim before publishing — not as a source to
quote from directly (see the license note at the bottom).

All five textbooks are OpenStax (Rice University), so chapter/section numbers below are
stable and citable, e.g. "Calculus Volume 1, §2.2."

## 1. Numbers & Patterns
- **College Algebra 2e** — Ch. 1 (Real Numbers, Radicals, Polynomials), Ch. 5 (Power &
  Polynomial Functions), Ch. 6 (Exponential & Logarithmic Functions) for number-behavior
  claims (growth rates, exponents, roots).
- **Principles of Data Science** — §3.1–3.5 (Measures of Center/Variation, Probability
  Theory) for claims about numeric patterns in data.
- *Best for:* prime/Fibonacci-adjacent number behavior, exponential growth claims,
  probability-flavored number curiosities.

## 2. Geometry & Symmetry
- **Calculus Volume 1** — Ch. 1.3 (Trigonometric Functions), Ch. 6 (Areas, Volumes,
  Arc Length — useful for golden-ratio/spiral and solid-geometry claims that involve
  measurement).
- **College Algebra 2e** — Ch. 2.1 (Rectangular Coordinate Systems and Graphs) for
  coordinate/graph-based geometry claims.
- *Gap:* none of the five textbooks is a dedicated geometry text — classical
  theorem/proof claims (Pythagorean theorem variants, Platonic solids, tessellations)
  should be checked against a primary geometry reference, not just these. Flagged in
  `GAPS_AND_OPEN_ITEMS.md`.

## 3. History & Mathematicians
- **No source in this repo covers this pillar.** All five textbooks are modern OpenStax
  instructional texts with essentially no historical/biographical content. This is a real
  gap, not just a thin one — flagged in `GAPS_AND_OPEN_ITEMS.md` with suggested sources
  (e.g. MacTutor History of Mathematics archive, Britannica) to add before publishing
  history-pillar content.

## 4. Math in Nature
- **Calculus Volume 1** — Ch. 3.4 (Derivatives as Rates of Change), Ch. 4 (Applied
  Optimization) for claims framed as "nature optimizes" (honeycombs, growth curves).
- **02_Visual_Assets** — the Fractals & Self-Similar Patterns and Fractal Zoom & Growth
  Animations categories are the strongest asset match for this pillar even though no
  textbook here directly covers fractal math in nature.
- *Gap:* no dedicated popular-science source for nature claims (phyllotaxis, shell
  spirals, coastlines). Flagged alongside the history gap — these are the two pillars
  most likely to need an outside source before a fact-check pass.

## 5. Paradoxes & Mind-Benders
- **Introductory Statistics 2e** / **Introductory Business Statistics 2e** — Ch. 3
  (Probability Topics, Independent & Mutually Exclusive Events) covers the groundwork
  for Monty Hall–style conditional-probability paradoxes.
- **Principles of Data Science** — §3.4–3.5 (Probability Theory, Distributions) for
  probability paradox claims.
- *Gap:* Zeno's paradox and infinite-set paradoxes (different sizes of infinity) are not
  covered in any of these five texts — they're calculus/set-theory-adjacent but not
  actually in Calculus Volume 1's table of contents. Verify externally.

## 6. Everyday Math Magic
- **Introductory Business Statistics 2e** — full text, especially Ch. 2 (Display/Measures
  of Data) and Ch. 8–10 (confidence intervals, hypothesis testing) for real-world/business
  claims.
- **Principles of Data Science** — Ch. 6–7 (Machine Learning, Neural Networks) for
  everyday-AI claims, Ch. 9 (Data Visualization) for chart/graph claims.
- **College Algebra 2e** — Ch. 4.2–4.3 (Modeling with Linear Functions) for real-world
  modeling claims (finance, music, architecture ratios).

---

## License note — read before quoting or reproducing textbook content
All five OpenStax textbooks in `Textbooks/` are licensed **CC BY-NC-SA 4.0**
(Attribution, NonCommercial, ShareAlike). That license permits using them freely to
**verify facts and figures for original writing** — the underlying facts and ideas
aren't copyrightable — but it does **not** clear you to reproduce their text verbatim,
lift their diagrams, or otherwise redistribute textbook content if this account's
output is used commercially (sponsorships, paid promotion, monetized platforms). Have
whoever owns the compliance gate confirm this is fine given how the account is
monetized, tracked alongside the image licensing question in
`05_Compliance/Compliance_Notes.md`.
