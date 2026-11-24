# Stickman / flat illustration explainer experiments

Experiments in generating short explainer videos with Claude driving Google Vids.
Unplanned, exploratory work: treat everything here as a starting point, not a finished product.

## Contents

| File | What it is |
|---|---|
| `erp_script.md` | Script for the earlier "ERP Go-Live" stickman explainer |
| `ERP_Go-Live_Stickman_Explainer.mp4` | Rendered stickman explainer |
| `contact_sheet.png` | Contact sheet of the stickman scenes |
| `story_script.md` | 15-clip script for a 3D presenter video ("Why do small businesses struggle with disconnected systems?") |
| `what_is_erp_script.md` | Narration and scene plan for the flat 2D "What is ERP?" video (about 1:20) |

## How the "What is ERP?" video was made

1. Claude wrote a short script (nine narrated scenes).
2. Scenes were built in Google Vids: coral/colour backgrounds, stock illustrations, a speech-bubble shape, built-in animations (slide, rise, scale, zoom, spin).
3. Vids' AI voiceover (voice "Fola") narrated each scene; a stock music track was added and levels balanced with Vids' "Balance sound".
4. Exported to Google Drive as MP4.

## Known limits

- Slideshow-style: stock illustrations plus built-in animation, not custom character animation.
- Scenes 1, 2 and 9 reuse the same cartoon man and bubble.
- Some stock images have white backgrounds that clash with scene colours.
- The 3D presenter attempt stopped after 9 of 15 clips when Vids hit its AI video generation limit.

## Ideas for contributors

- Replace stock images with a consistent custom illustration set.
- Script-first workflow with brand colours decided up front.
- Automate scene building instead of driving the Vids UI by hand.

## /stickman-stickwoman workflow

Relatable everyday-life shorts with Stickman and Stickwoman: portrait 9:16 (Instagram, TikTok, YouTube Shorts)
and landscape 16:9 (YouTube), generated with Google Vids AI Video. Type `/stickman-stickwoman` in Claude Code.

- Skill: `.claude/skills/stickman-stickwoman/SKILL.md`
- Characters and reference images: `characters/`
- Scripts and prompt logs: `scripts/`
