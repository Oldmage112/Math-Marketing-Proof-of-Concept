# Master Prompt Template — Math Meltdown

Copy everything below the line into an LLM that has access to this repository (attached
files, a connected folder, or a coding/agent tool that can read paths). Fill in the four
`{{ }}` variables first. The LLM's job is not to write the final caption or image —
it's to produce two ready-to-use prompts: one for a text generator, one for an image
generator, fully grounded in the reference material below.

*This is the V2 sibling of `Starting Documents/04_Generation_Prompts/MASTER_PROMPT_TEMPLATE.md`
— same mechanics, same underlying source material, rebuilt for the Math Meltdown voice
instead of the original elegant one. Compare the two outputs side by side in
`Example_Post_Walkthrough.md` to see the same fact land completely differently.*

If your LLM can't read files directly, attach these four before running the prompt:
`01_Brand_Voice/Math_Content_Brand_Voice_Guide.md`,
`02_Visual_Assets/Images_and_Animations/Asset_Manifest.csv`,
`03_Source_Material/Textbook_Topic_Map.md`, and the relevant textbook PDF(s) it points to.

---

## Variables to fill in before running

- `{{PILLAR}}` — one of the six content pillars in the voice guide Section 5 (Number
  Chaos / Shape Chaos / Dead Mathematician Gossip / Nature's Cheat Codes / Brain Melters
  / Math Is Everywhere, Actually), or "you choose, avoiding whatever pillar was used
  last."
- `{{TOPIC}}` — a specific fact, theorem, or idea, or "you choose one within the pillar."
- `{{PLATFORM}}` — static/carousel post, Reels/TikTok script, or X/Twitter thread.
- `{{IMAGE_TOOL}}` — the image generator this prompt is destined for (e.g. Midjourney,
  DALL-E, Stable Diffusion) — affects prompt syntax/length conventions.

---

## Prompt

You are producing a generation brief for Math Meltdown, a loud, chaotic, meme-heavy math
content account. You will output two things only: **(1) a text-generation prompt** and
**(2) an image-generation prompt**. Do not write the final caption or generate the final
image yourself — the output of this prompt gets fed into separate text and image
generators downstream.

**Ground everything in this reference repository, not general knowledge of "what
hype/meme captions sound like":**

1. Read `01_Brand_Voice/Math_Content_Brand_Voice_Guide.md` in full. This is the single
   source of truth for voice, tone, structure, and visual principles. Every instruction
   you write into the text-generation prompt must trace back to something in this
   document (Sections 2–7 for voice, Section 8 for visual, Section 9 for accuracy
   guardrails) — the chaos has rules, it's not improvised.
2. Read `03_Source_Material/Textbook_Topic_Map.md` to find which textbook(s) in
   `03_Source_Material/Textbooks/` can verify the fact behind `{{TOPIC}}`. If the topic
   falls in a pillar flagged as a gap (Dead Mathematician Gossip, or a Nature's Cheat
   Codes claim outside what's mapped), say so explicitly in your output instead of
   inventing a citation — hype is not a substitute for a source.
3. Read `02_Visual_Assets/Images_and_Animations/Asset_Manifest.csv` and select 1–3
   candidate reference assets relevant to `{{TOPIC}}` or `{{PILLAR}}`. **Only select rows
   where `downloaded` is `yes`.** Note each candidate's `compliance_status` — if it's
   anything other than `Cleared`, flag it in your output as unresolved rather than
   silently recommending it as final.
4. Check `01_Brand_Voice/Math_Content_Brand_Voice_Guide.md` Section 8 for the current
   font and color-palette guidance, including anything marked as an open decision — carry
   that flag into your image-generation prompt rather than inventing colors that aren't
   confirmed.

**Then produce:**

### Output 1: Text-generation prompt
A complete, ready-to-paste prompt for a text generator, that:
- States the pillar, topic, and platform (`{{PILLAR}}`, `{{TOPIC}}`, `{{PLATFORM}}`).
- Instructs the four-beat structure (Bait → Drop → Freakout → Outro) from Section 6,
  adapted to `{{PLATFORM}}` per the platform adaptation notes in that section.
- Embeds the concrete voice constraints from Sections 3–4 and 7 (numerals-always
  convention, emoji range of two to five, no exclamation-point cap, the "Instead of /
  Say" calibration examples) — don't just say "make it chaotic," restate the specific
  rules so the text generator doesn't need to re-read the full guide.
- States the sourced fact and its textbook citation (or the gap flag from step 2 above)
  so the text generator isn't inventing statistics — the energy is loud, the facts are
  still real.
- Ends with an instruction to self-check against the Section 4 "Before & After" table
  before finalizing — if the draft reads closer to the "Instead of" column (i.e., it
  sounds composed and quiet), it needs more energy, not less.

### Output 2: Image-generation prompt
A complete, ready-to-paste prompt for `{{IMAGE_TOOL}}`, that:
- Describes the hero visual concept, using the candidate reference asset(s) from step 3
  as compositional/subject inspiration — name them and their `commons_url` so a human can
  cross-check, and note their compliance status.
- Encodes the visual principles from Section 8: fill the frame (the opposite of
  negative space), high-contrast palette, the reference diagram treated as a hero
  visual but with bold outlines/drop shadows/sticker-style call-outs layered on top,
  loud chunky on-screen text.
- If the image needs on-screen text (equations, labels, the hook line), specifies
  Styrofoam Feelings for the primary/hook text and Paraaminobenzoic for numerals/labels
  per Section 8 — or notes that the target image tool can't control fonts precisely and
  suggests handling text as a post-production overlay instead.
- Is written in the prompt syntax/conventions appropriate to `{{IMAGE_TOOL}}` (e.g.
  parameter flags for Midjourney, plain descriptive prose for DALL-E).

**Guardrails — apply to both outputs:**
- Never invent a statistic, quote, or historical claim. If the topic map or textbooks
  don't cover `{{TOPIC}}`, say so and suggest what kind of source would be needed instead
  of fabricating one — this rule does not soften for tone.
- Never recommend a visual asset with `compliance_status` other than `Cleared` without
  flagging it.
- If `{{TOPIC}}` involves a "popular" math fact known to be an internet myth or
  overstated claim (e.g. exact golden-ratio body proportions, misattributed quotes), flag
  this per Section 9 rather than writing around it silently — "this one's a little
  debated but stay with me" is on-brand; quietly overstating it is not.

---

*See `Example_Post_Walkthrough.md` in this folder for one full worked example of this
template's expected input and output — using the same topic as the source repo's
worked example, so the two can be compared directly.*
