---
name: silas-photo-packaging-identity
description: "Use when turning separate photographs into individual 3:4 photo-plus-packaging identity posters with a preserved upper photograph and a packaging board below."
---

# Silas Photo Packaging Identity

Create one independent editorial poster for each supplied photo. Use this Skill for the fixed two-part poster, not ordinary retouching, multi-photo collages, standalone logos, or product mockups without the two-part format.

## Required workflow

1. Inspect every local input before editing and label the edit target. Build one normalized prompt per photo from [the production prompt](references/photo-packaging-prompt.zh-CN.md).
2. Make one 3:4 portrait poster per photo. Its single horizontal boundary is at the mathematical midpoint: the upper photograph and lower identity board have exactly equal pixel height.
3. Preserve the upper half as one continuous photograph: subject identity and count, anatomy or structure, pose, relationships, product geometry, materials, natural light, and original color atmosphere. Only restrained editorial grading and natural background extension for the upper 3:2 window are allowed. Do not stretch, mirror, beautify, relabel, duplicate, or reconstruct a locked subject.
4. Derive the lower-half visual genes from the source—such as silhouette, contour, posture, relationship, opening, structural lines, material behavior, or color relationship. Translate them into an abstract packaging family with five to eight source-appropriate carriers; use one or two hero packages and arrange the rest on a professional grid. An explicit user theme or palette overrides the lower half only.
5. Treat user-supplied title, brand, and allowed supporting text as authoritative. Render only the current allowed strings; remove stale text from earlier variants, gibberish, and repeated identical lockups.

## Revision and acceptance

For a lower-half-only revision, restore the approved upper half pixel-identically and replace the old lower-half brand and palette completely. First make one targeted generative correction. If the exact split still drifts, assemble approved regions proportionally without non-uniform stretching; use same-color padding when needed.

Save every accepted iteration under a new versioned filename. Before completion, fully decode the output and record its dimensions, upper and lower pixel heights, color mode, midpoint measurement, and SHA-256. Inspect fidelity, text, carrier count, layout, palette, and the visible transition; a nominal 3:4 ratio or visual approximation is insufficient.

Do not publish, embed, name, or otherwise expose original input assets or private local paths in external materials. Publish only authorized generated outputs and Skill documentation.
