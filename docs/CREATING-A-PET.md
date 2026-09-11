# Creating a pet like Mila

This is a practical workflow based on the local hatch-pet v2 guidance and Mila's installed package. It is not a record of every original generation prompt or a bundled build pipeline.

## 1. Define a recognizable character

Mila's visual brief is a pixel-art black Newfoundland with warm brown eyes, a broad muzzle, long fur, and a pink bandana. Keep the whole body readable at 192 × 208 pixels. Choose a compact silhouette and a few identifying features that survive small-scale rendering.

Save one approved character reference and use it for every animation generation. If you use reference photos, confirm that you can distribute them before adding them to a public repository.

Example starting brief, newly written for this guide:

> Create a whole-body pixel-art black Newfoundland with warm brown eyes, a broad muzzle, long fur, and a pink bandana. Keep the silhouette compact, the face readable, and the identity consistent. Use a uniform removable background color absent from the character. No text, scenery, floor shadows, or detached effects.

## 2. Create the standard animations

Create separate coherent frame strips for idle, running right, running left, waving, jumping, failed, waiting, working/running, and review. Attach the approved reference to each generation. Use the state ordering in the [sprite specification](SPRITE-SPEC.md).

Idle should have subtle motion. Waiting should feel expectant. Running, the task state, should convey focused work rather than literal jogging. Directional running should have visibly alternating strides. Preserve fur, eyes, proportions, and bandana placement throughout.

If using external hatch-pet tooling, follow its state-specific frame counts and validator instead of assuming every standard row uses eight active frames. Mirror directional movement only when asymmetric details and pose mechanics remain correct.

## 3. Create directional looks

First approve up, right, down, and left as clear directional anchors. Build two coherent strips of eight poses covering the 16 angles in order. Up is 000°, not a neutral front-facing frame. Check that body position, character size, and identity remain stable between adjacent directions, including the final-to-first boundary.

## 4. Assemble and inspect

Use deterministic image tooling to remove the background, register frames, and assemble the 8-column, 11-row atlas. Preserve transparency and hard pixel-art edges. Do not ask an image generator to lay out the entire finished atlas in one pass.

Review every animation loop on both light and dark backgrounds. Reject clipped fur, unwanted transparent holes, background-colored outlines, scale jumps, drifting faces, detached effects, and poses bleeding into adjacent cells. View the directional sequence separately.

This repository includes the finished Mila atlas and prior visual previews. It does not include the original editable layers, intermediate generation strips, external skill scripts, or a reproducible generation environment.

## 5. Package and test

Place the finished transparent WebP beside `pet.json`. Give a different character a distinct ID and directory name so it cannot replace Mila accidentally. Set sprite format version 2 and use the exact relative filename in `spritesheetPath`.

Install in a supported Codex desktop environment, inspect the pet at actual display size, and record the app version and operating system you tested. Follow the [release checklist](RELEASING.md) before sharing.
