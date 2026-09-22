# PRD: Space Defense (Space Invaders clone)

**Course:** Games and AI · Week 5 exercise
**Platform:** Browser, HTML5 canvas, one `index.html` (no frameworks, no build step)
**How to use this file:** put it in your project folder as `PRD.md`. Your first Cursor prompt is: *"Read PRD.md. Phase 1 is already built. Implement Phase 2, requirement R1 only."* One requirement per prompt. Run the game after every approved change.

---

## 1. Overview

A fixed-shooter: the player defends the bottom of the screen from a descending grid of invaders. The game is lost when an invader reaches the player's row; a wave is won when every invader is destroyed.

**Player fantasy:** last line of defense.
**Session length:** 2 to 5 minutes per run.

## 2. Core loop

Move · shoot · dodge · clear the wave · next wave is faster.

## 3. Controls

| Input | Action |
|---|---|
| Left / Right arrows (or A / D) | move ship horizontally |
| Space | fire (one player bullet on screen at a time) |
| P | pause |
| R on game-over screen | restart |

## 4. Mechanics spec (the numbers)

- Canvas: 800 x 600. Player ship: 48 px wide, moves at 300 px/s, clamped to canvas.
- Invader grid: 4 rows x 8 columns, 48 px cells, starting 60 px from the top.
- The grid marches horizontally as ONE unit; on touching a screen edge it drops 24 px and reverses direction.
- March speed starts at 30 px/s and increases every time an invader dies (classic tension ramp: last invader is fast).
- Player bullet: 500 px/s upward. Limit ONE on screen (this is the real Space Invaders feel: it forces aimed shots).
- Scoring: bottom rows 10 pts, middle 20 pts, top 30 pts.
- Lose condition: any invader's bottom edge reaches the player's row, OR lives reach 0.

## 5. States

START (title + "press Space") → PLAYING → GAME OVER (score + restart). Wave cleared → short banner → next wave, one row lower and 20% faster.

## 6. Phase 1: built live in class (already done when you get this)

- Canvas + game loop (requestAnimationFrame)
- Player ship: movement + clamped edges
- Firing: one bullet, collision vs invaders, invader dies
- One 4x8 invader grid that marches and reverses

The Phase 1 build compiles and runs. Everything after that line is yours.

## 7. Phase 2: YOUR exercise (each = one prompt, in order)

- **R1 · Invader fire.** Random bottom-row invaders shoot downward every 0.8 to 2s. Bullet speed 250 px/s. *Accept: player can be hit; hits are visible.*
- **R2 · Lives.** Player starts with 3 lives, shown top-left. Hit = lose a life + 1s of blinking invulnerability. *Accept: game over at 0 lives.*
- **R3 · Lose-by-descent.** Invaders reaching the player's row ends the game immediately. *Accept: demonstrate it once.*
- **R4 · Score + hi-score.** Row-based scoring per the spec, hi-score persists during the session, both shown top-right. *Accept: hi-score survives a restart.*
- **R5 · Waves.** Clearing the grid spawns the next wave one row lower and 20% faster, with a "WAVE N" banner. *Accept: reach wave 3.*
- **R6 · Shields.** Four destructible bunkers between player and invaders; each absorbs 6 hits from either side, degrading visibly. *Accept: both sides can chew through a shield.*
- **R7 · Game states.** Proper START and GAME OVER screens per section 5, pause with P. *Accept: full loop: start, die, restart, without reloading the page.*

## 8. Stretch goals (any one = strong work)

- UFO bonus ship crossing the top every ~20s (50 to 300 random pts)
- March sound that speeds up with the grid (the classic four-note heartbeat, via your own SFX)
- Screen shake on player death; invader death particles

## 9. Make it YOURS (graded)

Re-skin it. The mechanics stay; the theme is your choice: generate your own sprite set (player, 3 invader types, shield) with your style tail from Week 4, and replace all placeholder rectangles. Add 3 SFX (shoot, invader death, player death) next week (ElevenLabs). Update your prompt archive as you go: art prompts AND code prompts.

## 10. Definition of done

Runs from a double-click on index.html · all seven requirements pass their accept lines · your own art, no placeholder rectangles · prompt archive updated · one git commit per requirement.
