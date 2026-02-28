# MEMORY.md — Next.BLR Flow System

> The human-readable map of the entire content creation system. Must stay in sync with CLAUDE.md.
> Last synced with CLAUDE.md: 2026-02-28

---

## Water Flow Model

```
╔══════════════════════════════════════════════════════════════════╗
║                        INPUTS (you feed these)                  ║
║  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐    ║
║  │ Daily JSONs   │  │ Audio/Text   │  │ Weekly Research     │    ║
║  │ 3-data/       │  │ Feedback     │  │ Trends+Competitors  │    ║
║  └──────┬───────┘  └──────┬───────┘  └─────────┬──────────┘    ║
╚═════════╪══════════════════╪════════════════════╪═══════════════╝
          │                  │                    │
          ▼                  ▼                    ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 1: KNOW                                    [1-profile/]   │
│  Product bible + TG profile + customer stories + objective      │
│  + cast & crew + shoot resources                                │
│  WHO we sell to, WHAT we sell, WHERE we shoot, WHO acts         │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 2: LEARN                        [2-feedback/ + 3-data/]   │
│  Video feedback + concept feedback + audience feedback           │
│  + our content JSONs (winning/failing patterns)                  │
│  + competition JSONs (stealable formats)                         │
│  WHAT worked, WHAT failed, WHAT competitors do                  │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 3: INSPIRE              [4-inspiration/ + competitive-intel/]│
│  Cross-pollination library + life event calendar                │
│  + viral reference library + competitor strategy                 │
│  FORMATS to steal, TIMING to ride, GAPS to exploit             │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 4: IDEATE                                    [5-ideas/]   │
│  Raw one-liner ideas from objective                              │
│  Content mix: BD 40-50% | IE 30-35% | Magnet 15-20%            │
│  IDEAS come before CONCEPTS. Seeds before scripts.              │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
          ┌────────────────────────────────────┐
          │  DEBUG GATE 1: IDEA ALIGNMENT      │
          │  Objective match? TG fit?          │
          │  Content mix ratio check?          │
          │  Score 25+/30 to proceed           │
          └────────────────┬───────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 5: BUILD                                    [6-engine/]   │
│  Master concept formula + law-powered engine                     │
│  + 402 conversion laws + magnet framework                        │
│  + 292 visual hook laws (lookup)                                 │
│  Pick law stack → design 4-layer hook → build script            │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
          ┌────────────────────────────────────┐
          │  DEBUG GATE 2: CONCEPT DRIFT       │
          │  TG alignment? Product focus?      │
          │  Brand voice? Bangalore specific?  │
          │  Conversion path designed?         │
          └────────────────┬───────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 6: GUARD                                     [7-rules/]   │
│  34 global rules + content philosophy                            │
│  + kill tests (6 questions)                                      │
│  APPROVED patterns vs REJECTED patterns                         │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
          ┌────────────────────────────────────┐
          │  DEBUG GATE 3: KILL TESTS          │
          │  All 6 kill tests pass?            │
          │  No rejected pattern match?        │
          │  Has SOUL? (weird specific detail) │
          └────────────────┬───────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  TANK 7: VALIDATE                              [9-validation/]  │
│  24-point checklist + 30-law score + I×E×S share score          │
│  + edit direction template                                       │
│  SHOOT (25+) / FIX (20-24) / REWORK (15-19) / KILL (<15)      │
└──────────────────────────┬──────────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  OUTPUT: APPROVED CONCEPT                                       │
│  → 8-concepts/10-pending-*.md (pending review)                  │
│  → 8-concepts/0-approved-*.md (ready to shoot)                  │
│  → 11-tracking/shoot-done.md (post-production)                  │
└─────────────────────────────────────────────────────────────────┘

LOOKUP (used during BUILD, not sequential):
  10-hook/ — pattern interruption reference + 292 visual hook laws
```

---

## Debug Checkpoint System

At every gate transition, Claude outputs this box before proceeding:

```
┌─ DEBUG: [Step Name] ──────────────────┐
│ Objective Match: X/10                  │
│ TG Alignment: [Yes / Drift detected]  │
│ Product Focus: [On track / Drifting]   │
│ Content Mix: [Within ratio / Off]      │
│ Brand Voice: [Consistent / Drifting]   │
│ VERDICT: PROCEED / STOP               │
└────────────────────────────────────────┘
```

**STOP triggers** (any one = halt + ask user):
- Objective match < 7/10
- TG drift — concept doesn't speak to 22-35 Bangalore commuter
- Product drift — concept not connected to specific BCH product
- Content mix violation — ratio already maxed for this content type
- Brand voice drift — too corporate, too generic, not Bangalore enough

---

## File Lifecycle

### STATIC files (rarely change — foundational)
| File | What | Updated When |
|------|------|-------------|
| `1-profile/product-bible.md` | Product details, pricing, USPs | When products/pricing change |
| `1-profile/tg-deep-profile.md` | TG psychographics | When TG understanding deepens |
| `1-profile/objective.md` | Current phase + content mix targets | When business strategy shifts |
| `1-profile/cast-and-crew.md` | 15+ talent roster, gear list | When new talent/gear added |
| `1-profile/shoot-resources.md` | Locations, props, equipment | When inventory changes |
| `6-engine/BCH-brain.md` | Business data, offers | When offers/business data changes |

### GROWING files (accumulate data — you feed these)
| File | What | Updated When | How |
|------|------|-------------|-----|
| `1-profile/customer-stories.md` | Real stories, triggers | Weekly (THE GOLDMINE) | You paste/tell stories → Claude appends |
| `2-feedback/video-feedback.md` | Post-publish performance | After each video publishes | You paste audio/text → Claude routes here |
| `2-feedback/concept-feedback.md` | Review notes | After concept review sessions | You paste feedback → Claude routes here |
| `2-feedback/audience-feedback.md` | DMs, comments, shares | When patterns emerge | You paste reactions → Claude routes here |
| `3-data/our-content/*.json` | Our video performance data | After each video (daily) | You drop JSON files |
| `3-data/competition/*.json` | Competitor video analysis | When you study competitors (daily) | You drop JSON files |
| `competitive-intel/competitive-intel.md` | Competitor strategy | When new competitors studied | Claude updates during weekly research |
| `5-ideas/ideas-*.md` | Raw idea bank | During idea generation | Claude generates, filename has count |
| `8-concepts/10-pending-*.md` | Pending concepts | During concept generation | Claude appends, renames with count |
| `8-concepts/0-approved-*.md` | Approved concepts | After review sessions | You approve, Claude moves + renames |
| `11-tracking/shoot-done.md` | Shot tracking | After shoots | You update |

### LIVING files (evolve with research — weekly refresh)
| File | What | Updated When |
|------|------|-------------|
| `4-inspiration/cross-pollination-library.md` | Hooks from other niches | Weekly research |
| `4-inspiration/life-event-calendar.md` | Seasonal/event triggers | Weekly + before major events |
| `4-inspiration/viral-reference-library.md` | Decoded viral videos | When you find viral references |
| `competitive-intel/competitive-intel.md` | Competitor strategy gaps | Weekly research |

### ENGINE files (frameworks — updated during weekly research)
| File | What | Updated When |
|------|------|-------------|
| `6-engine/BCH-master-concept-formula.md` | Scoring + creation bible | When formula evolves |
| `6-engine/law-concept-engine.md` | 292 laws → concept in 7 phases | When engine improves |
| `6-engine/magnet-content-framework.md` | 3-level magnet system | When magnet strategy evolves |
| `6-engine/BCH-content-playbook.md` | Full theory, SOPs | When playbook updates |
| `6-engine/conversion-content-research.md` | Conversion research | During weekly research |
| `6-engine/300-LAWS-OF-CONVERSION-CONTENT.md` | 402 laws, 15 categories | When new laws discovered |
| `6-engine/research/` | 7 deep-dive source files | During weekly research |
| `7-rules/global-rules.md` | 34 rules (approved/rejected) | After review sessions |
| `7-rules/content-philosophy.md` | Owner's philosophy | When philosophy evolves |

### VALIDATION files (templates — stable)
| File | What | Updated When |
|------|------|-------------|
| `9-validation/script-checklist-rules.md` | 24-point checklist + edit direction | When checklist improves |
| `9-validation/law-score-template.md` | 30-law quick-score card | When scoring evolves |
| `10-hook/pattern-interruption-hook.md` | Hook reference (4 layers, scoring) | When hook system evolves |
| `10-hook/visual-hook-laws-master.md` | 292 laws lookup table | When new laws discovered |

---

## Session Protocols

### Daily Start
1. Scan `3-data/our-content/` and `3-data/competition/` for new JSONs
2. List new files found
3. Process using extraction rules from `3-data/README.md`
4. Update pattern summary
5. Ready for concept generation

### Audio Feedback (paste into chat)
You paste transcription → Claude classifies and routes:
| If it's about... | Goes to... |
|---|---|
| Video performance | `2-feedback/video-feedback.md` |
| Concept review | `2-feedback/concept-feedback.md` |
| Audience reactions | `2-feedback/audience-feedback.md` |
| Customer story | `1-profile/customer-stories.md` |
| Rule/preference | `7-rules/global-rules.md` |

Claude confirms routing before writing.

### Weekly Research
1. Trending formats — Reels/Shorts trends for lifestyle/EV/urban niche
2. Competitor moves — new content, strategy shifts
3. Algorithm updates — platform changes affecting reach
4. Update: `4-inspiration/`, `competitive-intel/`, `6-engine/` as needed
5. Flag any rule/framework updates needed

### MEMORY.md Sync
Whenever CLAUDE.md changes → MEMORY.md updates to match:
- File paths, flow steps, rules, thresholds, session protocols

---

## Quick Reference

### Scoring Thresholds
| Score | 30-Law | Hook | I×E×S | 24-Point |
|-------|--------|------|-------|----------|
| SHOOT | 25-30 | 8-10 | 500+ | 24/24 |
| FIX | 20-24 | 6-7 | 400-499 | 20-23 |
| REWORK | 15-19 | 4-5 | 300-399 | 16-19 |
| KILL | <15 | <4 | <300 | <16 |

### Content Mix Target
| Type | Target % | Purpose |
|------|----------|---------|
| Buying-Decision | 40-50% | Objection-busting, price anchoring, test ride triggers |
| Identity-Entertainment | 30-35% | "This is so Bangalore" shareability |
| Magnet | 15-20% | Follow magnets, DM triggers, save-worthy |

### Key Rules (non-negotiable)
- 4 Hook Layers: Visual + Spoken + On-Screen Text + SFX
- Protagonist = customer, NOT staff
- 2-Layer CTA: video-specific + "Cycle karidre, BCH ge banni"
- 85% Kannada / 15% English
- Bangalore specificity in every concept
- Concepts go ONLY in `8-concepts/10-pending-*.md`
- Persistent CTA banner on screen the ENTIRE video

> Last updated: 2026-02-28
