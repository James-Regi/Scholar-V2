# AI / Build Log

AI assistance was used to implement, debug, test, and document Scholar Slash. The creator directed the concept, evaluated playable versions, reported friction, and approved revisions through browser play.

## First Day: August 27, 2026

The project existed locally before it was placed under Git version control. Local filesystem metadata provides the earliest surviving build record:

- `index.html` created August 27, 2026 at 2:50 p.m. EDT
- `style.css` created August 27, 2026 at 2:50 p.m. EDT
- `game.js` created August 27, 2026 at 2:51 p.m. EDT

| Initial goal | Work completed |
| --- | --- |
| Create a browser game called **Scholar Slash**. | Established the HTML page, Canvas-based game code, and visual stylesheet. |
| Turn academic pressure into an arcade game. | Created the student fighter, coursework enemies, combat, health, scoring, and wave progression. |
| Give the project a distinctive presentation. | Built the dark campus setting, scarlet-and-gold interface, opening overlay, HUD, and keyboard control display. |
| Add variety and progression. | Developed collectible study powers and the structure leading to a final coursework boss. |

These August 27 files were later imported into Git. Because the Git repository itself was initialized on September 1, the August 27 work has file-creation timestamps rather than individual Git commits.

## Today: September 1, 2026

| Prompt, test, or observed problem | Revision made | Human or technical verification |
| --- | --- | --- |
| Publish the existing game and track it in Git. | Created the initial repository commit from the August 27 project files and published it to GitHub. | Initial Git commit `4efef47`. |
| Show the exact number of coursework enemies cleared. | Changed the HUD to count defeated textbooks rather than passive score growth. | Commit `e59210e`. |
| Give the final boss a jetpack and laser control. | Added and refined the boss loadout, assigning its laser to `C`. | Commits `cb57495` and `677bbba`. |
| The game would not open from GitHub or VS Code. | Traced a JavaScript syntax error and repaired the missing brace. | The live Enter button changed from `READY TO FIGHT` to `FIGHTING`; the creator confirmed that the game opened. Commit `be35e04`. |
| The game crashed after one or two Space attacks; Space should only attack. | Found `spark()` incorrectly scoped inside `spawn()`, corrected the scope, and consolidated duplicate keyboard listeners. `Space` now attacks only. | Real Space-key events defeated a test enemy while the loop remained active and no browser exception occurred. Commit `63908cd`. |
| A browser still appeared to run an older broken version. | Changed the game-script asset URL to force browsers to download the repaired code. | Compared deployed and local asset hashes and verified they matched. Commit `e0b8133`. |
| Enemy health bars extended left and enemies appeared not to die. | Clamped enemy health and bar width at zero and guaranteed removal at zero health. | Overkill damage removed the enemy, created its drop, and left the game active. The creator confirmed that it looked good. Commit `446c025`. |
| Round 3 felt too difficult because enemies arrived too quickly. | Increased its spawn interval from 0.58 seconds to 0.8 seconds without changing health or movement speed. | Loaded the game and confirmed the live Round 3 configuration. Commit `e9e4630`. |
| Prepare submission and presentation materials. | Added public links, this build log, a concise demonstration outline, and a reflection. | Verified the game and repository without authentication; both returned HTTP 200. |

## Verification Methods

- Loaded local and GitHub Pages builds in fresh Chrome profiles.
- Clicked the real Enter button and dispatched real keyboard events.
- Monitored the browser for uncaught JavaScript exceptions.
- Tested repeated attacks, enemy defeat, power-up drops, continued animation, and zero-health handling.
- Compared deployed GitHub Pages files with local hashes after repairs.
- Checked the public game and repository while signed out.

## Current Links

- Public game: https://james-regi.github.io/Scholar-V2/
- Public source: https://github.com/James-Regi/Scholar-V2
