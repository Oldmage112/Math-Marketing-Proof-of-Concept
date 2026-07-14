# Math Marketing — Reference Repository

Reference material for an AI-generated math content account (captions, scripts, and
diagram/image prompts). This file is the entry point — read this first, whether you're
a person orienting in the repo or an LLM being pointed at it for a generation task.

## If you just want to generate a post
Go straight to `04_Generation_Prompts/MASTER_PROMPT_TEMPLATE.md`. It's a ready-to-paste
prompt that pulls together everything else in this repo — you shouldn't need to read the
rest of this file for a single generation task.

## Folder map

| Folder | What's in it | Use it for |
|---|---|---|
| `01_Brand_Voice/` | The brand & voice guideline doc — tone, structure, content pillars, visual/type system, accuracy rules | The single source of truth for how anything written or designed should sound and look |
| `02_Visual_Assets/` | 100 catalogued public-domain/CC-licensed math diagrams & animations, plus the FreeFont family | Reference imagery and typography for image-generation prompts |
| `03_Source_Material/` | 5 OpenStax math/stats/data-science textbooks + a topic map | Fact-checking claims before they go into a caption |
| `04_Generation_Prompts/` | The master prompt template + one worked example | The actual generation workflow — start here for day-to-day use |
| `05_Compliance/` | License/attribution tracker + notes | Sign-off tracking before any asset or textbook content is used in something published |

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
your head each time.

## Known gaps and open decisions
See `GAPS_AND_OPEN_ITEMS.md` in the repo root. Two are worth knowing about before you
generate anything for real: the brand color palette isn't finalized yet, and nothing in
`05_Compliance/License_Attribution_Tracker.csv` has been reviewed yet.
