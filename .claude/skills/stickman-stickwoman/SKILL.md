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

## Reference content (what "good" looks like)
Watched frames of both (not full audio), noted here so scripts aim at the same feel:
- **Rico Animations, "When intrusive thoughts kick in!"** (https://www.youtube.com/shorts/X5n-hIVuau4):
  one universal, slightly ridiculous inner-monologue moment (holding a baby and the urge to throw it).
  Plain flat background, black-outline cartoon, big expressive eyes, a title line at the top plus a
  subtitle-style caption that follows the spoken thought, small faint channel watermark. The joke is the
  relatable thought spiralling, not a complicated plot.
- **Alan Becker, "Handshake"** (https://www.youtube.com/shorts/B5OU2T3BiFo): a single repeated action that
  escalates ("Level 1" ... "Level 100"), simple stick figures on a clean game-like background, a number
  counter as the running gag, a surprising payoff.
- Takeaways: one idea per short, universal feeling or escalating gag, readable in 1 to 2 seconds, captions on
  screen, quick loop-friendly ending. Tone can be funny, ridiculous or occasionally serious/heartfelt.
- Make our own original ideas in the Stickman/Stickwoman style. Do not copy their jokes, scripts, characters or footage.

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
5. **Insert** the clip so it is saved, check it, and report what you saw.
6. **Brand it** (every short, see "House style: POV caption and channel badge" below): add the POV caption
   and the **ebsa** channel badge in Vids.
7. **Export** (downloading needs the user's yes) after branding, so the MP4 includes caption and badge.
8. **Log** the prompt and result in `scripts/<slug>.md`, then commit and push when the user asks.

## House style: POV caption and channel badge
Both are added in Google Vids after the clip is inserted. Neither uses AI generation quota.

**POV caption** (so viewers understand the joke at a glance)
- One line that frames the joke from the viewer's side, e.g. `POV: You said you're not hungry...`
  Start with "POV:" and keep it under about 40 characters so it fits in 2 lines.
- Style: white, bold, Arial, **size 28**, drop shadow on, whole length of the clip.
  Position: Format > Format options > Position, X -2, Y 20 (top of a 9:16 frame). Size 46 was too big and
  covered the characters' heads.
- Add it with Text panel > Add a title. Then edit the text. Size: expand the toolbar (the three-dot button in
  the top toolbar) and type the number in the Font size box. Colour: Format > Text > Color.

**Channel badge: "ebsa"** (our own visible brand mark)
- Channel name is **ebsa**. Badge = red circle (the characters' red), bold white text `ebsa`, size 12,
  bottom-right corner, on every short, same place each time.
- Make it from Shapes > oval, then Fill = red, double-click and type the name. In the shape's text, Ctrl+A then
  Delete twice before retyping, otherwise old characters stay.
- It is a deliberate, visible badge. Do NOT colour-match it to the background to hide anything, and do not
  crop, cover or paint out the AI-generation mark Vids adds to generated clips. When posting, tick the platform's
  "AI-generated / altered content" label (YouTube, TikTok, Instagram).

**Vids editing quirks (built-in browser pane)**
- Dragging and arrow-key nudging do not move objects. Use Format options > Position for exact X/Y.
- Ctrl+Shift+, only shrinks text by tiny steps. Type the size in the Font size box instead.
- If the editor shows an old/blank page after a sign-out, ask the user to sign in again (never type passwords).

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
- Quota: after a generation Vids shows "You have N seconds of video generation left this month. Limits reset
  Dec 1 at 8 AM". Generated seconds count against it, so a 10 s clip uses 10 s. Plan clip lengths accordingly.
- A generated clip is lost if the tab reloads before you press Insert. Insert as soon as it finishes; a
  "Previewing / Insert" prompt may appear, confirm it.
- Export: File > Download > MP4 (the user asking to export is the yes). The file lands in the Downloads folder;
  copy it into `exports/<slug>_portrait.mp4`.
- Never accept terms, download, or share on the user's behalf without their yes.

## Output locations
- Characters: `characters/` (master prompts, reference images)
- Scripts and prompt logs: `scripts/`
- Exports (if the user approves): `exports/`
