# Reference Folder

Video data that feeds the concept engine. Drop JSONs here — Claude extracts the rules.

## Folders
- `our-content/` — Our own well-performing videos (JSON per video)
- `competition/` — Competitor videos worth studying (JSON per video)
- `viral-reference-library.md` — Decoded viral mechanics (text format)

## How to Use
1. After a video performs well, create a JSON in `our-content/` using `template.json`
2. When you spot a competitor video worth studying, create a JSON in `competition/` using `template.json`
3. Before generating new concepts, Claude reads ALL JSONs and extracts patterns

## JSON Extraction Rules (for Claude)

When reading these JSONs before concept generation, extract and apply:

### From Our Content (`our-content/*.json`)

**WINNING PATTERNS — repeat these:**
1. **Hook types that got highest share rates** → Use these hook types more
2. **Emotions that triggered DMs/shares** → Lead with these emotions
3. **Bangalore locations/pain points that performed** → Reuse these locations
4. **Video durations with best watch-through** → Target this duration
5. **First-frame patterns with highest reach** → Replicate these thumbnails
6. **CTAs that generated most DMs** → Use this CTA structure
7. **Comments that repeated** → These are the audience's language — use their words

**LOSING PATTERNS — avoid these:**
1. **Hook types with low share rate** → Deprioritize
2. **Durations with drop-off** → Shorten or restructure
3. **Topics with low non-follower reach** → Not cold-audience friendly
4. **What didn't work notes** → Never repeat

### From Competition (`competition/*.json`)

**STEAL (adapt for Next.BLR):**
1. **Viral mechanics that work in adjacent niches** → Adapt hook to Bangalore e-cycle context
2. **Format structures with high share rates** → Copy the structure, change the content
3. **Emotion levers proven to work** → Apply to our TG (urban Bangalore 22-35)
4. **Hook techniques scoring viral** → Map to our 4-layer hook system

**FILTER (don't blindly copy):**
1. **Skip anything that doesn't pass Bangalore specificity test** — If it can't be made Bangalore-specific, skip
2. **Skip anything targeting wrong TG** — Our TG is urban, 22-35, techie. Not rural, not 40+
3. **Skip production styles we can't replicate** — We shoot at BCH store with iPhone
4. **Skip anything that violates our global rules** — Check against `rules/global-rules.md`

### Pattern Extraction Output

After reading all JSONs, Claude should mentally build:
- **Top 3 hook types by share rate** (from our data)
- **Top 3 emotions by DM conversion** (from our data)
- **Top 3 formats to steal** (from competition)
- **Top 3 things to NEVER do again** (from our failures)
- **Bangalore triggers that are proven** (from our data)

These patterns feed directly into concept generation Step 2.
