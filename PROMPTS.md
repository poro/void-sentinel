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
