# Mila sprite specification

This document describes the supplied package and local hatch-pet v2 contract. It is not an official promise of compatibility with every Codex release.

## Package

`mila/pet.json` contains ID `mila`, display name `Mila`, a character description, `spriteVersionNumber` set to `2`, and `spritesheetPath` set to `spritesheet.webp`. The referenced file must sit beside the manifest. Keep these two files together.

## Atlas geometry

| Property | Value |
| --- | --- |
| Format | WebP with transparency |
| Columns × rows | 8 × 11 |
| Cell dimensions | 192 × 208 pixels |
| Atlas dimensions | 1536 × 2288 pixels |
| Standard animation rows | 0–8 |
| Directional look rows | 9–10 |

Rows are zero-indexed from the top; columns run from left to right. Standard rows may contain inactive cells; eight columns do not imply eight active frames for every state.

| Row | State or direction angles |
| --- | --- |
| 0 | idle |
| 1 | running-right |
| 2 | running-left |
| 3 | waving |
| 4 | jumping |
| 5 | failed |
| 6 | waiting |
| 7 | running (task work) |
| 8 | review |
| 9 | 000, 022.5, 045, 067.5, 090, 112.5, 135, 157.5 |
| 10 | 180, 202.5, 225, 247.5, 270, 292.5, 315, 337.5 |

Angles advance clockwise: 000 is up, 090 is screen-right, 180 is down, and 270 is screen-left.

## Verification limits

Matching dimensions and manifest fields establishes structural consistency only. Check animation timing, directional meaning, silhouette continuity, and in-app rendering visually. The README GIF and contact sheets are existing showcase artifacts; regenerate them if the atlas changes.
