# CLAUDE.md — Ancient History: Origins to 1200 CE

Project-specific instructions for AI-assisted authoring. The global instructions at `~/.claude/CLAUDE.md` apply on top of this file.

## Project Overview

This is an undergraduate intelligent textbook covering ancient world history from cosmic origins through approximately 1200 CE. It is organized around the UCLA "World History for Us All" Big Era framework (Eras 1–5) and three thematic axes (Humans and the Environment, Humans and Other Humans, Humans and Ideas).

A core editorial commitment of this textbook is to **incorporate archaeological, paleoanthropological, and paleogenomic findings published in the last fifteen years as first-class concept nodes**, not as footnotes to canonical pre-2010 textbook content. When generating chapter content, glossary terms, quizzes, or supplementary material, default to the current evidence base (Göbekli Tepe and the Tas Tepeler complex, Lomekwi 3 stone tools, Sahelanthropus and Ardipithecus, Homo Naledi, the Jebel Irhoud finds, Doggerland, Madjedbebe, the White Sands footprints, Sulawesi cave art, Sanxingdui, Liangzhu Culture, Caral-Supe, Cahokia, Chaco Canyon, Aguada Fenix, the ancient-DNA understanding of Yamnaya migration and Proto-Indo-European, the 4.2 ka Event, the Late Antique Little Ice Age, the Justinianic Plague, etc.) rather than the 1990s textbook narrative.

## Tone and Voice for Chapter Content

This is a textbook, but it is **not** a stuffy one. Default to a tone that is **light, warm, optimistic, and quietly funny**. We are not taking ourselves too seriously. The goal is for a student to come away from a section grinning, not yawning.

### Posture

- Treat the reader as a smart friend, not a captive audience.
- Be **playful** with framings, section openers, analogies, and asides — but the *evidence and dates* underneath stay rigorous.
- A few well-placed jokes per chapter are encouraged. Dry, observational, slightly nerdy humor lands best (think: pointing out that bronze-age accountants invented spreadsheets in clay, or that the Late Bronze Age Collapse was, in modern terms, a really bad supply-chain outage). Avoid pun-overload, slapstick, or jokes that punch down at ancient peoples.
- Aim for one chuckle and one "huh, I never thought of it that way" per major section.
- Wonder is a tool. When something is genuinely amazing — that 45,500-year-old Sulawesi pig painting, that Sumerian schoolboy's homework tablet, that Polynesian navigators crossed thousands of km of open ocean by reading swells — *say so*. Earned awe, not breathless hype.

### The Superpowers Framing

Frame the entire textbook as **superpower acquisition**. Studying ancient history doesn't just fill your head with names and dates — it gives you concrete cognitive abilities you can use the rest of your life. Return to this framing in chapter openers, capstones, and Chronos admonitions. The four superpowers:

1. **Critical thinking** — distinguishing claims from evidence, weighing alternative interpretations, recognizing when a confident-sounding source is actually thin on data.
2. **Systems thinking** — seeing how environment, technology, religion, trade, and politics interact and produce cascading change rather than treating events as isolated.
3. **Positive skepticism** — the *constructive* kind: not cynicism, but the habit of asking "how do we know this?" before accepting or sharing a claim. Ancient historians do this for a living because their evidence is fragmentary; the same muscle works on social-media posts.
4. **Bias and misinformation detection** — recognizing point-of-view, agenda, and selective framing in sources (ancient *and* modern), and resisting both viral falsehoods and overconfident "well-actually" corrections.

When relevant, point out that the analytical move a student just learned (e.g., "compare two primary sources that disagree") is the same move that helps them spot a misleading screenshot in their feed. Don't preach it — *show* it.

### Style guardrails (still apply)

- Stay accurate. Jokes never override evidence; if a punchline requires distorting the historical record, drop the punchline.
- Don't be flippant about suffering (slavery, plague, conquest, genocide). Warmth is fine; mockery of victims is not.
- No modern political point-scoring.
- No contemporary slang that will date the textbook in two years ("vibes," "it's giving," "based," etc.). Timeless wit ages better.
- Optimism is the default emotional register, but it is *earned* optimism — acknowledge the dark parts honestly, then point out what humans have figured out, recovered from, or built anew.

## Learning Mascot: Chronos the Tortoise

### Character Overview

- **Name:** Chronos
- **Species:** Galápagos-style tortoise
- **Personality:** Wise, patient, curious, warm
- **Catchphrase:** "The long view starts here."
- **Visual signature:** Warm earthy-brown domed shell with subtle amber-gold ridges; sandy-tan skin with gentle wrinkle textures suggesting age; small round gold-wire scholar's spectacles. Arms and legs are intentionally free of any accessories, scrolls, satchels, or clothing — body language must stay fully expressive.

### Voice Characteristics

- Speaks with the calm authority of an experienced teacher who has thought about the long arc of history many times before — and who genuinely enjoys it
- Warm, encouraging, and quietly funny. Chronos is the mascot equivalent of a beloved professor whose lectures students don't skip because the asides are too good to miss
- Uses concrete, evidence-grounded examples — never vague exhortations
- Patient by default; does not scold. *May* dramatize gently for emphasis when the moment earns it ("Pull back the lens for a moment — what we are about to see took 13.7 billion years of setup")
- Connects local detail to the longer historical arc when it would help a student
- Occasionally winks at the modern reader: a wry one-liner, a knowing comparison ("Yes, that really is an Akkadian customer-complaint tablet about a bad copper shipment"), a moment of earned awe
- Reinforces the **superpowers framing** — reminding students that the analytical move they just practiced works on social-media claims too
- Signature phrases: *"The long view starts here."*, *"Pull back the lens for a moment."*, *"Notice what we know now that earlier textbooks didn't."*, *"This is one of your superpowers."*
- Avoid: exclamation-mark spam, baby-talk, contemporary slang, treating ancient people condescendingly, mocking victims of conquest or disaster

### Mascot Admonition Format

Always place mascot images in the admonition body, never in the title bar. Use the `md_in_html` extension to embed `<img>` tags.

```markdown
!!! mascot-welcome "Title Here"
    <img src="../../img/mascot/welcome.png" class="mascot-admonition-img" alt="Chronos waving welcome">
    Admonition text goes here after the img tag. Keep it to 1–3 sentences.
```

The `src` path is **relative to the rendered page URL**, not the markdown file. MkDocs uses directory URLs, so for a chapter page at `chapters/01-cosmic-origins/index.md` (which renders at `chapters/01-cosmic-origins/`) use `../../img/mascot/POSE.png`. Count directories from the rendered page to `docs/img/mascot/`.

### Pose Filenames

| Filename | When to use |
|---|---|
| `neutral.png` | General sidebars / default / site logo |
| `welcome.png` | Chapter openings only |
| `thinking.png` | Key insights or paradigm-reframing concepts |
| `tip.png` | Actionable study or analytical advice |
| `warning.png` | Common pitfalls and misconceptions |
| `encouraging.png` | Beginning of difficult passages |
| `celebration.png` | End of major sections, chapter capstones |

### Placement Rules (hard limits)

| Context | Admonition type | Frequency |
|---|---|---|
| General sidebar | `mascot-neutral` | as needed |
| Chapter opening | `mascot-welcome` | exactly **one** per chapter |
| Key concept | `mascot-thinking` | 2–3 per chapter |
| Helpful tip | `mascot-tip` | as needed |
| Common mistake | `mascot-warning` | as needed |
| Difficult content | `mascot-encourage` | as needed |
| Chapter close / capstone | `mascot-celebration` | exactly **one** per chapter |

**Hard caps:**

- ≤ 6 mascot admonitions per chapter total
- Never two mascot admonitions back-to-back
- Never use the mascot for purely decorative purposes — every appearance must add a teaching point Chronos can plausibly own

### Do's and Don'ts

**Do:**

- Use Chronos to introduce new eras with the "long view" framing
- Include the catchphrase *"The long view starts here."* in chapter-opening welcome admonitions
- Keep dialogue brief (1–3 sentences)
- Match the pose image to the content type
- Make Chronos's voice consistent across chapters

**Don't:**

- Exceed 6 mascot admonitions per chapter
- Place mascot admonitions back-to-back
- Change Chronos's personality, species, or voice across chapters
- Use Chronos for decorative purposes only
- Anthropomorphize beyond gentle scholarly warmth (no slapstick, no contemporary slang) — Chronos can be witty, but he is still a tortoise of letters, not a stand-up comedian

## Style Conventions for This Textbook

- **Periodization:** Use BCE/CE, not BC/AD
- **Geographic naming:** Use period-appropriate names (Constantinople, not Istanbul, for the Byzantine period)
- **Civilizational framing:** When using the word "civilization," do so consciously and acknowledge its analytical limits per the course's evaluative outcomes
- **Recent evidence integration:** When a topic has been substantially revised by post-2010 evidence, *say so explicitly* and name the discovery — don't quietly update the canon without flagging the revision
- **Citations:** Prefer peer-reviewed archaeological journals and university press monographs from the last 10 years; flag older syntheses when used
- **Markdown:** Always put a blank line before any markdown list (mkdocs requirement)

## Project File Map

- `docs/course-description.md` — full syllabus
- `docs/learning-graph/` — concept list, dependency CSV/JSON, taxonomy, quality metrics, distribution
- `docs/learning-graph/learning-graph.json` — 297-concept DAG (Big Era Framework + Big Bang are the two roots)
- `docs/sims/graph-viewer/` — interactive vis-network viewer
- `docs/img/mascot/` — Chronos pose images (see `image-prompts.md` for prompts)
- `docs/css/mascot.css` — mascot admonition styling
- `logs/` — session logs from skill runs (concept revisions, learning-graph generation)
