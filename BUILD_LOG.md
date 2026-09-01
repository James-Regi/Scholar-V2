# AI / Build Log

Development date: September 1, 2026

AI assistance was used to implement, debug, test, and document the game. The creator directed the concept, evaluated the playable results, reported friction, and approved revisions through repeated browser play.

| Major prompt or goal | Change made | Human verification / response |
| --- | --- | --- |
| Build a playable **Scholar Slash** browser game. | Created the static HTML, CSS, and Canvas JavaScript game with coursework enemies, waves, powers, HUD, and final boss. | Creator reviewed the game concept and continued directing control and balance revisions. |
| Show the exact number of coursework enemies cleared. | Changed the HUD counter to track defeated textbooks rather than passive score growth. | Retained in the final build. |
| Give the final boss a jetpack and laser control. | Added the final loadout and assigned it to `C`. | Creator continued testing the revised boss controls. |
| The game will not open from GitHub or VS Code. | Traced a JavaScript syntax error, repaired the missing brace, and verified the public Enter button. | Creator confirmed: “Ok it does open now.” |
| The game crashes after one or two Space attacks; restore Space to attack only. | Found `spark()` incorrectly scoped inside `spawn()`, corrected the scope, and consolidated duplicate keyboard listeners. `Space` now attacks only; `C` remains the boss control. | Creator tested the published revision and reported the next visible gameplay issue rather than the startup crash. |
| Enemy health bars extend left and enemies sometimes do not die. | Clamped damage and health-bar ratios to zero, guaranteed zero-health removal, and forced browsers to fetch the fixed asset. | Creator confirmed: “Wow looks good.” |
| Make Round 3 slightly easier by slowing enemy releases. | Increased the Round 3 spawn interval from 0.58 seconds to 0.8 seconds without changing enemy health or movement speed. | Published for final creator review. |
| Prepare submission evidence. | Added public links, this factual build log, a demonstration outline, and reflection. | Creator reviewed the requested submission materials. |

## Verification performed during development

- Loaded the local and GitHub Pages versions in fresh headless Chrome profiles.
- Triggered the real Enter button and confirmed the state changed from `READY TO FIGHT` to `FIGHTING`.
- Dispatched real Space keyboard events and monitored uncaught browser errors.
- Verified repeated hits, enemy defeat, power-up drops, continued animation, and zero-health handling.
- Compared deployed GitHub Pages assets with local file hashes after each repair.
- Checked the public game and repository URLs without authentication; both returned HTTP 200.

## Version record

- `4efef47`: initial game
- `be35e04`: startup syntax repair
- `63908cd`: attack crash and keyboard simplification
- `e0b8133`: browser cache refresh
- `446c025`: enemy health and defeat correction
- `e9e4630`: Round 3 balance adjustment
