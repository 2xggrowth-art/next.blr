# Reference Folder

Video data that feeds the concept engine. Drop JSONs here — Claude extracts the rules.

## Folders
- `our-content/` — Our own video performance JSONs
- `competition/` — Competitor video analysis JSONs
- `viral-reference-library.md` — Decoded viral mechanics (text format)

## How to Use
1. After a video performs well (or fails), create a JSON in `our-content/` using `template.json`
2. When you spot a competitor video worth studying, create a JSON in `competition/` using `template.json`
3. Before generating new concepts, Claude reads ALL JSONs and extracts patterns

## JSON Structure (10 Sections)

Both folders use the same format:

| Section | What It Captures | Why It Matters |
|---------|-----------------|----------------|
| `content_identity` | Title, archetype, objective, awareness stage | Knows WHAT the content is trying to do |
| `hook_engineering` | First 3 sec visual/audio/text, pattern interrupt type, re-hooks | The scroll-stopping mechanics |
| `story_psychology_flow` | 4-beat structure, emotional arc, dopamine spikes, open loops | Why people STAY watching |
| `visual_dominance_analysis` | Visual anchor, contrast, color psychology, movement frequency | What the EYES track |
| `audio_psychology_layer` | Music type, energy curve, silence usage, audio interrupts | What the EARS feel |
| `cta_conversion_engineering` | CTA type, wording, friction level, urgency, social proof | What makes people ACT |
| `metrics_intelligence` | Views, shares, completion rate, ratios, drop-off points | PROOF of what works |
| `audience_psychological_model` | Core pain, identity desire, trigger type, belief shift | WHO this reaches and WHY |
| `replication_blueprint` | Extracted templates for hook, story, visual, emotional arc, CTA | Ready-to-use FORMULAS |
| `optimization_layer` | 6 scores (hook/retention/emotion/conversion/visual/algorithm) + overall /100 | Objective quality ranking |

## Extraction Rules (for Claude)

### Step 1: Rank All Videos by `optimization_layer.overall_score_100`
Separate into tiers: 80+ (study deeply), 60-79 (note patterns), below 60 (study failures).

### Step 2: From Our Content — Extract WINNING PATTERNS

**Hook patterns (from `hook_engineering`):**
- Which `pattern_interrupt_type` correlates with highest share rates?
- Which `camera_movement` + `frame_density` combos get best completion?
- What `curiosity_gap_created` wording patterns repeat in top performers?
- Where are the `re_hook_points` in videos with 70%+ completion? Use same timing.

**Story patterns (from `story_psychology_flow`):**
- Which `emotional_journey_curve` arcs get highest shares? (Shares = virality)
- Which `retention_mechanisms_used` appear in 80+ score videos?
- What `beat_3_shift_or_reveal` timing works best for our audience?
- Which `dopamine_spike_moments` timestamps correlate with retention spikes?

**Conversion patterns (from `cta_conversion_engineering`):**
- Which `cta_type` generates most DMs?
- What `friction_level` converts best? (Usually Low)
- Does `urgency_mechanism` improve or hurt conversion for our TG?
- What `exact_wording` patterns repeat in highest-converting videos?

**Audience patterns (from `audience_psychological_model`):**
- Which `primary_trigger_type` appears most in top-performing videos?
- Which `belief_shift_created` resonates with our Bangalore TG?
- What `core_pain` + `deep_identity_desire` combos hit hardest?

### Step 3: From Our Content — Extract FAILURE PATTERNS

**From videos scoring below 60:**
- What `hook_engineering.pattern_interrupt_type` DOESN'T work for us?
- What `content_archetype` underperforms for our audience?
- Where is `drop_off_point_estimate_seconds`? What happens right before it?
- What does `biggest_weakness` reveal about systemic problems?

### Step 4: From Competition — Extract STEALABLE MECHANICS

**From `replication_blueprint`:**
- Take `hook_template_extracted` — adapt to Bangalore e-cycle context
- Take `story_structure_template` — swap variables for our product/TG
- Take `emotional_arc_template` — map to our proven emotions
- Check `scalability_score` — only steal formats scoring 7+ scalability
- Check `risk_of_market_fatigue` — skip High fatigue formats

**From `hook_engineering`:**
- Steal `first_3sec_visual` patterns that work in adjacent niches
- Adapt `curiosity_gap_created` to Bangalore-specific pain points

**From `audience_psychological_model`:**
- If their `core_pain` overlaps with ours → their solution format likely works for us
- If their `deep_identity_desire` matches our TG → their emotional arc transfers

### Step 5: Filter Competition Through Our Rules

Before applying any competition pattern, validate:
- Does it pass Bangalore specificity? (Can it name a real location/pain?)
- Does it fit our TG (urban, 22-35, techie)?
- Can we shoot it at BCH store with iPhone?
- Does it violate any of our 34 global rules?
- Does the `content_archetype` align with our proven archetypes?

### Output: Pattern Summary Before Generating

After reading all JSONs, Claude builds:
1. **Top 3 hook formulas** (from `replication_blueprint.hook_template_extracted` of 80+ videos)
2. **Top 3 emotional arcs** (from `story_psychology_flow.emotional_journey_curve` of highest-shared)
3. **Top 3 CTA structures** (from `cta_conversion_engineering` of highest-converting)
4. **Top 3 competition formats to steal** (from competition `replication_blueprint` with 7+ scalability)
5. **Top 3 things to NEVER do** (from our failures + `optimization_layer.biggest_weakness`)
6. **Proven Bangalore triggers** (from `audience_psychological_model.core_pain` of top performers)

These patterns feed directly into concept generation Steps 3-4.
