---
name: stickman-stickwoman
description: Create relatable everyday-life short videos starring the Lifestyle Stickman (male) and Stickwoman (female) in Google Vids. Portrait 9:16 for Instagram Reels, TikTok and YouTube Shorts; landscape 16:9 for YouTube. Use when the user types /stickman-stickwoman or asks for a stickman/stickwoman relatable video.
---

# /stickman-stickwoman: relatable content with Stickman and Stickwoman

## The idea
Short, funny, relatable scenes from everyday life that people go through daily: relationships, home life,
money, shopping, cooking, travel, technology, friends, work-from-home, everyday struggles and small wins.
Two recurring characters, always the same design (see `characters/master_prompts.md` and the reference
images in `characters/`). Never redesign them.

## Formats (make both unless told otherwise)
| Platform | Aspect | Vids setting |
|---|---|---|
| Instagram Reels, TikTok, YouTube Shorts | 9:16 portrait | Aspect ratio: Portrait |
| YouTube (regular) | 16:9 landscape | Aspect ratio: Landscape |

For one idea, write one script and generate the portrait and the landscape version from it
(re-compose the prompt for each frame shape; do not just crop).

## Steps
1. **Idea**: take the user's topic, or propose 3 relatable situations (one line each) and let them pick.
   Keep it to ONE clear moment per clip with a punchline or a feeling people recognise ("it's me").
2. **Script**: hook in the first 2 seconds, one beat, a payoff. Write the action, expression and any
   on-screen caption. Save as `scripts/<slug>.md`.
3. **Prompts**: build one Vids prompt per format from `characters/master_prompts.md`
   (copy the character descriptions word for word) plus scene, action, camera, and "No text, no extra characters."
4. **Generate in Google Vids** (see "Driving Google Vids" below). Do NOT use Higgsfield.
5. **Insert** the clip so it is saved, check it, and report what you saw. Offer export (downloading needs the
   user's yes).
6. **Log** the prompt and result in `scripts/<slug>.md`, then commit and push when the user asks.

## Character rules (consistency)
- HIM: large round bald head, big white eyes with black pupils, thick curved black eyebrows, thick black
  moustache, one rounded ear, slim black stick body, thin arms and legs, oversized rounded white feet,
  bright red necktie.
- HER: large round head, big white eyes with long eyelashes, curved black eyebrows, black hair in a high
  bun, bright red headband, round red earrings, slim stick body, bright red top, simple black skirt,
  thin arms and legs, oversized rounded white feet.
- Style: polished 2D cartoon vector, bold smooth black outlines, white/cream character fill, bright balanced colours.
- Background adapts to the situation; avoid clutter. Friendly, humorous, everyday people, not corporate.

## Driving Google Vids (what we learned)
- Open `https://docs.google.com/videos/u/<n>/` in the built-in browser. Blank video, then **AI Video** in the right rail.
- The prompt panel starts collapsed: click the chevron (bottom right of the panel) to expand it.
- Model is **Omni**, 720p. Gear row: model, resolution, Aspect ratio (Landscape/Portrait), Video duration
  slider (3 to 15 s). Click the slider handle and use the Left/Right arrow keys. The slider can be disabled
  (locked at 3 s) on an account that is out of limits or on a text-only prompt; try again or switch account.
- Typing quirk: click inside the text box first, type ONCE, then verify with JavaScript that the prompt exists
  exactly once (`document.querySelector('[aria-label^="Describe your video"]').innerText`). Doubled text happens
  when focus is wrong. Use the **Clear** button to reset.
- Submit with the round arrow button. Generation takes about 1 minute. Poll the screenshot, do not resubmit.
- **Insert** the clip into the scene, otherwise Vids discards it when the tab closes.
- "You've hit your limits for generating videos in Vids" means the account's AI quota is used up. Google's pages
  disagree on reset (daily at midnight PT vs monthly on the 1st). Stop and tell the user; do not retry in a loop.
  Switching to another signed-in Vids account worked once.
- Reference-image upload (Ingredients, up to 3 images) opens a native file picker the built-in browser can't
  drive, and it first shows a consent dialog ("Create content from images in Workspace"). Accepting terms is the
  user's decision: ask them. Default to describing the characters in text.
- Never accept terms, download, or share on the user's behalf without their yes.

## Output locations
- Characters: `characters/` (master prompts, reference images)
- Scripts and prompt logs: `scripts/`
- Exports (if the user approves): `exports/`
