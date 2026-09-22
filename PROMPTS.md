# Void Sentinel — Prompt Archive

## Phase 1
Starter from course template (already built). Commit: Phase 1 starter.

## R1
**Prompt:** Read PRD.md. Phase 1 is already built. Implement Phase 2, requirement R1 only. Do not implement R2-R7. Do not refactor unrelated code.
**Outcome:** Invader fire works — bottom-column invaders shoot every 0.8–2s at 250 px/s; hits flash the ship red.

## R2
**Prompt:** Implement R2 from PRD.md only. Do not modify any other behavior.
**Outcome:** Player starts with 3 lives shown top-left; each damaging hit removes one life and grants 1 second of blinking invulnerability. At 0 lives, gameplay stops and GAME OVER appears.

## R3
**Prompt:** Implement R3 from PRD.md only. Do not modify any other behavior.
**Outcome:** A living invader's bottom edge reaching the player's row immediately stops gameplay and shows GAME OVER, regardless of remaining lives or invulnerability.

## R4
**Prompt:** Implement R4 from PRD.md only. Do not modify any other behavior.
**Outcome:** Invader kills award 30/20/10/10 points from top row to bottom. Score and hi-score appear top-right; session storage preserves the hi-score when the page is reloaded to restart, while score starts at zero.

## R5
**Prompt:** Implement R5 from PRD.md only. Do not modify any other behavior.
**Outcome:** Clearing the grid advances to the next wave, starting 48 pixels lower and 20% faster per wave. A 1.2-second WAVE N banner pauses play between waves; leftover shots are cleared while lives and score carry over.

## R6
**Prompt:** Implement R6 from PRD.md only. Do not modify any other behavior.
**Outcome:** Four bunkers between the ship and invaders each absorb six hits total from player or enemy shots. Each hit consumes the shot, dims the bunker, and removes one lit health segment; the sixth destroys it. Shield damage persists between waves.

## R7
**Prompt:** Implement R7 from PRD.md only. Do not modify any other behavior.
**Outcome:** The game opens on a SPACE DEFENSE title screen and starts with Space. P pauses/resumes gameplay, including wave banners and timers. GAME OVER shows the final score and an R restart prompt; restarting resets the run while preserving the hi-score, without reloading the page.

## Section 9 — Void Sentinel reskin + section 8 UFO
**User/code prompt:** Read PRD.md section 9. Re-skin the game as Void Sentinel: rename title/UI from Space Defense to Void Sentinel, replace all placeholder rectangles with canvas-drawn custom sprites (player ship, 3 distinct invader types by row that remain distinguishable in grayscale, and shields). Prefer solid canvas pixel art (no external image files required). Do not add SFX. Also implement ONE stretch goal from PRD section 8: the UFO bonus ship crossing the top every ~20s for 50-300 random points. Do not break R1-R7 Accept behavior. Update PROMPTS.md with the art/code prompts used.

**Art prompt/design brief:** Draw original solid canvas pixel art for Void Sentinel, a last-line-of-defense arcade shooter against a dark starfield. Use a cyan interceptor with swept wings, a bright central cockpit and amber engines. Give invaders three silhouettes readable without color: a crowned diamond Wraith on the top row, an antennaed Raker with side claws on the second row, and a broad armored Crawler with splayed legs on the bottom two rows. Use lavender, coral and sage palettes with dark eyes. Build four arched shield bunkers with six hull lamps and progressive missing-pixel craters. Draw the bonus UFO as a gold domed saucer, and give both projectile types shaped pixel patterns. Keep hard pixel edges, solid fills and no external image assets. Art is authored directly as pixel maps in JavaScript; no image generator was used.

**Implementation brief:** Preserve existing movement, collision boxes, row scores, damage, invulnerability, wave progression and state controls. Share score/hi-score bookkeeping with the UFO. Spawn one non-shooting UFO above the grid every 20 seconds of active play, alternating crossing direction at 70 px/s. A player shot consumes the UFO and awards a random integer from 50 through 300 once, showing the awarded value. Freeze UFO movement, countdown and score notice during pause and wave banners; reset them on restart. Keep the original storage key to preserve existing session hi-scores. Add no audio, particles or screen shake.

**Outcome:** Browser/tab, page heading and START screen now read Void Sentinel. All game entities use custom canvas pixel sprites. Bunker damage remains six hits from either side with visible craters and hull lamps. The UFO is the sole stretch goal; all R1–R7 acceptance behavior is retained.
