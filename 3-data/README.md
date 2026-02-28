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

## JSON Structures

### Our Content Template (10 Sections)
`our-content/template.json` — full performance tracking with metrics we can measure.

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

### Competition Template v2.0 (10 Sections — Trimmed for Concept Generation)
`competition/template.json` — optimized for stealing formats. Every field feeds concept creation.

| Section | What It Captures | Why It Matters |
|---------|-----------------|----------------|
| `content_identity` | Title, creator, niche, archetype, why selected | WHAT the video is and why we're studying it |
| `entry_arrest` | First 3 sec breakdown + 4 scored dimensions (visual disruption, feed contrast, motion, cognitive tension) | HOW it stops the scroll — scored and classified |
| `retention_mechanics` | Story shape, beat structure, twist, retention devices, re-hooks, drop-off prevention | WHY people stay watching |
| `visual_and_audio` | Visual anchor, color, motion, face, voice, music, mute-effectiveness | What eyes and ears experience |
| `share_drivers` | Primary/secondary driver, who DMs to whom, share trigger timestamp, safety score | The ONLY metric that matters for growth |
| `cta_analysis` | CTA type, wording, friction, does CTA kill shareability | How they convert (and if it backfires) |
| `audience_model` | Who it reaches, pain, identity desire, trigger, TG overlap | Does their audience match OURS |
| `stealable_template` | Hook/story/emotional/visual templates + one-line replication instruction + swap variables + non-negotiables vs flexible elements | THE OUTPUT — ready-to-use format for our concepts |
| `scores` | 6 scores (hook/retention/emotion/share/visual/steal-worthiness) + overall /100 | Quick ranking across 100 videos |

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

**From `stealable_template` (THE key section):**
- Take `hook_template` — adapt to Bangalore e-cycle context
- Take `story_template` — swap variables for our product/TG
- Take `emotional_arc_template` — map to our proven emotions
- Read `one_line_replication_instruction` — this is the format in one sentence
- Use `variables_to_swap_for_our_context` — plug in our locations, characters, pain points
- Read `non_negotiable_elements` — these MUST stay or the format breaks
- Read `flexible_elements` — these you CAN change
- Check `scalability_score` — only steal formats scoring 7+ scalability
- Check `fatigue_risk` — skip High fatigue formats

**From `entry_arrest` (hook scoring):**
- Steal `first_3sec_visual` patterns that work in adjacent niches
- Adapt `curiosity_gap_created` to Bangalore-specific pain points
- Track `entry_arrest_scores` — which dimension (visual disruption, feed contrast, motion, cognitive tension) dominates in top performers?
- Use `dominant_hook_type` to cluster videos: shock vs kinetic vs suspense entry
- Map to `maps_to_our_hook_taxonomy` to connect to our proven hook types

**From `share_drivers`:**
- Track `primary_share_driver` across all competition videos — which driver dominates in our niche?
- Use `who_would_DM_this_and_to_whom` — if the sharing relationship matches our TG, the format transfers
- Check `share_safety_score` — low safety = won't get shared regardless of quality

**From `retention_mechanics`:**
- Which `story_shape` appears most in high-scoring competition videos?
- Which `retention_devices_used` repeat across 60%+ of viral hits?
- Where do `re_hook_points` land? Copy the timing.

**From `audience_model`:**
- If `overlaps_with_our_TG` = Strong → steal aggressively
- If `core_pain_addressed` overlaps with ours → their solution format likely works for us
- If `identity_desire_activated` matches our TG → their emotional arc transfers

### Step 5: Filter Competition Through Our Rules

Before applying any competition pattern, validate:
- Does it pass Bangalore specificity? (Can it name a real location/pain?)
- Does it fit our TG (urban, 22-35, techie)?
- Can we shoot it at BCH store with iPhone?
- Does it violate any of our 34 global rules?
- Does the `content_archetype` align with our proven archetypes?
- Does `stealable_template.scalability_score` ≥ 7?
- Is `stealable_template.fatigue_risk` ≠ High?

### Output: Pattern Summary Before Generating

After reading all JSONs, Claude builds:

**From Our Content:**
1. **Top 3 hook formulas** (from `replication_blueprint.hook_template_extracted` of 80+ score videos)
2. **Top 3 emotional arcs** (from `story_psychology_flow.emotional_journey_curve` of highest-shared)
3. **Top 3 CTA structures** (from `cta_conversion_engineering` of highest-converting)
4. **Top 3 things to NEVER do** (from our failures + `optimization_layer.biggest_weakness`)
5. **Proven Bangalore triggers** (from `audience_psychological_model.core_pain` of top performers)

**From Competition (v2.0 template):**
6. **Top 5 stealable formats** (from `stealable_template` with scalability ≥ 7 + fatigue_risk ≠ High)
7. **Dominant entry arrest pattern** (which `entry_arrest_scores` dimension dominates across viral hits)
8. **Primary share driver for this niche** (most common `share_drivers.primary_share_driver` across 100 videos)
9. **Top 3 retention devices** (most repeated `retention_mechanics.retention_devices_used`)
10. **Hook archetype clusters** (group videos by `entry_arrest.dominant_hook_type` — which cluster performs best?)

**Aggregation Rule (every 25 videos):**
After every 25 competition videos analyzed, Claude auto-generates a pattern cluster summary:
- Hook archetype distribution (% shock vs kinetic vs suspense vs hybrid)
- Share driver distribution (% status vs tribal vs utility vs emotional vs moral)
- Story shape distribution (which shapes dominate in 80+ score videos)
- Non-negotiable elements that repeat across 60%+ of top performers
- Failure patterns from lowest-scoring videos

These patterns feed directly into concept generation Steps 3-4.
