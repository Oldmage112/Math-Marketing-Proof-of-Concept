# Math Meltdown — Reference Repository (V2 / Proof-of-Concept Sibling)

Reference material for an AI-generated math content account (captions, scripts, and
diagram/image prompts). This file is the entry point — read this first, whether you're
a person orienting in the repo or an LLM being pointed at it for a generation task.

**This is a deliberate contrast build.** It mirrors `Starting Documents/` file for file
— same folder structure, same source textbooks, same image library, same font files —
but with a completely different brand voice, aesthetic, and content framing. It exists
to confirm that swapping the brand-voice and prompt-template layer actually changes the
generated output, using identical raw material as the control. See
`01_Brand_Voice/Math_Content_Brand_Voice_Guide.md` for the full contrast, or
`04_Generation_Prompts/Example_Post_Walkthrough.md` for the same fact run through both
brands side by side.

## If you just want to generate a post
Go straight to `04_Generation_Prompts/MASTER_PROMPT_TEMPLATE.md`. It's a ready-to-paste
prompt that pulls together everything else in this repo — you shouldn't need to read the
rest of this file for a single generation task.

## Folder map

| Folder | What's in it | Use it for |
|---|---|---|
| `01_Brand_Voice/` | The Math Meltdown brand & voice guideline doc — loud, chaotic tone, structure, content pillars, visual/type system, accuracy rules | The single source of truth for how anything written or designed should sound and look |
| `02_Visual_Assets/` | The same 100 catalogued public-domain/CC-licensed math diagrams & animations as the source repo, plus the same two font files, reassigned to different roles | Reference imagery and typography for image-generation prompts |
| `03_Source_Material/` | The same 5 OpenStax math/stats/data-science textbooks + topic map as the source repo | Fact-checking claims before they go into a caption — accuracy standards don't change just because the tone did |
| `04_Generation_Prompts/` | The master prompt template + one worked example, rebuilt for the Math Meltdown voice | The actual generation workflow — start here for day-to-day use |
| `05_Compliance/` | License/attribution tracker + notes (same underlying assets as the source repo) | Sign-off tracking before any asset or textbook content is used in something published |

## How the pieces connect

A generation task should touch all four reference folders, in this order:

1. **Voice** (`01_Brand_Voice`) — what pillar, what tone, what structure.
2. **Facts** (`03_Source_Material`) — verify the claim, or flag that it can't be verified
   against what's in this repo.
3. **Visuals** (`02_Visual_Assets`) — find a grounded reference image/diagram, or note
   that none exists for this topic.
4. **Compliance** (`05_Compliance`) — check whether anything selected in steps 2–3 is
   actually cleared to use.

`MASTER_PROMPT_TEMPLATE.md` encodes exactly this sequence so you don't have to hold it in
your head each time — same sequence as the source repo, proving the workflow itself is
brand-agnostic even though the output isn't.

## Known gaps and open decisions
See `GAPS_AND_OPEN_ITEMS.md` in the repo root. Same underlying gaps as the source repo
(shared asset/textbook library), plus the color palette here is a fresh open decision —
nothing in `05_Compliance/License_Attribution_Tracker.csv` has been reviewed yet either.
