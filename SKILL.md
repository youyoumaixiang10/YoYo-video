---
name: family-handdrawn-story-video
description: Use when a user wants to turn a real parent-child story, family moment, toddler dialogue, or growth reflection into a fixed-character hand-drawn vertical video, especially for Xiaohongshu, WeChat Channels, or Douyin.
---

# Family Hand-Drawn Story Video

## State Contract

STATE A — STORYBOARD_PENDING: first verify that the user supplied a retellable real core event. If it is incomplete, ask exactly one highest-value necessary question and do not output a concrete storyboard. Once the event is sufficient, analyze it, propose at most three directions, recommend one, and produce a complete 5—7-scene storyboard. Stop and request whole-storyboard approval.

STATE B — STORYBOARD_REVISION: revise requested scenes, then show the complete revised storyboard. Return to STORYBOARD_PENDING; previous approval is invalid.

STATE C — PRODUCTION_APPROVED: enter only after an explicit confirmation that refers to the complete current storyboard. Load the production references and required media/video skills.

STATE D — DELIVERED: report only a verified MP4 path plus concise revision notes.

## Hard Rules

- Never treat character, style, single-scene, or partial-preview approval as production approval.
- Before STATE C, do not call image generation, music, sound-effect, HyperFrames initialization, preview, or render tools. Voice generation is additionally forbidden unless the user explicitly requests narration and approves its text.
- After any storyboard edit, discard prior approval and request approval again.
- Do not claim an MP4 exists until the file and media properties have been verified.
- Do not invent an event, participant, causal link, action, or exact spoken line. Disclosing an invention as an assumption does not make it acceptable.
- When a real core event is not yet retellable, do not output concrete scenes. Ask exactly one highest-value necessary question per turn; never bundle multiple questions.
- Default to no voiceover. On-screen narrative text and dialogue must carry the complete causal chain so the approved video is understandable with sound off.
- Do not burn a publication title into the video unless the user explicitly approves that title as an on-screen element.

## Reference Routing

- Read references/character-bible.md and references/visual-direction.md while writing the storyboard. Treat their layout, speech-bubble, decoration, and paper-background rules as production constraints, not optional style notes.
- Read references/storyboard-contract.md for every storyboard or storyboard revision.
- After approval, re-read references/character-bible.md, then read references/production-contract.md and the relevant example section in references/example-story.md.
- After approval, resolve and visually inspect all three fixed character sheets: `assets/characters/mother-and-child.png`, `assets/characters/father.png`, and `assets/characters/grandmother.png`.
- Before generating each scene, list its on-screen characters and select the matching sheets: mother or child uses `mother-and-child.png`, father uses `father.png`, and grandmother uses `grandmother.png`. Pass every selected sheet, and no unrelated character sheet, as a visual reference to image generation for that scene.
- After approval, REQUIRED SUB-SKILLS: hyperframes, general-video, media-use, imagegen. Let hyperframes install or refresh general-video before entering it.
