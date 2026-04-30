# Chapter Design Log

**Date:** 2026-04-29
**Skill:** book-chapter-generator
**Source:** docs/learning-graph/learning-graph.json (297 concepts, 483 dependency edges)

## Inputs Reviewed

- `docs/course-description.md` — UCLA Big Era framework (Eras 1–5), three thematic axes (Environment, Other Humans, Ideas), AHA Tuning competencies, currency-of-evidence commitment to post-2010 archaeology/paleogenomics.
- `docs/learning-graph/learning-graph.json` — 297 nodes, 483 edges, validated DAG.
- `docs/learning-graph/concept-taxonomy.md` — 13 taxonomy categories (METH, THEME, COSMIC, HOMIN, PALEO, NEO, BRONZE, CLASS, AXIAL, POSTC, ISLAM, AMER, BRIDGE).
- `docs/learning-graph/taxonomy-distribution.md` — distribution counts per category.

## Edge-Direction Validation

Confirmed edges run in the **dependency direction** (from dependent → prerequisite). Foundational concepts (zero entries in the prereqs map) are exactly the two course roots:

- 1: Big Era Framework (METH)
- 21: Big Bang (COSMIC)

These are simple, introductory concepts — confirming the edge direction is NOT inverted to the enablement direction. Safe to proceed with `prereqs[edge['from']].add(edge['to'])`.

## Final Chapter Structure (16 chapters, 297 concepts, 0 dependency violations)

| Ch | Title | Count |
|---|---|---|
| 1 | Foundations of Historical Thinking | 22 |
| 2 | Cosmic and Biological Origins | 12 |
| 3 | Hominin Evolution and the Genus Homo | 18 |
| 4 | Paleolithic Migrations and Ice-Age Worlds | 20 |
| 5 | Paleolithic Symbolic Culture and Other Hominins | 20 |
| 6 | The Neolithic Revolution | 19 |
| 7 | Bronze Age Origins and the First Civilizations of Mesopotamia and Egypt | 23 |
| 8 | Bronze Age Asia, the Aegean, and the Late Bronze Age Collapse | 20 |
| 9 | Iron Age and the Classical Greco-Roman World | 24 |
| 10 | The Axial Age and World Religions | 22 |
| 11 | Classical Empires of Asia and Imperial Networks | 17 |
| 12 | Late Antiquity and the Byzantine World | 13 |
| 13 | The Rise of Islam | 13 |
| 14 | Tang and Song China and Carolingian Europe | 16 |
| 15 | Afro-Eurasian Networks: Africa, Indian Ocean, and East-Southeast Asia | 16 |
| 16 | The Pre-Columbian Americas and the Eve of Integration | 22 |

- Range: 12–24 concepts per chapter (all within acceptable 8–25 bounds)
- Average: 18.6 concepts per chapter
- All 297 concepts assigned exactly once
- Every prerequisite appears in same or earlier chapter than its dependent (validated by strict topological check)

## Major Design Decisions

### 1. Sixteen chapters, not fifteen

Initial draft used 15 chapters with a single combined "Late Antiquity, Byzantium, and the Rise of Islam" chapter at 26 concepts — exceeding the 25-concept soft cap. Split into Ch 12 (Late Antiquity & Byzantium, 13) + Ch 13 (Rise of Islam, 13). The split is also pedagogically clean: Late Antiquity is a transformation-of-Rome story; the Rise of Islam is a foundation-and-expansion story with its own internal arc.

### 2. Axial Age placed BEFORE Classical Empires of Asia (Ch 10 before Ch 11)

**Why:** Qin Dynasty (153) depends on Legalism (157, an Axial-Age school). Maurya/Gupta-era concepts like Ashoka (160), Hindu Synthesis (165), and Sanskrit Literature (168) depend on the Vedic-Upanishadic tradition (163, 164), Buddhism Origins (161), and Gupta Empire (167). Putting Classical Asia before Axial would force either Legalism into a chapter before its umbrella concept, or leave Qin without its philosophical prerequisite.

**Trade-off:** Several "religious" concepts that depend on classical-empire concepts (160 Ashoka, 165 Hindu Synthesis, 167 Gupta, 168 Sanskrit, 169 Indian Math, 182 Early Spread of Buddhism) are moved into Ch 11 instead of Ch 10. This means the Axial Age chapter focuses on the *foundational* religious/philosophical traditions, while Ch 11 covers the empires that institutionalized and spread them. The result is narratively coherent and dependency-clean.

### 3. Late-Roman concepts (150 Diocletian, 151 Constantine, 152 Crisis of Third Century) moved from CLASS into Ch 12

**Why:** Constantine's Conversion (151) depends on Christianity Origins (147), which is in the Axial Age chapter. Keeping these in Ch 9 (Greco-Roman World) would force Christianity to appear earlier than the Axial Age treatment, breaking the pedagogical narrative.

**Effect:** Ch 9 ends at Pax Romana / Augustus; Ch 12 picks up with the third-century crisis and Late Antiquity.

### 4. "Primary vs Secondary Civilization" (114) moved from BRONZE into Ch 16 (Americas)

**Why:** Concept 114 has six prerequisites including Olmec Civilization (112), which sits in the AMER hemispheric chapter. Keeping 114 in the Bronze Age chapter would either force Olmec out of the Americas chapter (fragmenting the hemispheric narrative) or violate the dependency.

**Effect:** Ch 16 opens with a comparative synthesis across all six primary-civilization centers (Mesopotamia, Egypt, Indus, Yellow River, Olmec, plus a discussion of Caral-Supe), which is pedagogically apt for an Americas chapter that needs to position the New World alongside the Old.

### 5. Liangzhu Culture (286) moved from NEO (Ch 6) to BRONZE (Ch 7)

**Why:** Liangzhu depends on Urban Revolution (88, BRONZE). Although tagged NEO in the taxonomy, its hydraulic-state character requires the urban-revolution concept already to be in play.

### 6. Paleolithic split into two chapters (Ch 4 + Ch 5), 20 concepts each

**Why:** PALEO has 40 concepts — too large for one chapter. Split is by *theme* rather than chronology:

- Ch 4 = migrations, climate, ice-age geography, hunter-gatherer organization (the "where and how they moved" story)
- Ch 5 = symbolic culture, cave art, Neanderthals/Denisovans, Mesolithic transitions (the "what they thought and made" story)

The split keeps Late-Paleolithic transitional content (Mesolithic 62, Microliths 66, Doggerland 280) with the symbolic-culture chapter so the Mesolithic context flows directly into the Neolithic chapter that follows.

### 7. Bronze Age split into two chapters (Ch 7 + Ch 8)

**Why:** BRONZE has 43 concepts — too large for one chapter. Split is by *region*:

- Ch 7 = Bronze Age origins, Mesopotamia, Egypt, plus Yamnaya/Proto-Indo-European/Steppe pastoralism and the 4.2 ka event (the western/steppe story)
- Ch 8 = Indus, Yellow River/Shang/Zhou, Aegean (Minoan/Mycenaean), Phoenicians, Hebrew origins, Late Bronze Age system and Collapse, Sanxingdui, Erlitou, Stonehenge (the eastern + Aegean + collapse story)

### 8. Classical period split into Ch 9 + Ch 11 (with Axial Age in between)

**Why:** CLASS has 41 concepts. The split is geographic + the Axial Age sandwiched between:

- Ch 9 = Greco-Roman world (Iron Age, Greek poleis, Achaemenid, Hellenistic, Republic through Pax Romana)
- Ch 10 = Axial Age (intervenes to provide the religious-philosophical foundation)
- Ch 11 = Classical empires of Asia (Qin, Han, Maurya, Gupta, Parthian, Sasanian, Silk Road, Roman–Indian Ocean trade, Bantu Migrations)

### 9. POSTC (42 concepts) split into three chapters (Ch 12, 14, 15) plus ISLAM standalone (Ch 13)

**Why:** Forty-two concepts is too large for one chapter. The split is by region and network:

- Ch 12 = Late Antiquity + Byzantine arc + climate/plague (Mediterranean transformation)
- Ch 14 = Tang/Song China + Carolingian Europe (the "two ends of Eurasia rebuild" story, plus Vikings/Kievan Rus)
- Ch 15 = Africa + Indian Ocean + East/SE Asia (the maritime-and-overland network story, plus Polynesian expansion)

### 10. ISLAM kept as standalone Ch 13 (13 concepts)

**Why:** Although 13 concepts is at the lower bound of the acceptable range, the Islamic civilization arc is pedagogically self-contained (Muhammad → caliphates → Islamic Golden Age → dar al-Islam → Sufism), and several POSTC concepts (Trans-Saharan Trade, Indian Ocean Trade, Kilwa Kisiwani) depend on Dar al-Islam. The course-taxonomy doc explicitly split ISLAM out of POSTC for pedagogical importance; the chapter design respects that decision.

### 11. AMER kept consolidated in Ch 16 (with BRIDGE)

**Why:** AMER has only 10 concepts spanning Big Era 3 (Caral-Supe, Olmec) through Big Era 5 (Maya, Cahokia, Aguada Fenix). Scattering them by date would under-represent the Americas (the very problem the AMER taxonomy split was created to solve). Combining with BRIDGE (11 concepts) gives a 22-concept final chapter that closes the course with hemispheric synthesis + the eve-of-integration framing for the post-1200 companion course.

## Validation Methodology

A Python script (`/tmp/design_chapters.py` during the run) was used to:

1. Build the prerequisite map with the correct dependency direction (`prereqs[edge['from']].add(edge['to'])`).
2. Confirm foundational concepts are simple/introductory (Big Era Framework, Big Bang) — guards against the inverted-edge footgun.
3. Map each concept to its assigned chapter index.
4. For every chapter and every concept in it, check every prerequisite is in the same or an earlier chapter; collect any violations.
5. Confirm every concept is assigned exactly once (no missing, no extra, no duplicates).

Final result: **0 dependency violations, 297/297 concepts assigned uniquely**.
