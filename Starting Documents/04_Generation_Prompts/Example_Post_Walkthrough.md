# Worked Example: `MASTER_PROMPT_TEMPLATE.md` End to End

This shows one full pass through the master template, so you can see what "grounded in
the reference repo" actually looks like in practice before running it on a new topic.

## Inputs used

- `{{PILLAR}}` = Numbers & Patterns
- `{{TOPIC}}` = "Add any two consecutive triangular numbers and you get a perfect square"
- `{{PLATFORM}}` = static/carousel post
- `{{IMAGE_TOOL}}` = Midjourney

## What the LLM found when it followed the grounding steps

- **Voice guide:** this exact fact already appears as a "Say…" example in Section 4 of
  `Math_Content_Brand_Voice_Guide.md` — a useful calibration anchor, but the caption
  below shouldn't just repeat that line verbatim, it should build the full four-beat
  structure around it.
- **Textbook grounding:** `Textbook_Topic_Map.md` points Numbers & Patterns claims to
  College Algebra 2e. Chapter 9 ("Sequences, Probability, and Counting Theory"), §9.2
  (Arithmetic Sequences) and §9.4 (Series and Their Notations) cover the arithmetic-series
  sum formula that proves this fact — triangular numbers are partial sums of 1+2+3+…+n.
  Note: the textbook doesn't use the term "triangular number" itself, so the citation is
  to the underlying formula, not a verbatim definition.
- **Visual asset:** `Asset_Manifest.csv` doesn't have a purpose-built "triangular numbers
  as a dot triangle" diagram. The closest legitimate match is `Pascal's Triangle rows
  0-16.svg` (Number Patterns category) — triangular numbers are the third diagonal of
  Pascal's Triangle, so it's a real connection, not a stretch. Its `compliance_status` in
  `License_Attribution_Tracker.csv` is `Not Reviewed`, so the image prompt below flags it
  rather than treating it as cleared.

---

## Output 1: Text-generation prompt (produced by the LLM)

> Write one static/carousel caption for a math-facts account. Follow this exact
> four-beat structure — Hook, Fact, Illumination, Close — one beat per slide is fine if
> the platform supports it.
>
> Voice: elegant, precise, awestruck, unhurried. Composed, not loud; reverent, not
> cutesy; trusts the reader's intelligence. Never open with "Did you know?!" or
> similar engagement-bait. Maximum one exclamation point in the whole caption. Zero or
> one emoji, and only if it's mathematically relevant (π, ∞, °, φ) — default to zero.
> Spell out numbers zero through nine in prose; use numerals for ten and up and for any
> value inside an equation.
>
> Fact to build around: add any two consecutive triangular numbers (1, 3, 6, 10, 15…)
> and the sum is always a perfect square. Ground this in the arithmetic-series sum
> formula (this is provable, not a curiosity — cite it as such, don't hedge with "some
> say").
>
> The Close should land quietly — a reflective line or related thought, not a
> "LIKE AND FOLLOW" style call to action.
>
> Before finalizing, check the draft against these calibration pairs and revise if it
> reads closer to the left column:
> "You won't BELIEVE what happens when you add these numbers 🤯" → "Add any two
> consecutive triangular numbers, and something exact happens: you get a perfect
> square."
> "Fun fact: pi is infinite!!" → "π never repeats, never ends, and yet is exact."

## Output 2: Image-generation prompt (produced by the LLM, for Midjourney)

> A single elegant hero diagram illustrating triangular numbers building into a perfect
> square — two triangular arrangements of dots (e.g. the 3rd and 4th triangular numbers)
> fitting together into one square grid of dots. Minimalist geometric line-art style,
> generous negative space, dots and thin construction lines only — no clutter, no
> background texture.
>
> Palette: neon colors, cold off-white dots/lines, one restrained
> accent color reserved for the square outline where the two triangles meet.
>
> Skip this instruction for now, adding it in for later: Do not render any text/numerals in the image itself — captions and equations will be added as a post-production overlay in FreeSans, per the brand type system.
>
> Compositional reference (inspiration, not a source to reproduce): `Pascal's Triangle
> rows 0-16.svg` from the reference library — the third diagonal of Pascal's Triangle is
> the triangular number sequence, which is the mathematical link between this image and
> that asset.
>
> --ar 4:5 --style raw --v 6
