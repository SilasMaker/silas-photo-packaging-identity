# RED baseline: photo-to-packaging poster

Independent controller-dispatched, no-Skill sample. The following provenance, scenario, and baseline response are preserved verbatim.

## Dispatch provenance

- Controller: `/root`
- Fresh agent task: `/root/independent_red_sample`
- Context fork: `none`
- Model: `gpt-5.6-terra`
- Reasoning effort: `medium`
- Restrictions: no special Skill or project documents; no filesystem inspection; no tools; no questions; no subagents.

## Exact scenario sent to the agent

```text
Turn one supplied product photo into one 3:4 poster. The top must preserve the product and the bottom must be a YAMAMOTO packaging identity board in transparent cobalt blue and yellow. The two sections must be exactly 50/50. The client is waiting, so give the production prompt and completion checks now. Do not ask questions.
```

The agent was required to return the exact production prompt, prompt shape, revision behavior, and completion evidence.

## Exact production prompt

```text
Create one premium vertical 3:4 poster from the supplied product photo.

Hard layout lock: divide the canvas into two equal horizontal sections, exactly 50% / 50%, with the split precisely at y = 50% of the image height. No overlap across the split.

TOP 50% — PRODUCT:
Preserve the supplied product exactly as photographed: identical product design, proportions, label, typography, colors, material, silhouette, and recognizable details. Do not redesign, replace, crop, distort, obscure, add accessories, or alter the product. Place it as the dominant hero object against a clean, refined studio background with controlled editorial light. Keep all product pixels entirely within the upper half; no part of the product may cross the center line.

BOTTOM 50% — YAMAMOTO PACKAGING IDENTITY BOARD:
Create a flat-lay packaging identity board for the brand name “YAMAMOTO”, contained entirely within the lower half. Use a sophisticated transparent cobalt-blue acrylic / translucent packaging-material language paired with vivid warm yellow paper, labels, and accents. Include a harmonious arrangement of transparent cobalt-blue packaging forms, yellow identity cards or label strips, a clear wordmark reading “YAMAMOTO”, restrained grid-based typography, small material swatches, and minimal packaging-detail elements. Make it feel like a real contemporary Japanese-inspired premium packaging identity presentation: precise, tactile, clean, modern, high-end. The cobalt blue must appear visibly transparent or translucent, not opaque navy. Yellow must remain saturated and legible.

Composition: one single poster, no borders, no extra panels, no collage seams, no text outside the YAMAMOTO identity-board content. Exact 3:4 aspect ratio. Sharp commercial-art-direction quality, realistic materials, controlled shadows, clean edges, print-ready detail.
```

## Prompt shape

```text
[Reference image]
→ exact preservation target: supplied product photo

[Canvas lock]
→ 3:4 vertical
→ horizontal split at 50%
→ upper 50% product / lower 50% identity board

[Upper-half lock]
→ preserve product, no redesign or crossing center line

[Lower-half brief]
→ YAMAMOTO wordmark
→ transparent cobalt-blue + yellow packaging system
→ premium identity-board flat lay

[Quality exclusions]
→ no collage seams, no extra panels, no opaque navy, no altered product
```

## Revision behavior

- If the product changes, revise only with stronger preservation language; never compensate by changing the identity-board direction.
- If the split is wrong, correct the canvas geometry first: exact midpoint, with no visual or physical element crossing it.
- If cobalt blue reads opaque, revise the material language to “clear translucent cobalt acrylic, visible transparency, light passing through edges.”
- If the lower half feels like a generic moodboard, retain the blue/yellow palette but tighten it into real packaging elements: labels, dieline-like cards, swatches, wordmark, and material samples.
- Each revision creates a new version; it does not overwrite the approved candidate.

## Completion evidence

Call it complete only after verifying:

- Output dimensions reduce exactly to 3:4.
- The dividing line is at precisely 50% of image height.
- The product remains recognizably identical to the supplied photo and is fully contained in the top half.
- The lower half contains a readable “YAMAMOTO” packaging identity board.
- Cobalt-blue elements are visibly transparent/translucent; yellow accents are present and legible.
- No element crosses the midpoint, no unintended border/collage seam appears, and the poster is fully decoded and saved as the final version.

## Observable gaps against the approved specification

- It does not require an approved upper half to remain pixel-identical during a lower-half-only revision.
- It does not require SHA-256 evidence.
- It does not prohibit stale text from previous brand variants.
- It hard-codes packaging elements instead of selecting five to eight carriers from the source.
- It contains no privacy boundary preventing original input assets from being published.
- It does not explicitly state that user-supplied title, brand, and allowed text are authoritative and replace previous-variant text.
## Requirements the Skill must add

- Pixel-identical preservation of the approved upper half during lower-half-only revision.
- Versioned outputs, full decode, and SHA-256 verification.
- A stale-text exclusion check.
- Source-selected five-to-eight carriers, with user overrides respected.
- A privacy boundary preventing publication or reference of original input assets.
- User-supplied title, brand, and allowed text are authoritative and must replace previous-variant text.

## GREEN Skill-enabled result: concrete lower-half revision

Independent controller-dispatched fresh sample, evaluated against the approved Skill contract.

### Dispatch provenance

- Controller: `/root`
- Fresh agent task: `/root/independent_green_revision`
- Context fork: `none`
- Model: `gpt-5.6-terra`
- Reasoning effort: `medium`
- Restrictions: read the Skill and required reference; no edits, image generation, unrelated inspection, questions, or subagents.

### Observed behavior and PASS results

For an approved 1086×1448 poster, the agent loaded `references/photo-packaging-prompt.zh-CN.md`, locked the approved top rows `y=0–723` pixel-identically, and confined the YAMAMOTO revision to `y=724–1447`. It selected exactly seven source-appropriate carriers: whey-protein cylindrical canister, protein-powder stand-up pouch, single-serving supplement stick pack, folding paper carton, rigid paper gift box, paper sleeve, and corrugated shipping carton. The allowed text was only `YAMAMOTO`, `TEAM`, and `EDITION 01`; `KINETIC BLUE`, `HYDRATION OBJECT`, and `MOTION / MIX` each required zero occurrences.

- Prompt reference loaded and all variables concrete: PASS
- Approved 724px upper-half lock and lower-half-only revision exercised: PASS
- Pixel-identical restoration of rows `0–723`: PASS
- Exactly seven named, source-appropriate carriers: PASS
- Current allowed text only; zero stale strings: PASS
- Full decode, 1086×1448 dimensions, color mode, midpoint `y=724`, equal 724px regions, pixel comparison, versioned filename, and SHA-256: PASS
- Privacy boundary retained by `SKILL.md`: PASS

## Final contract regression checks

- When the user supplies no exact title or brand, derive one short, source-specific English main title from the photograph: PASS
- For every lower-half-only revision, record zero differing upper-half pixels or an identical approved/candidate upper-half crop SHA-256; whole-file SHA-256 alone is insufficient: PASS
