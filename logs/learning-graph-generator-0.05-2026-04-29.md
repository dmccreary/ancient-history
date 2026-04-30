# Learning Graph Generation Session Log

**Skill:** learning-graph-generator v0.05
**Date:** 2026-04-29
**Project:** Ancient History: Origins to 1200 CE
**Working directory:** `/Users/dan/Documents/ws/ancient-history`

## Tool versions used

| Tool | Version |
|---|---|
| learning-graph-generator skill | 0.05 |
| analyze-graph.py | (unversioned in skill) |
| add-taxonomy.py | (bypassed — used inline Python with explicit ID lists) |
| csv-to-json.py | 0.04 |
| taxonomy-distribution.py | (unversioned in skill) |
| validate-learning-graph.sh | (unversioned in skill) |

## Inputs

- **Course description:** `docs/course-description.md` (quality score: 100/100, pre-existing)
- **Course description assessment:** `docs/learning-graph/course-description-assessment.md` (pre-existing, version 0.03)

## Step-by-step record

### Step 0 — Setup
- `docs/` and `docs/learning-graph/` directories already existed.
- No `mkdocs.yml` at project root; flagged for follow-up via `/book-installer`.
- Pulled latest from `~/Documents/ws/claude-skills` (already up to date).
- Copied skill Python programs and schema into `docs/learning-graph/`.

### Step 1 — Course description quality assessment
- **Skipped** because existing assessment scored 100/100.

### Step 2 — Concept list generation
- Initial draft: 254 concepts organized by Big Era 1-5, methodology, and bridge unit.
- Five user-driven revision passes added 42 concepts (final total: **296**).
- Detailed revision history captured in `logs/revised-concepts-list.md`.
- Footgun pattern named: the "settled timeline" footgun in LLM-generated concept lists.

### Step 3 — Dependency graph CSV
- Wrote `learning-graph.csv` with 296 rows, columns `ConceptID,ConceptLabel,Dependencies`.
- Two cycles found and fixed:
  - **159 ↔ 160** (Maurya Empire ↔ Ashoka): removed 160 from Maurya's deps.
  - **190 ↔ 191** (Byzantine Empire ↔ Justinian): removed 191 from Byzantine's deps.

### Step 4 — Quality validation
- `python3 analyze-graph.py learning-graph.csv quality-metrics.md` succeeded.
- **DAG validation:** ✅ valid, 0 cycles, 0 self-dependencies.
- **Foundational roots:** 2 (Big Era Framework, Big Bang).
- **Orphans:** 0.
- **Average dependencies/concept:** 1.64.
- **Max chain length:** 56 (cosmos through Bronze Age).
- **Note:** `find_cycles()` in analyze-graph.py crashes when cycles exist (line 128 ValueError). The DAG check itself works; the crash only blocks the human-readable cycle listing. Worked around by using a manual topological-sort scan to identify the cyclic concepts.

### Step 5 — Concept taxonomy
- Wrote `concept-taxonomy.md` with **13 categories** (slightly above the ~12 target; within ±2-3 tolerance).
- Largest category: BRONZE at 14.5% (well under 30% cap).
- ISLAM split out from POSTC; AMER split out as a region-spanning category to prevent under-representation.

### Step 5b — Taxonomy names JSON
- Wrote `taxonomy-names.json` mapping all 13 IDs to human-readable names.

### Step 6 — Add taxonomy to CSV
- **Bypassed `add-taxonomy.py`** (uses range/keyword matching). Used inline Python with explicit ConceptID lists per category for precise control.
- All 296 concepts mapped, 0 unmapped, 0 fell through to MISC.

### Step 7 — Metadata
- Wrote `metadata.json` with title, description, creator (Dan McCreary), date, version, format, schema URL, license (CC BY-NC-SA 4.0 DEED).

### Step 8 — Color config
- Wrote `color-config.json` assigning distinct CSS named colors to each TaxonomyID, drawn from the recommended 24-color distinct palette in csv-to-json.py v0.04.

### Step 9 — Generate learning-graph.json
- `python3 csv-to-json.py learning-graph.csv learning-graph.json color-config.json metadata.json taxonomy-names.json` succeeded.
- All 13 groups present with classifierName + color + auto-assigned font color.
- Schema validation surfaced a **known mismatch** between csv-to-json.py output (color as string) and `learning-graph-schema.json` (color as object). The script's output is the canonical format used by the graph-viewer; schema is stricter than the script. Skill marks validation as optional; not blocking.

### Step 10 — Taxonomy distribution report
- `python3 taxonomy-distribution.py learning-graph.csv taxonomy-distribution.md` succeeded.

### Step 11 — Index page
- Wrote `docs/learning-graph/index.md` from `index-template.md`, customized with course title, current scores (100/100 description, 2 roots, 0 orphans, max chain 56), 13-category taxonomy summary, and a "Currency of Evidence" callout describing the recent-archaeology integration.

### Step 12 — Session log
- This file.

## Files produced

| File | Purpose |
|---|---|
| `docs/learning-graph/concept-list.md` | Master 296-concept list, organized by section |
| `docs/learning-graph/learning-graph.csv` | Dependency graph + TaxonomyID column |
| `docs/learning-graph/learning-graph.json` | vis-network format with metadata, groups, nodes, edges |
| `docs/learning-graph/quality-metrics.md` | Graph structure validation report |
| `docs/learning-graph/concept-taxonomy.md` | 13-category taxonomy definitions |
| `docs/learning-graph/taxonomy-names.json` | TaxonomyID → human-readable name mapping |
| `docs/learning-graph/taxonomy-distribution.md` | Per-category concept distribution |
| `docs/learning-graph/metadata.json` | Dublin-Core-style learning graph metadata |
| `docs/learning-graph/color-config.json` | Stable color assignment per TaxonomyID |
| `docs/learning-graph/index.md` | Section landing page |
| `docs/course-description.md` | Updated with "Currency of Evidence" paragraph |
| `logs/revised-concepts-list.md` | Concept-list revision history (5 passes) |
| `logs/learning-graph-generator-0.05-2026-04-29.md` | This session log |

## Issues and follow-ups

1. **Project lacks `mkdocs.yml`** — run `/book-installer` to scaffold MkDocs Material site infrastructure and the graph viewer (`docs/sims/graph-viewer/`).
2. **`analyze-graph.py` cycle finder crashes** — non-blocking but worth filing upstream against the skill repo. The bug is in `find_cycles()` line 128 (`path.index(next_node)` raises when path doesn't contain `next_node`).
3. **Schema vs. script mismatch on color format** — `learning-graph-schema.json` requires `color` as an object; `csv-to-json.py` v0.04 outputs `color` as a string. Either the schema or the script needs to be updated upstream.
4. **Concept review** — concept list, taxonomy, and dependency graph are now locked. Strongly recommend a manual review pass before running `/book-chapter-generator`, since chapter generation is token-heavy and mistakes are expensive to fix downstream.

## Quality summary

- ✅ Valid DAG, 0 cycles, 0 self-dependencies, 0 orphans
- ✅ 2 foundational roots (Big Era Framework, Big Bang)
- ✅ 13 balanced taxonomies, largest 14.5% (BRONZE)
- ✅ All 296 concepts mapped to a taxonomy (0 fell through to MISC)
- ✅ Avg dependencies per concept: 1.64
- ✅ Max chain length: 56
- ✅ Recent-archaeology coverage integrated (42 of 296 concepts are post-2010 finds or methods)

**Overall quality score (subjective):** 92 / 100 — solid graph with current evidence base, balanced taxonomy, validated structure. Could improve with explicit primary-source nodes per Big Era and a wider AHA-competency tagging schema, but those are enrichment, not corrections.
