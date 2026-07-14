# Worked Example: `MASTER_PROMPT_TEMPLATE.md` End to End — Math Meltdown

This uses the **exact same topic, fact, and reference asset** as the source repo's
worked example (`Starting Documents/04_Generation_Prompts/Example_Post_Walkthrough.md`),
run through the Math Meltdown voice instead. Same input, same grounding material,
deliberately different output — that's the whole point of this V2 build. Read the two
side by side.

## Inputs used

- `{{PILLAR}}` = Number Chaos
- `{{TOPIC}}` = "Add any two consecutive triangular numbers and you get a perfect square"
- `{{PLATFORM}}` = static/carousel post
- `{{IMAGE_TOOL}}` = Midjourney

## What the LLM found when it followed the grounding steps

- **Voice guide:** this exact fact appears as the top row of the "Before & After" table
  in Section 4 of `Math_Content_Brand_Voice_Guide.md` — here it's the *elegant* version
  that's now the "Instead of" column, since this brand's calibration table runs in
  reverse. The chaotic target version in that table is the calibration anchor for the
  caption below.
- **Textbook grounding:** identical to the source repo — `Textbook_Topic_Map.md` points
  Number Chaos (= Numbers & Patterns) claims to College Algebra 2e, Chapter 9
  ("Sequences, Probability, and Counting Theory"), §9.2 (Arithmetic Sequences) and §9.4
  (Series and Their Notations), which cover the arithmetic-series sum formula that
  proves this fact. The textbook doesn't use the term "triangular number" itself, so the
  citation is to the underlying formula — this doesn't change with the tone.
- **Visual asset:** same match as the source repo — `Pascal's Triangle rows 0-16.svg`
  (Number Patterns category), since triangular numbers are the third diagonal of
  Pascal's Triangle. `compliance_status` in `License_Attribution_Tracker.csv` is
  `Not Reviewed`, so it's flagged below exactly as it is in the source repo's example —
  compliance flags don't get relaxed for a louder brand either.

---

## Output 1: Text-generation prompt (produced by the LLM)

> Write one static/carousel caption for Math Meltdown. Follow this exact four-beat
> structure — Bait, Drop, Freakout, Outro — one beat per slide is fine if the platform
> supports it.
>
> Voice: loud, chaotic, unhinged (affectionately). Meme-heavy, sarcastic, high-momentum
> — the opposite of composed or reverent. Open with maximum hype, caps for emphasis
> welcome. No cap on exclamation points. Two to five emoji, mixing reaction emoji with
> one topic-relevant symbol. Numerals always, even for small numbers — never spell out
> "three" as a word.
>
> Fact to build around: add any two consecutive triangular numbers (1, 3, 6, 10, 15…)
> and the sum is always a perfect square. Ground this in the arithmetic-series sum
> formula (this is provable, not a curiosity — cite it as such even at full hype, don't
> hedge with "some say").
>
> The Outro should land with momentum, not a quiet fade — a "wait for part two" or
> "follow for more" style call-out fits this brand and is encouraged here.
>
> Before finalizing, check the draft against these calibration pairs and revise if it
> reads closer to the left column (i.e., if it sounds composed and quiet instead of
> loud):
> "Add any two consecutive triangular numbers, and something exact happens: you get a
> perfect square." → "OK WAIT. Take any two triangular numbers next to each other. ADD
> THEM. It's a perfect square. EVERY. SINGLE. TIME. 🤯🔺➕🔺"
> "π never repeats, never ends, and yet is exact." → "π has been running forever, never
> repeats ONCE, and somehow every circle in the universe is still obsessed with it. Make
> it make sense 😵‍💫♾️"

## Output 2: Image-generation prompt (produced by the LLM, for Midjourney)

> A hero diagram of triangular numbers building into a perfect square — two triangular
> arrangements of dots (e.g. the 3rd and 4th triangular numbers) fitting together into
> one square grid of dots — but treated as a loud, maximalist graphic, not a minimal
> diagram: bold black outline around each dot cluster, a hard drop shadow, and the frame
> filled edge to edge rather than floating in negative space.
>
> Palette: hot pink and acid yellow dots on an electric blue and pure black background —
> maximum contrast, no restraint. *(This palette is a suggested default, not yet
> confirmed brand palette — see Section 8 of the voice guide, same open-decision status
> as the source brand's palette.)*
>
> Leave room in the composition for a big bold caption treatment — captions and
> equations will be added as a post-production overlay in Styrofoam Feelings (hook
> text) and Paraaminobenzoic (numerals), per the brand type system in Section 8.
>
> Compositional reference (inspiration, not a source to reproduce): `Pascal's Triangle
> rows 0-16.svg` from the reference library — the third diagonal of Pascal's Triangle is
> the triangular number sequence, which is the mathematical link between this image and
> that asset. **Compliance status: Not Reviewed — confirm license clearance before this
> asset (or a close derivative of it) is used in anything published.**
>
> --ar 4:5 --style raw --v 6 --stylize 750

---

## Side-by-side takeaway
Same fact, same textbook citation, same reference asset, same compliance flag — the only
thing that changed between this output and the source repo's is what flowed through
`01_Brand_Voice/Math_Content_Brand_Voice_Guide.md`. That's the confirmation this V2 build
was made to produce: the brand-voice and prompt-template layer is what's actually doing
the work, not the underlying source material.
