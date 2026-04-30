---
title: Mascot Image Prompts — Chronos the Tortoise
description: Self-contained AI image-generation prompts for each of the seven Chronos mascot poses.
---

# Image Prompts for Chronos the Tortoise

Each prompt below is **fully self-contained** — you can paste any single one into ChatGPT/DALL-E, Midjourney, Stable Diffusion, or any other image generator without needing to copy a separate base description. Generate at **1024×1024**, then save into `docs/img/mascot/` with the filename indicated.

After saving, run the padding-trimmer on each file (AI generators typically leave large transparent borders that make the mascot look too small at 90px display size):

```bash
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/neutral.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/welcome.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/thinking.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/tip.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/warning.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/encouraging.png
python ~/Documents/ws/claude-skills/src/image-utils/trim-padding-from-image.py docs/img/mascot/celebration.png
```

## Character reference (for human reviewers, not for the prompt)

- **Name:** Chronos
- **Species:** Galápagos-style tortoise
- **Personality:** Wise, patient, curious, warm
- **Catchphrase:** "The long view starts here."
- **Visual signature:** Warm earthy-brown domed shell with subtle amber-gold ridges; sandy-tan skin with gentle wrinkle textures; small round gold-wire scholar's spectacles; **arms and legs entirely free of any accessories or clothing** so body language stays fully expressive.

## Pose 1 — Neutral (general purpose / default / site logo)

**Filename:** `neutral.png`

```
Please generate a new png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell. The shell scutes
are a slightly darker chestnut brown outlined in subtle amber-gold ridges
that catch the light, evoking aged terracotta and weathered parchment. The
skin of the head, neck, and limbs is a warm sandy tan with gentle wrinkle
textures suggesting age and accumulated wisdom. Chronos wears small round
scholar's spectacles with thin gold wire frames and clear lenses, perched on
the bridge of his nose. The eyes are large, kind, deep-amber colored with a
warm closed-mouth smile. Arms and legs are entirely free of any
accessories, scrolls, satchels, or clothing — the body language must stay
fully expressive.

POSE: Chronos stands upright in a balanced, relaxed neutral pose, facing the
viewer directly. All four limbs rest naturally — front legs at his sides, hind
legs in a stable stance. No specific gesture. Expression: calm, attentive,
warmly intelligent. The pose is unassuming and suitable as a general-purpose
or default illustration that can also serve as a site logo.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame. No
background scenery.
```

## Pose 2 — Welcome (chapter openings)

**Filename:** `welcome.png`

```
Please generate a new welcome png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos faces the viewer with one front leg raised in a cheerful,
unmistakable wave of welcome. The other front leg rests at his side. His
expression is warmly excited — a wide friendly smile, eyes a little bright,
brow slightly raised in welcome. The pose unmistakably says "welcome,
let's get started." Slight forward lean to the body language.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame.
```

## Pose 3 — Thinking (key concepts)

**Filename:** `thinking.png`

```
Please generate a new thinking png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos has one front leg raised, with the toe gently touching his
chin in a classic "hmm, let me think" gesture. Head tilted slightly upward
and to one side. Eyes looking up and to the side as if considering something
important. Mouth in a small, contemplative half-smile. Above his head floats
a single warm-amber lightbulb (no text inside the bulb), suggesting an idea
forming. The bulb glows softly with a faint amber halo.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame.
```

## Pose 4 — Tip (hints and helpful guidance)

**Filename:** `tip.png`

```
Please generate a new tip png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos faces the viewer with one front leg raised and a single toe
extended upward in a "here's a useful tip" gesture, similar to a teacher
emphasizing a helpful point. The other front leg rests naturally at his side.
Expression: knowing, helpful, slightly conspiratorial — as if sharing
insider knowledge. A small four-pointed amber-gold sparkle floats just above
the upraised toe to draw the eye to the gesture.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame.
```

## Pose 5 — Warning (common mistakes / pitfalls)

**Filename:** `warning.png`

```
Please generate a new warning png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos faces the viewer with both front legs raised, palms outward,
in a gentle "wait, be careful here" gesture. The body language is cautioning,
not alarmed. Expression: concerned but caring — slightly furrowed brow,
gentle worry in the eyes, mouth in a small downward "be careful" curve. To
one side of his head floats a small amber exclamation mark inside a soft
yellow-amber circle, signalling caution without looking aggressive or
hostile.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame.
```

## Pose 6 — Encouraging (difficult content / "you've got this")

**Filename:** `encouraging.png`

```
Please generate a new encouraging png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos faces the viewer with one front leg raised in a clear
thumbs-up gesture (toe extended upward, others tucked). The other front leg
rests naturally at his side. Expression: warm and reassuring — a confident
soft smile, eyes crinkled slightly at the corners, head tilted just enough
to convey "you can do this." The overall body language radiates patient
confidence and "I believe in you" support, suitable for difficult or
challenging passages of the textbook.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber, fully transparent background — NOT white,
NOT black, NOT a checkered pattern. No text in image. No frame.
```

## Pose 7 — Celebration (achievements / chapter completion)

**Filename:** `celebration.png`

> **Background note for designers:** the celebration admonition uses a *dark deep-purple background* in CSS so that pale gold confetti sparkles read clearly. Keep confetti and sparkles in pale gold/cream/white — they will contrast against the dark admonition body. The mascot itself can stay in its normal warm-brown palette.

```
Please generate a new celebration png image now with a fully transparent background.

A modern flat-vector illustration of Chronos the Tortoise, a friendly
pedagogical mascot for an undergraduate ancient-history textbook covering
cosmic origins through 1200 CE. Chronos is a warm earthy-brown
Galápagos-style tortoise with a richly textured domed shell, chestnut-brown
scutes outlined in amber-gold ridges. Sandy-tan skin with gentle wrinkle
textures. Small round scholar's spectacles in thin gold wire frames perched
on the bridge of his nose. Large, kind, deep-amber eyes. Arms and legs are
entirely free of accessories or clothing.

POSE: Chronos is mid-celebration, both front legs raised high above his
head in a triumphant, joyful pose. Mouth open in a wide happy smile, eyes
squinted slightly with delight. Body leaning slightly back to emphasize the
upward motion. Falling around him are roughly a dozen pieces of pale-gold
and cream confetti — small four-pointed stars, thin streamers, and tiny
sparkle dots — distributed in a loose ring above and beside him. The
confetti must be PALE (gold, cream, off-white, soft yellow) so it will remain
visible against a dark deep-purple admonition background. Do NOT use dark
confetti colors.

STYLE: modern flat vector, confident dark outlines, soft shading, warm
earthy palette of brown and amber for the tortoise himself, pale-gold and
cream for the confetti. Fully transparent background — NOT white, NOT
black, NOT a checkered pattern. No text in image. No frame.
```

## Quality checklist after generation

For each PNG, before committing:

1. **Truly transparent background** (open in Preview or a browser; the background should show your desktop / page color through it, not a checker pattern saved into the file)
2. **Spectacles present and consistent** across all seven poses
3. **No accessories or clothing** on arms or body — these *must* stay free
4. **Color consistency** — the shell brown and amber-gold ridge colors should look like the same character across poses
5. **Pose actually reads** at 90px (open the image, then preview it shrunk down to ~90px wide; the gesture should still be unmistakable)
6. **Confetti for celebration is pale** (gold/cream/white), not dark
